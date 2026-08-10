import React from "react";
import {
  ShoppingBag,
  Truck,
  ShieldCheck,
  RefreshCw,
  Star,
  Search,
  Menu,
  ChevronRight,
  Heart,
  Sparkles,
  BadgePercent,
  Headphones,
  ArrowRight,
  Instagram,
  Facebook,
  Youtube,
} from "lucide-react";

const products = [
  {
    name: "Smart Kitchen Cleaning Brush",
    price: "₹299",
    oldPrice: "₹499",
    tag: "Best Seller",
  },
  {
    name: "2-in-1 Soap Dispensing Brush",
    price: "₹349",
    oldPrice: "₹599",
    tag: "Top Rated",
  },
  {
    name: "Portable Mini Fan",
    price: "₹499",
    oldPrice: "₹799",
    tag: "Hot Deal",
  },
  {
    name: "LED Motion Sensor Light",
    price: "₹399",
    oldPrice: "₹699",
    tag: "Trending",
  },
];

const categories = [
  "Home & Kitchen",
  "Gadgets",
  "Beauty",
  "Fitness",
  "Car Accessories",
  "Lifestyle",
];

const features = [
  {
    icon: Truck,
    title: "Fast & Reliable Delivery",
    text: "Nationwide shipping with clear tracking and dependable order updates.",
  },
  {
    icon: ShieldCheck,
    title: "Secure Checkout",
    text: "Safe payments designed to build customer trust and reduce friction.",
  },
  {
    icon: RefreshCw,
    title: "Easy Returns",
    text: "A simple return flow that keeps buyers confident at checkout.",
  },
  {
    icon: Headphones,
    title: "Customer Support",
    text: "Friendly customer support to handle order questions quickly.",
  },
];

const testimonials = [
  {
    name: "Aman Verma",
    text: "The store feels premium, the checkout is simple, and my order arrived exactly on time.",
  },
  {
    name: "Priya Sharma",
    text: "Very clean design and great product quality. I loved how easy it was to browse.",
  },
  {
    name: "Rahul Singh",
    text: "Excellent support and fast delivery updates. Nolexcart looks like a brand people can trust.",
  },
];

function App() {
  return (
    <div className="min-h-screen bg-[#f7f8fc] text-slate-900">

      {/* HEADER */}
      <header className="sticky top-0 z-50 border-b border-slate-200 bg-white/90 backdrop-blur">
        <div className="mx-auto flex max-w-7xl items-center justify-between px-4 py-4 lg:px-8">

          <div className="flex items-center gap-3">
            <div className="flex h-11 w-11 items-center justify-center rounded-2xl bg-slate-900 text-white">
              <ShoppingBag className="h-5 w-5" />
            </div>

            <div>
              <div className="text-xl font-bold">
                Nolexcart
              </div>

              <div className="text-xs uppercase tracking-[0.3em] text-slate-500">
                Ecommerce • Dropshipping
              </div>
            </div>
          </div>

          <nav className="hidden items-center gap-8 lg:flex">
            <a href="#shop">Shop</a>
            <a href="#collections">Collections</a>
            <a href="#about">About</a>
            <a href="#reviews">Reviews</a>
            <a href="#faq">FAQ</a>
          </nav>

          <div className="flex items-center gap-3">

            <button className="hidden rounded-full border border-slate-200 bg-white p-3 lg:inline-flex">
              <Search className="h-4 w-4" />
            </button>

            <button className="hidden rounded-full border border-slate-200 bg-white p-3 lg:inline-flex">
              <Heart className="h-4 w-4" />
            </button>

            <button className="rounded-full bg-slate-900 px-5 py-3 text-sm font-semibold text-white">
              Shop Now
            </button>

            <button className="rounded-full border border-slate-200 bg-white p-3 lg:hidden">
              <Menu className="h-4 w-4" />
            </button>

          </div>
        </div>
      </header>


      {/* HERO */}
      <section className="relative overflow-hidden">

        <div className="absolute inset-0 bg-[radial-gradient(circle_at_top_left,_rgba(15,23,42,0.08),_transparent_32%),radial-gradient(circle_at_bottom_right,_rgba(59,130,246,0.12),_transparent_28%)]" />

        <div className="relative mx-auto grid max-w-7xl gap-12 px-4 py-16 lg:grid-cols-2 lg:px-8 lg:py-24">

          <div className="flex flex-col justify-center">

            <div className="mb-5 inline-flex w-fit items-center gap-2 rounded-full border border-slate-200 bg-white px-4 py-2 text-sm shadow-sm">
              <Sparkles className="h-4 w-4" />
              Trending products • Great prices
            </div>

            <h1 className="max-w-xl text-5xl font-black tracking-tight sm:text-6xl">
              Discover better products at{" "}
              <span className="text-slate-600">
                Nolexcart.
              </span>
            </h1>

            <p className="mt-6 max-w-xl text-lg leading-8 text-slate-600">
              Shop trending products, everyday essentials and smart finds
              with a simple, secure and premium shopping experience.
            </p>

            <div className="mt-8 flex flex-col gap-4 sm:flex-row">

              <button className="inline-flex items-center justify-center gap-2 rounded-full bg-slate-900 px-7 py-4 font-semibold text-white">
                Shop Now
                <ArrowRight className="h-4 w-4" />
              </button>

              <button className="inline-flex items-center justify-center gap-2 rounded-full border border-slate-300 bg-white px-7 py-4 font-semibold">
                Explore Collections
                <ChevronRight className="h-4 w-4" />
              </button>

            </div>

            <div className="mt-10 grid max-w-xl grid-cols-3 gap-4">

              <div className="rounded-3xl border bg-white p-5">
                <div className="text-2xl font-black">
                  10k+
                </div>
                <div className="text-sm text-slate-500">
                  Orders
                </div>
              </div>

              <div className="rounded-3xl border bg-white p-5">
                <div className="text-2xl font-black">
                  4.8/5
                </div>
                <div className="text-sm text-slate-500">
                  Rating
                </div>
              </div>

              <div className="rounded-3xl border bg-white p-5">
                <div className="text-2xl font-black">
                  24/7
                </div>
                <div className="text-sm text-slate-500">
                  Support
                </div>
              </div>

            </div>
          </div>


          {/* HERO CARD */}
          <div className="relative">

            <div className="overflow-hidden rounded-[2rem] border bg-white p-4 shadow-2xl">

              <div className="rounded-[1.5rem] bg-slate-900 p-6 text-white">

                <div className="text-sm uppercase tracking-[0.25em] text-slate-300">
                  Featured Drop
                </div>

                <div className="mt-3 text-3xl font-black">
                  Premium deals every day
                </div>

                <div className="mt-6 rounded-[1.5rem] border border-white/10 bg-white/5 p-5">

                  <div className="flex items-center gap-4">

                    <div className="flex h-14 w-14 items-center justify-center rounded-2xl bg-white text-slate-900">
                      <ShoppingBag />
                    </div>

                    <div>
                      <div className="font-semibold">
                        Nolexcart Collection
                      </div>

                      <div className="text-sm text-slate-300">
                        Quality products • Great value
                      </div>
                    </div>

                  </div>

                </div>

              </div>

              <div className="mt-4 grid gap-4 sm:grid-cols-2">

                <div className="rounded-[1.5rem] bg-slate-50 p-5">
                  <div className="text-sm text-slate-500">
                    Popular Category
                  </div>

                  <div className="mt-2 text-xl font-bold">
                    Home Essentials
                  </div>
                </div>

                <div className="rounded-[1.5rem] bg-slate-50 p-5">
                  <div className="text-sm text-slate-500">
                    Shop Smart
                  </div>

                  <div className="mt-2 text-xl font-bold">
                    Best Deals
                  </div>

                  <div className="mt-3 flex items-center gap-2 text-sm">
                    <BadgePercent className="h-4 w-4" />
                    Special offers
                  </div>
                </div>

              </div>

            </div>
          </div>

        </div>
      </section>


      {/* CATEGORIES */}
      <section id="collections" className="mx-auto max-w-7xl px-4 py-10 lg:px-8">

        <div className="rounded-[2rem] border bg-white p-6 shadow-sm">

          <h2 className="text-2xl font-black">
            Shop by Collection
          </h2>

          <p className="mt-2 text-slate-600">
            Explore our most popular categories.
          </p>

          <div className="mt-6 flex flex-wrap gap-3">

            {categories.map((category) => (
              <button
                key={category}
                className="rounded-full border bg-slate-50 px-5 py-3 text-sm font-medium hover:bg-slate-100"
              >
                {category}
              </button>
            ))}

          </div>
        </div>
      </section>


      {/* PRODUCTS */}
      <section id="shop" className="mx-auto max-w-7xl px-4 py-16 lg:px-8">

        <div>
          <div className="text-sm font-semibold uppercase tracking-[0.25em] text-slate-500">
            Featured Products
          </div>

          <h2 className="mt-2 text-3xl font-black">
            Trending products
          </h2>
        </div>


        <div className="mt-8 grid gap-6 md:grid-cols-2 xl:grid-cols-4">

          {products.map((product) => (

            <article
              key={product.name}
              className="group overflow-hidden rounded-[1.75rem] border bg-white shadow-sm transition hover:-translate-y-1 hover:shadow-xl"
            >

              <div className="relative aspect-square bg-slate-100 p-6">

                <div className="flex h-full items-center justify-center rounded-[1.5rem] border border-dashed border-slate-300 bg-white">

                  <div className="text-center">

                    <div className="mx-auto flex h-20 w-20 items-center justify-center rounded-3xl bg-slate-900 text-white">
                      <ShoppingBag className="h-8 w-8" />
                    </div>

                    <div className="mt-4 text-sm text-slate-500">
                      Product Image
                    </div>

                  </div>
                </div>

                <div className="absolute left-4 top-4 rounded-full bg-slate-900 px-3 py-1 text-xs font-semibold text-white">
                  {product.tag}
                </div>

                <button className="absolute right-4 top-4 rounded-full bg-white p-2 shadow">
                  <Heart className="h-4 w-4" />
                </button>

              </div>


              <div className="p-5">

                <h3 className="text-lg font-bold">
                  {product.name}
                </h3>

                <div className="mt-2 flex items-center gap-1">

                  {[1, 2, 3, 4, 5].map((star) => (
                    <Star
                      key={star}
                      className="h-4 w-4 fill-slate-900"
                    />
                  ))}

                  <span className="ml-2 text-sm text-slate-500">
                    128 reviews
                  </span>

                </div>


                <div className="mt-4 flex items-center gap-3">

                  <div className="text-2xl font-black">
                    {product.price}
                  </div>

                  <div className="text-sm font-semibold text-slate-400 line-through">
                    {product.oldPrice}
                  </div>

                </div>


                <button className="mt-5 flex w-full items-center justify-center gap-2 rounded-full bg-slate-900 px-5 py-3 text-sm font-semibold text-white hover:bg-slate-800">

                  Add to Cart

                  <ArrowRight className="h-4 w-4" />

                </button>

              </div>

            </article>

          ))}

        </div>
      </section>


      {/* TRUST FEATURES */}
      <section className="mx-auto max-w-7xl px-4 py-8 lg:px-8">

        <div className="grid gap-6 md:grid-cols-2 xl:grid-cols-4">

          {features.map(({ icon: Icon, title, text }) => (

            <div
              key={title}
              className="rounded-[1.75rem] border bg-white p-6 shadow-sm"
            >

              <div className="flex h-12 w-12 items-center justify-center rounded-2xl bg-slate-900 text-white">
                <Icon className="h-5 w-5" />
              </div>

              <h3 className="mt-4 text-lg font-bold">
                {title}
              </h3>

              <p className="mt-2 text-sm leading-6 text-slate-600">
                {text}
              </p>

            </div>

          ))}

        </div>
      </section>


      {/* ABOUT */}
      <section id="about" className="mx-auto max-w-7xl px-4 py-16 lg:px-8">

        <div className="grid gap-8 rounded-[2rem] border bg-white p-8 shadow-sm lg:grid-cols-2 lg:p-12">

          <div>

            <div className="text-sm font-semibold uppercase tracking-[0.25em] text-slate-500">
              About Nolexcart
            </div>

            <h2 className="mt-2 text-3xl font-black">
              Ecommerce made simple.
            </h2>

          </div>

          <div className="space-y-4 leading-7 text-slate-600">

            <p>
              Nolexcart is a modern ecommerce and dropshipping brand focused
              on bringing useful, trending and affordable products to
              customers.
            </p>

            <p>
              We focus on a clean shopping experience, transparent product
              information and reliable customer service.
            </p>

            <p>
              From everyday essentials to smart gadgets, Nolexcart makes
              online shopping simple and convenient.
            </p>

          </div>

        </div>
      </section>


      {/* REVIEWS */}
      <section id="reviews" className="mx-auto max-w-7xl px-4 py-8 lg:px-8">

        <div className="text-sm font-semibold uppercase tracking-[0.25em] text-slate-500">
          Customer Reviews
        </div>

        <h2 className="mt-2 text-3xl font-black">
          What our customers say
        </h2>


        <div className="mt-8 grid gap-6 lg:grid-cols-3">

          {testimonials.map((review) => (

            <div
              key={review.name}
              className="rounded-[1.75rem] border bg-white p-6 shadow-sm"
            >

              <div className="flex gap-1">

                {[1, 2, 3, 4, 5].map((star) => (
                  <Star
                    key={star}
                    className="h-4 w-4 fill-slate-900"
                  />
                ))}

              </div>

              <p className="mt-4 leading-7 text-slate-600">
                “{review.text}”
              </p>

              <div className="mt-6 font-bold">
                {review.name}
              </div>

              <div className="text-sm text-slate-500">
                Verified Buyer
              </div>

            </div>

          ))}

        </div>
      </section>


      {/* CTA */}
      <section className="mx-auto max-w-7xl px-4 py-16 lg:px-8">

        <div className="grid gap-8 rounded-[2rem] bg-slate-900 p-8 text-white lg:grid-cols-2 lg:p-12">

          <div>

            <div className="text-sm font-semibold uppercase tracking-[0.25em] text-slate-300">
              Nolexcart
            </div>

            <h2 className="mt-3 text-3xl font-black">
              Ready to discover your next favourite product?
            </h2>

            <p className="mt-4 text-slate-300">
              Explore our latest products and special offers today.
            </p>

          </div>

          <div className="flex items-center lg:justify-end">

            <button className="inline-flex items-center gap-2 rounded-full bg-white px-7 py-4 font-semibold text-slate-900">
              Shop Now
              <ArrowRight className="h-4 w-4" />
            </button>

          </div>

        </div>

      </section>


      {/* FAQ */}
      <section id="faq" className="mx-auto max-w-5xl px-4 py-8 lg:px-8">

        <div className="text-center">

          <div className="text-sm font-semibold uppercase tracking-[0.25em] text-slate-500">
            FAQ
          </div>

          <h2 className="mt-2 text-3xl font-black">
            Frequently Asked Questions
          </h2>

        </div>


        <div className="mt-8 space-y-4">

          {[
            [
              "What does Nolexcart sell?",
              "Nolexcart offers trending products across home, kitchen, gadgets, lifestyle, beauty, fitness and accessories.",
            ],
            [
              "Is payment secure?",
              "Yes. Our checkout is designed to provide customers with a safe and convenient payment experience.",
            ],
            [
              "Do you offer returns?",
              "Yes. Customers can follow the return and refund policy provided on the store.",
            ],
            [
              "How can I track my order?",
              "Once your order is shipped, tracking information can be provided through your order confirmation and shipping updates.",
            ],
          ].map(([question, answer]) => (

            <details
              key={question}
              className="group rounded-[1.5rem] border bg-white p-5 shadow-sm"
            >

              <summary className="flex cursor-pointer list-none items-center justify-between font-semibold">

                {question}

                <span className="text-xl transition group-open:rotate-45">
                  +
                </span>

              </summary>

              <p className="mt-4 leading-7 text-slate-600">
                {answer}
              </p>

            </details>

          ))}

        </div>
      </section>


      {/* NEWSLETTER */}
      <section className="mx-auto max-w-7xl px-4 py-16 lg:px-8">

        <div className="rounded-[2rem] border bg-white p-8 shadow-sm lg:p-12">

          <div className="grid gap-8 lg:grid-cols-2 lg:items-center">

            <div>

              <div className="text-sm font-semibold uppercase tracking-[0.25em] text-slate-500">
                Stay Connected
              </div>

              <h2 className="mt-2 text-3xl font-black">
                Get exclusive deals & new product alerts.
              </h2>

              <p className="mt-4 text-slate-600">
                Subscribe to receive special offers and product updates.
              </p>

            </div>


            <div className="flex gap-2">

              <input
                type="email"
                placeholder="Enter your email"
                className="w-full rounded-full border bg-slate-50 px-5 py-3 outline-none focus:border-slate-500"
              />

              <button className="rounded-full bg-slate-900 px-6 py-3 font-semibold text-white">
                Subscribe
              </button>

            </div>

          </div>

        </div>

      </section>


      {/* FOOTER */}
      <footer className="border-t bg-white">

        <div className="mx-auto grid max-w-7xl gap-8 px-4 py-12 lg:grid-cols-4 lg:px-8">

          <div>

            <div className="flex items-center gap-3">

              <div className="flex h-10 w-10 items-center justify-center rounded-2xl bg-slate-900 text-white">
                <ShoppingBag className="h-5 w-5" />
              </div>

              <div className="text-xl font-bold">
                Nolexcart
              </div>

            </div>

            <p className="mt-4 text-sm leading-6 text-slate-600">
              A modern ecommerce and dropshipping store bringing useful,
              trending and affordable products to customers.
            </p>

          </div>


          <div>

            <h3 className="font-bold">
              Shop
            </h3>

            <ul className="mt-4 space-y-3 text-sm text-slate-600">
              <li>All Products</li>
              <li>Best Sellers</li>
              <li>New Arrivals</li>
              <li>Special Offers</li>
            </ul>

          </div>


          <div>

            <h3 className="font-bold">
              Customer Care
            </h3>

            <ul className="mt-4 space-y-3 text-sm text-slate-600">
              <li>Contact Us</li>
              <li>Shipping Policy</li>
              <li>Return & Refund</li>
              <li>Privacy Policy</li>
            </ul>

          </div>


          <div>

            <h3 className="font-bold">
              Follow Us
            </h3>

            <div className="mt-4 flex gap-3">

              <button className="rounded-full border p-3">
                <Instagram className="h-4 w-4" />
              </button>

              <button className="rounded-full border p-3">
                <Facebook className="h-4 w-4" />
              </button>

              <button className="rounded-full border p-3">
                <Youtube className="h-4 w-4" />
              </button>

            </div>

          </div>

        </div>


        <div className="border-t py-5 text-center text-sm text-slate-500">
          © 2026 Nolexcart. All rights reserved.
        </div>

      </footer>

    </div>
  );
}

export default App;
