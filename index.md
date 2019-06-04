---
layout: default
---
  <div class="site-wrap">
    <div class="site-blocks-cover overlay" style="background-image: url({{site.url}}/images/hero_bg_1.jpg);" data-aos="fade" data-stellar-background-ratio="0.5">
      <div class="container">
        <div class="row align-items-center justify-content-center text-center">

          <div class="col-md-8" data-aos="fade-up" data-aos-delay="400">
            {% assign latest_post = site.posts.first %}
            <h2 class="text-white font-weight-light mb-2 display-4">{{ latest_post.title }}</h2>
            <div class="text-white mb-4"><span class="text-white-opacity-05"><small>{{latest_post.people}} | {{latest_post.date | date: "%-d %B %Y"}} | {{latest_post.duration}}</small></span></div>
            <p><a href="{{latest_post.url}}" class="btn btn-primary btn-sm py-3 px-4 small">Read The Show Notes</a></p>

            <div class="player">
              <audio id="player1" preload="none" controls style="max-width: 100%">
                <source src="{{latest_post.audio}}" type="audio/mp3">
              </audio>
            </div>

          </div>
        </div>
      </div>
    </div>

    {% assign post_count = site.posts | size %}
    {% if post_count > 1 %}

    <section class="site-section bg-light">
      <div class="container">

        <div class="row mb-5" data-aos="fade-up">
          <div class="col-md-12 text-center">
            <h2 class="font-weight-bold text-black">Recent Podcasts</h2>
          </div>
        </div>

        {% for post in site.posts limit: 5 offset: 1 %}

        <div class="d-block d-md-flex podcast-entry bg-white mb-5" data-aos="fade-up">
          <div class="image" style="background-image: url('{{site.url}}{{post.coverart}}');"></div>
          <div class="text">

            <h3 class="font-weight-light"><a href="{{site.url}}{{post.url}}">{{post.title}}</a></h3>
            <div class="text-white mb-3"><span class="text-black-opacity-05"><small>{{post.people}} | {{post.date | date: "%-d %B %Y"}} | {{post.duration}}</small></span></div>
            <p class="mb-4">{{post.summary}}</p>

            <div class="player">
              <audio id="player{{forloop.index}}" preload="none" controls style="max-width: 100%">
                <source src="{{post.audio}}" type="audio/mp3">
              </audio>
            </div>

          </div>
        </div>

        {% endfor %}
        </div>
<!--
      <div class="container" data-aos="fade-up">
        <div class="row">
          <div class="col-md-12 text-center">
            <div class="site-block-27">
              <ul>
                <li><a href="#">&lt;</a></li>
                <li class="active"><span>1</span></li>
                <li><a href="#">2</a></li>
                <li><a href="#">3</a></li>
                <li><a href="#">4</a></li>
                <li><a href="#">5</a></li>
                <li><a href="#">&gt;</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
-->
    </section>
    {% endif %}
<!--
    <section class="site-section">
      <div class="container" data-aos="fade-up">
        <div class="row mb-5">
          <div class="col-md-12 text-center">
            <h2 class="font-weight-bold text-black">Behind The Mic</h2>
          </div>
        </div>
        <div class="row">
          <div class="col-md-6 col-lg-4 mb-5 mb-lg-5">
            <div class="team-member">

              <img src="{{site.url}}/images/people/person_1.jpg" alt="Image" class="img-fluid">

              <div class="text">

                <h2 class="mb-2 font-weight-light h4">Megan Smith</h2>
                <span class="d-block mb-2 text-white-opacity-05">Creative Director</span>
                <p class="mb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit ullam reprehenderit nemo.</p>
                <p>
                  <a href="#" class="text-white p-2"><span class="icon-facebook"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-twitter"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-linkedin"></span></a>
                </p>
              </div>

            </div>
          </div>

          <div class="col-md-6 col-lg-4 mb-5 mb-lg-5">
            <div class="team-member">

              <img src="{{site.url}}/images/people/person_2.jpg" alt="Image" class="img-fluid">

              <div class="text">

                <h2 class="mb-2 font-weight-light h4">Brooke Cagle</h2>
                <span class="d-block mb-2 text-white-opacity-05">Creative Director</span>
                <p class="mb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit ullam reprehenderit nemo.</p>
                <p>
                  <a href="#" class="text-white p-2"><span class="icon-facebook"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-twitter"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-linkedin"></span></a>
                </p>
              </div>

            </div>
          </div>

          <div class="col-md-6 col-lg-4 mb-5 mb-lg-5">
            <div class="team-member">

              <img src="{{site.url}}/images/people/person_3.jpg" alt="Image" class="img-fluid">

              <div class="text">

                <h2 class="mb-2 font-weight-light h4">Philip Martin</h2>
                <span class="d-block mb-2 text-white-opacity-05">Creative Director</span>
                <p class="mb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit ullam reprehenderit nemo.</p>
                <p>
                  <a href="#" class="text-white p-2"><span class="icon-facebook"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-twitter"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-linkedin"></span></a>
                </p>
              </div>

            </div>
          </div>

          <div class="col-md-6 col-lg-4 mb-5 mb-lg-5">
            <div class="team-member">

              <img src="{{site.url}}/images/people/person_4.jpg" alt="Image" class="img-fluid">

              <div class="text">

                <h2 class="mb-2 font-weight-light h4">Steven Ericson</h2>
                <span class="d-block mb-2 text-white-opacity-05">Creative Director</span>
                <p class="mb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit ullam reprehenderit nemo.</p>
                <p>
                  <a href="#" class="text-white p-2"><span class="icon-facebook"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-twitter"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-linkedin"></span></a>
                </p>
              </div>

            </div>
          </div>

          <div class="col-md-6 col-lg-4 mb-5 mb-lg-5">
            <div class="team-member">

              <img src="{{site.url}}/images/people/person_5.jpg" alt="Image" class="img-fluid">

              <div class="text">

                <h2 class="mb-2 font-weight-light h4">Nathan Dumlao</h2>
                <span class="d-block mb-2 text-white-opacity-05">Creative Director</span>
                <p class="mb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit ullam reprehenderit nemo.</p>
                <p>
                  <a href="#" class="text-white p-2"><span class="icon-facebook"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-twitter"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-linkedin"></span></a>
                </p>
              </div>

            </div>
          </div>

          <div class="col-md-6 col-lg-4 mb-5 mb-lg-5">
            <div class="team-member">

              <img src="{{site.url}}/images/people/person_6.jpg" alt="Image" class="img-fluid">

              <div class="text">

                <h2 class="mb-2 font-weight-light h4">Brooke Cagle</h2>
                <span class="d-block mb-2 text-white-opacity-05">Creative Director</span>
                <p class="mb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit ullam reprehenderit nemo.</p>
                <p>
                  <a href="#" class="text-white p-2"><span class="icon-facebook"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-twitter"></span></a>
                  <a href="#" class="text-white p-2"><span class="icon-linkedin"></span></a>
                </p>
              </div>

            </div>
          </div>


        </div>
      </div>
    </section>

    <section class="site-section bg-light block-13">
      <div class="container">
        <div class="row mb-5">
          <div class="col-md-12 text-center">
            <h2 class="font-weight-bold text-black">Featured Guests</h2>
          </div>
        </div>
        <div class="nonloop-block-13 owl-carousel">

          <div class="text-center p-3 p-md-5 bg-white">
            <div class="mb-4">
              <img src="{{site.url}}/images/people/person_1.jpg" alt="Image" class="w-50 mx-auto img-fluid rounded-circle">
            </div>
            <div class="">
              <h3 class="font-weight-light h5">Megan Smith</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et, iusto. Aliquam illo, cum sed ea? Ducimus quos, ea?</p>
            </div>
          </div>

          <div class="text-center p-3 p-md-5 bg-white">
            <div class="mb-4">
              <img src="{{site.url}}/images/people/person_2.jpg" alt="Image" class="w-50 mx-auto img-fluid rounded-circle">
            </div>
            <div class="">
              <h3 class="font-weight-light h5">Brooke Cagle</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et, iusto. Aliquam illo, cum sed ea? Ducimus quos, ea?</p>
            </div>
          </div>

          <div class="text-center p-3 p-md-5 bg-white">
            <div class="mb-4">
              <img src="{{site.url}}/images/people/person_3.jpg" alt="Image" class="w-50 mx-auto img-fluid rounded-circle">
            </div>
            <div class="">
              <h3 class="font-weight-light h5">Philip Martin</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et, iusto. Aliquam illo, cum sed ea? Ducimus quos, ea?</p>
            </div>
          </div>

          <div class="text-center p-3 p-md-5 bg-white">
            <div class="mb-4">
              <img src="{{site.url}}/images/people/person_4.jpg" alt="Image" class="w-50 mx-auto img-fluid rounded-circle">
            </div>
            <div class="">
              <h3 class="font-weight-light h5">Steven Ericson</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et, iusto. Aliquam illo, cum sed ea? Ducimus quos, ea?</p>
            </div>
          </div>

          <div class="text-center p-3 p-md-5 bg-white">
            <div class="mb-4">
              <img src="{{site.url}}/images/people/person_5.jpg" alt="Image" class="w-50 mx-auto img-fluid rounded-circle">
            </div>
            <div class="">
              <h3 class="font-weight-light h5">Nathan Dumlao</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et, iusto. Aliquam illo, cum sed ea? Ducimus quos, ea?</p>
            </div>
          </div>

          <div class="text-center p-3 p-md-5 bg-white">
            <div class="mb-4">
              <img src="{{site.url}}/images/people/person_6.jpg" alt="Image" class="w-50 mx-auto img-fluid rounded-circle">
            </div>
            <div class="">
              <h3 class="font-weight-light h5">Brook Smith</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et, iusto. Aliquam illo, cum sed ea? Ducimus quos, ea?</p>
            </div>
          </div>

        </div>
      </div>
    </section>
-->

    <div class="site-section bg-light block-13">
      <div class="container">
        <div class="row align-items-center justify-content-center text-center">

          <div class="col-md-6" data-aos="fade-up" data-aos-delay="400">
            <h2>Subscribe</h2>
            <p class="mb-5">Find us on your favourite podcast player, or add our RSS feed directly: <a href="https://learningleadership.net/feed/podcast/">https://learningleadership.net/feed/podcast</a></p>
            <p><a href="https://open.spotify.com/show/42ggp9JTKPofpM6g3NsBG0"><img src="{{site.url}}/images/spotify-podcast-badge-wht-grn.png" alt="listen on Spotify"></a></p>
            <!--
            <form action="#" method="post" class="site-block-subscribe">
                <div class="input-group mb-3">
                  <input type="text" class="form-control border-secondary text-white bg-transparent" placeholder="Enter Email" aria-label="Enter Email" aria-describedby="button-addon2">}
                  <div class="input-group-append">
                    <button class="btn btn-primary" type="button" id="button-addon3">Send</button>
                  </div>
                </div>
              </form>
              -->
          </div>
        </div>
      </div>
    </div>
