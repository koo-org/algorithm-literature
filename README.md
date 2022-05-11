# algorithm-literature


<div class="entry-content">
		




<p>Social Media platforms are facing increasing scrutiny over the role played by algorithms in steering conversations on social media and in real life. Koo has always been a huge believer in fairness and transparency and it’s only fair that people know the broad variables used in algorithms to make the platform function smoothly.&nbsp; In the following article, we will talk about the broad philosophy and variables used for Koo’s algorithms. Generally companies don’t talk about algorithms openly to avoid risk of misuse by people with ill intent. We have avoided exact calculations as they may put the platform at a risk of being manipulated.&nbsp;</p>



<p>Koo works on algorithms. Once formulated and implemented, there is zero manual influence in the way these algorithms function. These algorithms are built to be fair, transparent and able to achieve smooth functioning at scale.&nbsp;</p>



<p><strong>Algorithm Customization</strong></p>



<p>While we start off by creating transparent intelligent algorithms to function smoothly and help people achieve more, our objective in the medium term will be to give the ability to users to create and customize their own variables and have control. We’ll give them the control on the kind of feed they want to see, who they want to get notified from and the type of trending content they want to see (basis location and category filters). This way we democratise content on the platform by giving users the ability to make choices that suit them best. Some power users would like these controls and it’s only fair to give it to those that seek it.</p>



<p><strong>Some important parts of Koo where algorithms are deployed are:</strong></p>



<ol><li>Feed</li><li>Trending section (# and words)</li><li>People feed</li><li>Notifications</li></ol>



<p>Before we dive deeper into each of the above, here are some terms that will be used in the discussion:<strong>:</strong></p>



<p><strong>Algorithm</strong>: This is a set of rules created and followed to achieve some set objective.</p>



<p><strong>Affinity</strong>: This is a calculation to depict the strength of the relationship between a follower and a followee. This is calculated by taking unique reactions as a percentage of unique content impressions.</p>



<p><strong>Time decay</strong>: 100 reactions within 1 minute vs 100 reactions in the last 10 hours need to be treated differently. Time decay is the calculation that helps normalize these two on the same level.</p>



<p><strong>Impressions</strong>: The number of views a piece of content gets when more than 3 seconds are spent on that content. The impressions can either be unique or total.&nbsp;</p>



<p><strong>Reactions</strong>: Reactions include actions such as Likes, Comments, Shares and Re-Koos. The reactions can either be unique or a summation.</p>



<ol><li><strong>Feed</strong></li></ol>



<p>The objective here is to help users quickly find the most relevant content immediately. Our assumption is that:</p>



<ul><li>Users have 1000s of Koos in their feed</li><li>Users would like to see the most relevant Koos right on top, without having to scroll the entire feed to find what or who they are looking for</li><li>The most relevant Koos are either<ul><li>From creators they have most affinity with (creators that they react to the most)</li><li>Content that is trending within their feed (has got many views and the most number of reactions, keeping in mind the time decay)</li></ul></li></ul>



<p>Our algorithm calculates these variables and surfaces all the Koos that qualify these criteria right on top in their feed. And the rest of the feed that doesn’t qualify is shown in the timeline fashion.</p>



<ul><li>There is an affinity score cut off that’s used to ensure that low affinity relationships don’t surface right on top.</li><li>We place a higher weightage on follower-followee affinity than trending contents and rank the Koos accordingly.</li><li>For the trending score, a cut-off is used for the number of impressions a piece of content got, and then the trending score is calculated for such Koos. When the reaction to impression ratio is healthy, these Koos qualify to be ranked and surfaced up in the feed.</li><li>Every Koo gets a score that helps us sequence these Koos in the feed.</li></ul>



<p>This helps Koo surface the most relevant content for every user right on top in their feed.</p>



<p>This feed algorithm went live on Feb 21, 2022. Till then all the users were shown a timeline feed. Koo keeps running experiments to change the weight of these variables or by trying new variables with the objective of showing users the most relevant content upfront.</p>



<p>We will further experiment with other variables such as content affinity (the category of content that a user prefers) and media type affinity (the kind of media that users prefer – text, image, video, gifs etc).</p>



<ol start="2"><li><strong>Trending section (# and words)</strong></li></ol>



<p>The trending section helps users know what the community is discussing. If any topic is new and gaining momentum, we try to highlight that. The 2 key variables used to discover these are (i) volume (the number of creators using either terms or # used in the Koos), and&nbsp;</p>



<p>(ii) velocity (time span within which these are created)&nbsp;</p>



<p>We identify words and # as the basis of this trending algorithm and run calculations with certain weights placed between volume and velocity. This helps us find topics that the community is discussing the most. This data is refreshed every 15 minutes and our objective will be to make this as live as possible and achieve shorter refresh periods.</p>



<ol start="3"><li><strong>People feed</strong></li></ol>



<p>Koo has a people feed that helps users&nbsp; quickly find people they can follow. All users who create content are called “creators” in the Koo ecosystem. All creators get access to the people feed, except for some that don’t qualify. The creators who don’t qualify are generally those with very shallow content that doesn’t add value to users (example of shallow content – just creating a post that says “Hello”, “Hi”, “How are you” etc).</p>



<p>Some creators get an Eminent tick mark basis a very transparent mechanism listed in detail here: <a href="https://www.kooapp.com/eminence">https://www.kooapp.com/eminence</a>. These are users who are either well-known or achievers internationally, nationally or locally. These are also usually people that users would want to connect with.&nbsp;</p>



<p>Our people feed surfaces such eminent creators and regular creators together to enable users to quickly find the people they want to follow. We categorize all the creators on the following basis:</p>



<ul><li>Their stated profession, and</li><li>The kind of content they create</li></ul>



<p>This makes it easy for users to discover the people they want to connect with.</p>



<p>We create a people score basis variables that show Quantity, Quality and Recency of their creations. The users are then ranked basis this calculation.</p>



<ul><li>Quality of their creations is a function of the reactions to impressions ratio their content receives.&nbsp;</li><li>Quantity of their creations is a function of the number of Koos within a timeframe.</li><li>Recency of their creations is about how active they are on the platform basis how often they Koo and the last time frame they were active in.</li></ul>



<p>This calculation transparently ranks the creators that are then shown to users. This way Koo is able to fairly help all those creators who&nbsp; work hard to keep in touch with their followers over those who are less frequent, less engaging and less recent.</p>



<p>Koo also has a lot of machine learning deployed to categorize people into accurate profession buckets so that users can discover people of a particular profession and to categorize people on the basis of the content they create. We use advanced machine learning models algorithms to categorize content on the basis of the words, # and visual content used.</p>



<p>Topics are created out of these clusters and users can follow such topics to get rich and relevant content around these topics, in their feed.</p>



<ol start="4"><li><strong>Notifications</strong></li></ol>



<p>Every user follows many creators and hence can have a large feed. It’s not possible to notify them every time someone that they follow, Koos. Hence an algorithm is used for notifications. The objective of this algorithm is to show the most relevant notifications to a user.&nbsp;</p>



<p>The basis for notifications is the follower-followee affinity score (defined above). The stronger the relationship, the stronger the score and the higher likelihood of the user getting notified about the Koos created by this person.&nbsp;&nbsp;</p>



<p>Notifications on Koo can be divided into the following categories:</p>



<ol><li>New Koo created</li><li>New followers</li><li>Reactions on creations</li><li>Informational notifications</li><li>Others</li></ol>



<p><strong>New Koo created: </strong>Basis the affinity score that a user has with a certain follower, a score is assigned. If the affinity score exceeds a cut off, they will be notified a certain number of times when this person Koos.</p>



<p><strong>New followers: </strong>Everytime someone gets a new follower, they are informed through a notification.</p>



<p><strong>Reactions on creations: </strong>Everytime a creator gets a new reaction on their Koo, they are notified.</p>



<p><strong>Informational notifications: </strong>These are some notifications that help users engage with the platform. Some examples are:</p>



<ul><li>Number of Koos in your feed: Sent in the evening to inform them about the number of Koos in their feed.</li><li>Creators who Koo’d today: A summary of the creators that created today.</li><li>Summary of activity on their profile: A summary of the people who viewed their profile and the summary of followers and reactions they received the previous day.</li></ul>



<p><strong>Algorithms and their place in Koo’s Mission</strong></p>



<p>Koo is a young start-up that’s driven by the broader mission of helping people connect better and deeper with communities they care about. We try to achieve this mission with the use of technology so that we can cater to the world at large in the best possible way. The reality is that users connect better when they find people that speak their language and vice versa. In a world that has 1000s of languages, we are divided by language and hence look for content from such people. Our objective is to help users that speak the same language to find each other in the easiest way possible and then to bridge the divide between people that speak different languages, to facilitate a fluid exchange of ideas, irrespective of language preferences.</p>



<p>We have made huge strides in achieving the former through our immersive language based micro-blogging. While micro-blogging has existed since a few decades, many languages other than English are very poorly penetrated by existing solutions. Koo is an innovator in language-based micro-blogging given the large language diversity it sees in its home country, India. While Koo is from India, the vision is to take this solution to the entire world and help people of all languages to connect deeply with those that speak their language and then with the rest of the world.</p>



<p>While we keep creating a better and more connected world through our creation, Koo, we look for everyone’s support in our journey to help us connect people better on the fundamental values of fairness, transparency in everything we do!</p>
	</div>
