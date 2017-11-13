# To Create Basic Board 

'post controller'
post#index => 모든 게시글을 보여준다. (root page)
post#new => 새로운 게시글을 만드는 form을 보여준다.
post#create => new에서 작성한 글을 쓴다. == db에 저장한다.
post#show => /post/show/:id 해당하는 글 1개만 보여준다.
post#modify => 게시글을 수정할 수 있는 form 을 보여준다.
post#update => modify에서 수정된 글을 db에 새로 저장한다. (update한다.)
post#destroy => show에서 확인한 글을 지울 수 있게 한다.

'user controller'
user#index => 모든 유저를 보여준다.
user#new => 새로운 유저를 만드는 form을 보여준다. (회원가입)
user#create => new에서 작성한 회원 정보를 db 에 저장한다.
user#show => /user/show/:id 해당하는 유저 1명만 보여준다.
user#login => form에 로그인이 가능한 페이지를 보여준다.
user#login_process => 로그인 정보와 db 유저 정보를 비교해 user를 로그인 시킨다.

1:1
1:N => User & Post (1명의 유저가 여러 포스트를 가질 수 있다. 포스트들은 특정한 유저에게 속해야 한다.)
M:N

 관계설정
post 모델에서 belongs_to :user
user 모델에서 has_many :posts
