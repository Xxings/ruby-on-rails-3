# Clone Coding

[link]()



## Settings

Ruby. 2.7

Ruby on Rails 5.2.4.3



## GEM

### :develop

> Rails 및 기타 Rack 앱에 대해 더 나은 오류 페이지를 제공합니다

* [better_errors](https://rubygems.org/gems/better_errors/versions/2.4) 

> 라이브 코딩 - 자동 리로드

* [guard](https://rubygems.org/gems/guard/versions/2.14.1)

* [guard-livereload](https://rubygems.org/gems/guard-livereload/versions/2.5.2)

> Flexbox를 기반으로 한 최신 CSS 프레임 워크

### :Operation

> CSS module

* [bulma-rails](https://rubygems.org/gems/bulma-rails/versions/0.6.1)

> 간편 Form

* [Simple_form](https://rubygems.org/gems/simple_form/versions/5.0.2)

> gravatar의 아바타 추가

* [gravatar-image-tag](https://rubygems.org/gems/gravatar_image_tag/versions/1.2.0)

> 권한

* [devise](https://rubygems.org/gems/devise/versions/4.3.0)

## Branch

**feature-1-tweet : 환경세팅 및 아래의 작업**

* Guard

* Scaffolding " tweet"

* install gems

```bash
bundle exec guard init
rails g simple_form:install
rails g devise:install
rails g devise:view

bundle exec guard
```

https://bulma.io/documentation/components/navbar/

![image-20200810004129196](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghkzlsvhczj31410430st.jpg)



**feature-2-feed : Feed css**

​		font-awesome(https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css)

​		 Feed CRUD

​		![image-20200810010524798](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghl0aptn8mj30rf04vmxt.jpg)

<img src="https://tva1.sinaimg.cn/large/007S8ZIlgy1ghl0jg3xcfj30jy07uglz.jpg" alt="image-20200810011349323" style="zoom: 33%;" />

**feature-3-follow**

> undefined method `model_name' for nil:NilClass

말그대로 nil - show부분에 render했지만 바인드안됨

![image-20200810024941839](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghl3b7h7zmj31ng0hi40g.jpg)

**Feature-4-users**

redirect_to root_path

> cf) ruby로 만들어졌는는지 확인하는 방법 : 

```bash
rails g devise User
```

![image-20200810025506378](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghl3guale8j30xc083dj3.jpg)

```bash
 rails g migration AddFieldsToUsers
```



* emmet 다시한번 정리 (헷갈림)

Tweets N : user 1

belongs_to :user, class_name: "user", foreign_key: "user_id"

has_many :tweets  

```bash
rails g migration AddUserIdToTweets user_id:integer
```



rails c

```
@user = User
User.connection
```

![image-20200810033911633](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghl4qphdzcj30z302faag.jpg)



[devise docs](https://github.com/heartcombo/devise)

![image-20200810034412474](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghl4vx871tj30yu00r748.jpg)

name, username 안들어가는 문제 -> routes.rb에서 :controllers를 추가 안함.

![image-20200810034815858](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghl505buxaj3156016wej.jpg)

uninitialized constant Tweet::user /// Foreginkey 수정후 db:migration 안해서 생긴문제

![image-20200810040320178](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghl5ftngxtj324s0miacv.jpg)



**Feature-5-Auth**

user_session

User_registration

user_signed_in

current_user

![image-20200810073028880](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghlbfd4xo1j326u0q6af8.jpg)

![image-20200810073041781](https://tva1.sinaimg.cn/large/007S8ZIlgy1ghlbfkp8pdj32760pcadv.jpg)