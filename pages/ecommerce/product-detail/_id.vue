<script>
import { products } from "../data-products";

/**
 * Product-detail component
 */
export default {
  head() {
    return {
      title: `${this.title} | Minton - Nuxtjs Responsive Admin Dashboard Template`,
    };
  },
  asyncData({ params }) {
    const productDetail = products.find(
      (user) => String(user.id) === params.id
    );
    return {
      productDetail,
    };
  },
  data() {
    return {
      title: "Product Detail",
      items: [
        {
          text: "Minton",
        },
        {
          text: "Ecommerce",
        },
        {
          text: "Product Detail",
          active: true,
        },
      ],
    };
  },
  middleware: "router-auth",
  methods: {
    /**
     * Change the product
     */
    changeImage(data) {
      document.getElementById("myImage").src = data.target.src;
    },
  },
};
</script>

<template>
  <div>
    <PageHeader :title="title" :items="items" />
    <div class="row">
      <div class="col-lg-12">
        <div class="card">
          <div class="card-body">
            <div class="row">
              <div class="col-lg-5">
                <div class="row justify-content-center">
                  <div class="col-xl-8">
                    <div
                      id="product-carousel"
                      class="carousel slide product-detail-carousel"
                      data-ride="carousel"
                    >
                      <div class="carousel-inner">
                        <div class="carousel-item active">
                          <div>
                            <img
                              src="~/assets/images/products/product-6.png"
                              alt="product-img"
                              id="myImage"
                              class="img-fluid"
                            />
                          </div>
                        </div>
                        <div class="carousel-item">
                          <div>
                            <img
                              src="~/assets/images/products/product-8.png"
                              alt="product-img"
                              class="img-fluid"
                            />
                          </div>
                        </div>
                        <div class="carousel-item">
                          <div>
                            <img
                              src="~/assets/images/products/product-1.png"
                              alt="product-img"
                              class="img-fluid"
                            />
                          </div>
                        </div>
                      </div>
                      <ol
                        class="carousel-indicators product-carousel-indicators mt-2"
                      >
                        <li
                          data-target="#product-carousel"
                          data-slide-to="0"
                          class="active"
                        >
                          <img
                            src="~/assets/images/products/product-6.png"
                            @click="changeImage($event)"
                            alt="product-img"
                            class="img-fluid product-nav-img"
                          />
                        </li>
                        <li data-target="#product-carousel" data-slide-to="1">
                          <img
                            src="~/assets/images/products/product-8.png"
                            @click="changeImage($event)"
                            alt="product-img"
                            class="img-fluid product-nav-img"
                          />
                        </li>
                        <li data-target="#product-carousel" data-slide-to="2">
                          <img
                            src="~/assets/images/products/product-1.png"
                            @click="changeImage($event)"
                            alt="product-img"
                            class="img-fluid product-nav-img"
                          />
                        </li>
                      </ol>
                    </div>
                  </div>
                </div>
              </div>

              <div class="col-lg-7">
                <div>
                  <div>
                    <a href="#" class="text-primary">T-shirts</a>
                  </div>
                  <h4 class="mb-1">
                    Hoodie for men (Blue)
                    <a href="javascript: void(0);" class="text-muted">
                      <i class="mdi mdi-square-edit-outline ml-2"></i>
                    </a>
                  </h4>

                  <p class="text-muted mr-3 font-16">
                    <span class="mdi mdi-star text-warning"></span>
                    <span class="mdi mdi-star text-warning"></span>
                    <span class="mdi mdi-star text-warning"></span>
                    <span class="mdi mdi-star text-warning"></span>
                    <span class="mdi mdi-star"></span>
                  </p>

                  <div class="mt-3">
                    <h6 class="text-danger text-uppercase">10 % Off</h6>
                    <h4>
                      Price :
                      <span class="text-muted mr-2">
                        <del>$ 50</del>
                      </span>
                      <b>$ 45</b>
                    </h4>
                  </div>
                  <hr />

                  <div>
                    <p>
                      If several languages coalesce, the grammar of the
                      resulting language is more simple and regular than that of
                      the individual new common simple and regular than existing
                    </p>

                    <div class="mt-3">
                      <h5 class="font-size-14">Specification :</h5>
                      <div class="row">
                        <div class="col-md-6">
                          <ul class="list-unstyled product-desc-list">
                            <li>
                              <i
                                class="mdi mdi-circle-medium mr-1 align-middle"
                              ></i>
                              Full Sleeve
                            </li>
                            <li>
                              <i
                                class="mdi mdi-circle-medium mr-1 align-middle"
                              ></i>
                              Cotton
                            </li>
                            <li>
                              <i
                                class="mdi mdi-circle-medium mr-1 align-middle"
                              ></i>
                              All Sizes available
                            </li>
                            <li>
                              <i
                                class="mdi mdi-circle-medium mr-1 align-middle"
                              ></i>
                              4 Different Color
                            </li>
                          </ul>
                        </div>
                        <div class="col-md-6">
                          <ul class="list-unstyled product-desc-list">
                            <li>
                              <i
                                class="mdi mdi-circle-medium mr-1 align-middle"
                              ></i>
                              All Sizes available
                            </li>
                            <li>
                              <i
                                class="mdi mdi-circle-medium mr-1 align-middle"
                              ></i>
                              4 Different Color
                            </li>
                          </ul>
                        </div>
                      </div>
                    </div>

                    <div>
                      <form class="form-inline mb-3">
                        <label class="my-1 mr-2" for="quantityinput"
                          >Quantity</label
                        >
                        <select
                          class="custom-select my-1 mr-sm-3"
                          id="quantityinput"
                        >
                          <option value="1">1</option>
                          <option value="2">2</option>
                          <option value="3">3</option>
                          <option value="4">4</option>
                          <option value="5">5</option>
                          <option value="6">6</option>
                          <option value="7">7</option>
                        </select>

                        <label class="my-1 mr-2" for="sizeinput">Size</label>
                        <select
                          class="custom-select my-1 mr-sm-3"
                          id="sizeinput"
                        >
                          <option selected>Small</option>
                          <option value="1">Medium</option>
                          <option value="2">Large</option>
                          <option value="3">X-large</option>
                        </select>
                      </form>

                      <div>
                        <button
                          type="button"
                          class="btn btn-success waves-effect waves-light"
                        >
                          <span class="btn-label">
                            <i class="mdi mdi-cart"></i> </span
                          >Add to cart
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <!-- end row -->

            <h5 class="mt-5 mb-3">Available Stocks & Outlets</h5>
            <div class="table-responsive">
              <table class="table table-bordered table-centered mb-0">
                <thead class="thead-light">
                  <tr>
                    <th>Outlets</th>
                    <th>Price</th>
                    <th>Stock</th>
                    <th>Revenue</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>ASOS Ridley Outlet - NYC</td>
                    <td>$139.58</td>
                    <td>
                      <div class="row align-items-center no-gutters">
                        <div class="col-auto">
                          <span class="mr-2">27%</span>
                        </div>
                        <div class="col">
                          <div class="progress progress-sm">
                            <div
                              class="progress-bar bg-danger"
                              role="progressbar"
                              style="width: 27%"
                              aria-valuenow="27"
                              aria-valuemin="0"
                              aria-valuemax="100"
                            ></div>
                          </div>
                        </div>
                      </div>
                    </td>
                    <td>$1,89,547</td>
                  </tr>
                  <tr>
                    <td>Marco Outlet - SRT</td>
                    <td>$149.99</td>
                    <td>
                      <div class="row align-items-center no-gutters">
                        <div class="col-auto">
                          <span class="mr-2">71%</span>
                        </div>
                        <div class="col">
                          <div class="progress progress-sm">
                            <div
                              class="progress-bar bg-success"
                              role="progressbar"
                              style="width: 71%"
                              aria-valuenow="71"
                              aria-valuemin="0"
                              aria-valuemax="100"
                            ></div>
                          </div>
                        </div>
                      </div>
                    </td>
                    <td>$87,245</td>
                  </tr>
                  <tr>
                    <td>Chairtest Outlet - HY</td>
                    <td>$135.87</td>
                    <td>
                      <div class="row align-items-center no-gutters">
                        <div class="col-auto">
                          <span class="mr-2">82%</span>
                        </div>
                        <div class="col">
                          <div class="progress progress-sm">
                            <div
                              class="progress-bar bg-success"
                              role="progressbar"
                              style="width: 82%"
                              aria-valuenow="82"
                              aria-valuemin="0"
                              aria-valuemax="100"
                            ></div>
                          </div>
                        </div>
                      </div>
                    </td>
                    <td>$5,87,478</td>
                  </tr>
                  <tr>
                    <td>Nworld Group - India</td>
                    <td>$159.89</td>
                    <td>
                      <div class="row align-items-center no-gutters">
                        <div class="col-auto">
                          <span class="mr-2">42%</span>
                        </div>
                        <div class="col">
                          <div class="progress progress-sm">
                            <div
                              class="progress-bar bg-warning"
                              role="progressbar"
                              style="width: 42%"
                              aria-valuenow="42"
                              aria-valuemin="0"
                              aria-valuemax="100"
                            ></div>
                          </div>
                        </div>
                      </div>
                    </td>
                    <td>$55,781</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
        <!-- end card -->
      </div>
    </div>
    <!-- end row -->
  </div>
</template>
