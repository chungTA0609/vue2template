<script>
/**
 * Contacts profile component
 */
export default {
  head() {
    return {
      title: `${this.title} | Minton - Nuxtjs Responsive Admin Dashboard Template`,
    };
  },
  data() {
    return {
      title: "Profile",
      items: [
        {
          text: "Minton",
          href: "/",
        },
        {
          text: "Apps",
          href: "/",
        },
        {
          text: "Profile",
          active: true,
        },
      ],
    };
  },
  middleware: "router-auth",
};
</script>

<template>
  <div>
    <PageHeader :title="title" :items="items" />
    <div class="row">
      <div class="col-lg-4 col-xl-4">
        <div class="card">
          <div class="card-body text-center">
            <img
              src="~/assets/images/users/avatar-1.jpg"
              class="rounded-circle avatar-xl img-thumbnail"
              alt="profile-image"
            />

            <h4 class="mt-3 mb-0">Nik G. Patel</h4>
            <p class="text-muted">@webdesigner</p>

            <button
              type="button"
              class="btn btn-success btn-xs waves-effect mb-2 waves-light"
            >
              Follow
            </button>
            <button
              type="button"
              class="btn btn-danger btn-xs waves-effect mb-2 waves-light"
            >
              Message
            </button>

            <div class="text-left mt-3">
              <h4 class="font-13 text-uppercase">About Me :</h4>
              <p class="text-muted font-13 mb-3">
                Hi I'm Johnathn Deo,has been the industry's standard dummy text
                ever since the 1500s, when an unknown printer took a galley of
                type.
              </p>

              <div class="table-responsive">
                <table class="table table-borderless table-sm">
                  <tbody>
                    <tr>
                      <th scope="row">Full Name :</th>
                      <td class="text-muted">Nik G. Patel</td>
                    </tr>
                    <tr>
                      <th scope="row">Mobile :</th>
                      <td class="text-muted">(123) 123 1234</td>
                    </tr>
                    <tr>
                      <th scope="row">Email :</th>
                      <td class="text-muted">user@email.domain</td>
                    </tr>
                    <tr>
                      <th scope="row">Location :</th>
                      <td class="text-muted">USA</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>

            <ul class="social-list list-inline mt-3 mb-0">
              <li class="list-inline-item">
                <a
                  href="javascript: void(0);"
                  class="social-list-item border-purple text-purple"
                >
                  <i class="mdi mdi-facebook"></i>
                </a>
              </li>
              <li class="list-inline-item">
                <a
                  href="javascript: void(0);"
                  class="social-list-item border-danger text-danger"
                >
                  <i class="mdi mdi-google"></i>
                </a>
              </li>
              <li class="list-inline-item">
                <a
                  href="javascript: void(0);"
                  class="social-list-item border-info text-info"
                >
                  <i class="mdi mdi-twitter"></i>
                </a>
              </li>
              <li class="list-inline-item">
                <a
                  href="javascript: void(0);"
                  class="social-list-item border-secondary text-secondary"
                >
                  <i class="mdi mdi-github"></i>
                </a>
              </li>
            </ul>
          </div>
          <!-- end card-box -->
        </div>
        <div class="card">
          <div class="card-body">
            <h4 class="header-title">Skills</h4>
            <p class="sub-header mb-3">
              Everyone realizes why a new common language would be desirable
            </p>

            <div class="pt-1">
              <h6 class="text-uppercase mt-0">
                HTML5
                <span class="float-right">90%</span>
              </h6>
              <b-progress
                height="5px"
                :value="90"
                variant="purple"
              ></b-progress>
            </div>

            <div class="mt-2 pt-1">
              <h6 class="text-uppercase">
                PHP
                <span class="float-right">67%</span>
              </h6>
              <b-progress
                height="5px"
                :value="67"
                variant="purple"
              ></b-progress>
            </div>

            <div class="mt-2 pt-1">
              <h6 class="text-uppercase">
                WordPress
                <span class="float-right">48%</span>
              </h6>
              <b-progress
                height="5px"
                :value="48"
                variant="purple"
              ></b-progress>
            </div>

            <div class="mt-2 pt-1">
              <h6 class="text-uppercase">
                Laravel
                <span class="float-right">95%</span>
              </h6>
              <b-progress
                height="5px"
                :value="95"
                variant="purple"
              ></b-progress>
            </div>

            <div class="mt-2 pt-1">
              <h6 class="text-uppercase">
                ReactJs
                <span class="float-right">72%</span>
              </h6>
              <b-progress
                height="5px"
                :value="72"
                variant="purple"
              ></b-progress>
            </div>
          </div>
          <!-- end card-box-->
        </div>
      </div>
      <!-- end col-->

      <div class="col-lg-8 col-xl-8">
        <div class="card">
          <div class="card-body">
            <b-tabs content-class="mt-1" pills class="navtab-bg">
              <b-tab active>
                <template v-slot:title>
                  <i class="mdi mdi-face-profile mr-1"></i>About Me
                </template>
                <div>
                  <h5 class="mb-4 text-uppercase">Experience</h5>

                  <ul class="list-unstyled timeline-sm">
                    <li class="timeline-sm-item">
                      <span class="timeline-sm-date">2015 - 18</span>
                      <h5 class="mt-0 mb-1">Lead designer / Developer</h5>
                      <p>websitename.com</p>
                      <p class="text-muted mt-2">
                        Everyone realizes why a new common language would be
                        desirable: one could refuse to pay expensive
                        translators. To achieve this, it would be necessary to
                        have uniform grammar, pronunciation and more common
                        words.
                      </p>
                    </li>
                    <li class="timeline-sm-item">
                      <span class="timeline-sm-date">2012 - 15</span>
                      <h5 class="mt-0 mb-1">Senior Graphic Designer</h5>
                      <p>Software Inc.</p>
                      <p class="text-muted mt-2">
                        If several languages coalesce, the grammar of the
                        resulting language is more simple and regular than that
                        of the individual languages. The new common language
                        will be more simple and regular than the existing
                        European languages.
                      </p>
                    </li>
                    <li class="timeline-sm-item">
                      <span class="timeline-sm-date">2010 - 12</span>
                      <h5 class="mt-0 mb-1">Graphic Designer</h5>
                      <p>themesbrand LLP</p>
                      <p class="text-muted mt-2 mb-0">
                        The European languages are members of the same family.
                        Their separate existence is a myth. For science music
                        sport etc, Europe uses the same vocabulary. The
                        languages only differ in their grammar their
                        pronunciation.
                      </p>
                    </li>
                  </ul>

                  <h5 class="mb-3 mt-5 text-uppercase">Projects</h5>
                  <div class="table-responsive mb-0">
                    <table class="table table-borderless mb-0">
                      <thead class="thead-light">
                        <tr>
                          <th>#</th>
                          <th>Project Name</th>
                          <th>Start Date</th>
                          <th>Due Date</th>
                          <th>Status</th>
                          <th>Clients</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr>
                          <td>1</td>
                          <td>App design and development</td>
                          <td>01/01/2015</td>
                          <td>10/15/2018</td>
                          <td>
                            <span class="badge badge-info"
                              >Work in Progress</span
                            >
                          </td>
                          <td>Halette Boivin</td>
                        </tr>
                        <tr>
                          <td>2</td>
                          <td>Coffee detail page - Main Page</td>
                          <td>21/07/2016</td>
                          <td>12/05/2018</td>
                          <td>
                            <span class="badge badge-success">Pending</span>
                          </td>
                          <td>Durandana Jolicoeur</td>
                        </tr>
                        <tr>
                          <td>3</td>
                          <td>Poster illustation design</td>
                          <td>18/03/2018</td>
                          <td>28/09/2018</td>
                          <td>
                            <span class="badge badge-pink">Done</span>
                          </td>
                          <td>Lucas Sabourin</td>
                        </tr>
                        <tr>
                          <td>4</td>
                          <td>Drinking bottle graphics</td>
                          <td>02/10/2017</td>
                          <td>07/05/2018</td>
                          <td>
                            <span class="badge badge-purple"
                              >Work in Progress</span
                            >
                          </td>
                          <td>Donatien Brunelle</td>
                        </tr>
                        <tr>
                          <td>5</td>
                          <td>Landing page design - Home</td>
                          <td>17/01/2017</td>
                          <td>25/05/2021</td>
                          <td>
                            <span class="badge badge-warning">Coming soon</span>
                          </td>
                          <td>Karel Auberjo</td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
                <!-- end tab-pane -->
              </b-tab>
              <b-tab>
                <template v-slot:title>
                  <i class="mdi mdi-settings-outline mr-1"></i>Settings
                </template>
                <form>
                  <h5 class="mb-3 text-uppercase bg-light p-2">
                    <i class="mdi mdi-account-circle mr-1"></i> Personal Info
                  </h5>
                  <div class="row">
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="firstname">First Name</label>
                        <input
                          id="firstname"
                          type="text"
                          class="form-control"
                          placeholder="Enter first name"
                        />
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="lastname">Last Name</label>
                        <input
                          id="lastname"
                          type="text"
                          class="form-control"
                          placeholder="Enter last name"
                        />
                      </div>
                    </div>
                    <!-- end col -->
                  </div>
                  <!-- end row -->

                  <div class="row">
                    <div class="col-12">
                      <div class="form-group">
                        <label for="userbio">Bio</label>
                        <textarea
                          id="userbio"
                          class="form-control"
                          rows="4"
                          placeholder="Write something..."
                        ></textarea>
                      </div>
                    </div>
                    <!-- end col -->
                  </div>
                  <!-- end row -->

                  <div class="row">
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="useremail">Email Address</label>
                        <input
                          id="useremail"
                          type="email"
                          class="form-control"
                          placeholder="Enter email"
                        />
                        <span class="form-text text-muted">
                          <small>
                            If you want to change email please
                            <a href="javascript: void(0);">click</a> here.
                          </small>
                        </span>
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="userpassword">Password</label>
                        <input
                          id="userpassword"
                          type="password"
                          class="form-control"
                          placeholder="Enter password"
                        />
                        <span class="form-text text-muted">
                          <small>
                            If you want to change password please
                            <a href="javascript: void(0);">click</a> here.
                          </small>
                        </span>
                      </div>
                    </div>
                    <!-- end col -->
                  </div>
                  <!-- end row -->

                  <h5 class="mb-3 text-uppercase bg-light p-2">
                    <i class="mdi mdi-office-building mr-1"></i> Company Info
                  </h5>
                  <div class="row">
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="companyname">Company Name</label>
                        <input
                          id="companyname"
                          type="text"
                          class="form-control"
                          placeholder="Enter company name"
                        />
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="cwebsite">Website</label>
                        <input
                          id="cwebsite"
                          type="text"
                          class="form-control"
                          placeholder="Enter website url"
                        />
                      </div>
                    </div>
                    <!-- end col -->
                  </div>
                  <!-- end row -->

                  <h5 class="mb-3 text-uppercase bg-light p-2">
                    <i class="mdi mdi-earth mr-1"></i> Social
                  </h5>
                  <div class="row">
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="social-fb">Facebook</label>
                        <div class="input-group">
                          <div class="input-group-prepend">
                            <span class="input-group-text">
                              <i class="fab fa-facebook-square"></i>
                            </span>
                          </div>
                          <input
                            id="social-fb"
                            type="text"
                            class="form-control"
                            placeholder="Url"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="social-tw">Twitter</label>
                        <div class="input-group">
                          <div class="input-group-prepend">
                            <span class="input-group-text">
                              <i class="fab fa-twitter"></i>
                            </span>
                          </div>
                          <input
                            id="social-tw"
                            type="text"
                            class="form-control"
                            placeholder="Username"
                          />
                        </div>
                      </div>
                    </div>
                    <!-- end col -->
                  </div>
                  <!-- end row -->

                  <div class="row">
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="social-insta">Instagram</label>
                        <div class="input-group">
                          <div class="input-group-prepend">
                            <span class="input-group-text">
                              <i class="fab fa-instagram"></i>
                            </span>
                          </div>
                          <input
                            id="social-insta"
                            type="text"
                            class="form-control"
                            placeholder="Url"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="social-lin">Linkedin</label>
                        <div class="input-group">
                          <div class="input-group-prepend">
                            <span class="input-group-text">
                              <i class="fab fa-linkedin"></i>
                            </span>
                          </div>
                          <input
                            id="social-lin"
                            type="text"
                            class="form-control"
                            placeholder="Url"
                          />
                        </div>
                      </div>
                    </div>
                    <!-- end col -->
                  </div>
                  <!-- end row -->

                  <div class="row">
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="social-sky">Skype</label>
                        <div class="input-group">
                          <div class="input-group-prepend">
                            <span class="input-group-text">
                              <i class="fab fa-skype"></i>
                            </span>
                          </div>
                          <input
                            id="social-sky"
                            type="text"
                            class="form-control"
                            placeholder="@username"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="form-group">
                        <label for="social-gh">Github</label>
                        <div class="input-group">
                          <div class="input-group-prepend">
                            <span class="input-group-text">
                              <i class="fab fa-github"></i>
                            </span>
                          </div>
                          <input
                            id="social-gh"
                            type="text"
                            class="form-control"
                            placeholder="Username"
                          />
                        </div>
                      </div>
                    </div>
                    <!-- end col -->
                  </div>
                  <!-- end row -->

                  <div class="text-right">
                    <button type="submit" class="btn btn-success mt-2">
                      <i class="mdi mdi-content-save"></i> Save
                    </button>
                  </div>
                </form>
              </b-tab>
            </b-tabs>
          </div>
          <!-- end card-box-->
        </div>
      </div>
      <!-- end col -->
    </div>
    <!-- end row-->
  </div>
</template>
