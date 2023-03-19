# Decentralized-Social-Media

A Social Media site that has web3 features like transparency and incentivisation which excites user to spend more time making content as well as take the top spot on the leadership board by liking and commenting the posts.

The smart contract is deployed on _polygon test network_ at "0x8b0B55bF9E1f23C8C925B0DbC0a10E33ff113927" address.

Try following commands to initialise-\
nvm install v16.19.0 // to download the required version of node.\
nvm use v16.19.0 //to use the required version of node\
npm install // to download/update the required dependencies\
npm run dev // to run the server at port 3000\

## Functions 
 createPost(string memory _content,string memory _imageURL)\
 likePost(address _postAuthor, uint256 _postId)\
 commentOnPost(address _postAuthor,uint256 _postId,string memory _content) \
 deleteComment(address _postAuthor, uint256 _postId)\
 deletePost(uint256 _postId)\
 editPost(uint256 _postId,string memory _content,string memory _imageURL)\
 getAllPosts() returns(Post[] memory)\
 getPostsByUser() returns (Post[] storage)\
 getPostById(uint256 _postId) returns (Post memory, address[] memory, uint256 id, address[] memory, string[] memory)\
 getPostCount(address user) returns (uint256)\
 censorPost(address postAuthor, uint256 postId)\
 uncensorPost(address postAuthor, uint256 postId)\

 ## Events
 NewPost(postId,author,content,timestamp,banCounter,isCensored,imageURL,score)\
 NewLike(postAuthor,likedBy,postId,like,authorScore)\
 NewComment(postAuthor,commentedBy,postId,content,authorScore)\
 DeleteComment(postAuthor,commentBy,postId,authorScore)\
 DeletePost(postId, postAuthor, authorScore)\
 EditPost(postId,author,content,timestamp,imageURL)\
 CensoredPost(moderator, postAuthor, postld, banCounter, isCensored)\
 UncensoredPost(address moderator, address postAuthor, uint256 postld, uint256 banCounter, bool isCensored)\

