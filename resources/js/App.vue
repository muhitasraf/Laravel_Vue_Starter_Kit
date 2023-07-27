<template>
    <!-- Main sidebar -->
    <div class="sidebar sidebar-dark sidebar-main sidebar-expand-lg">

        <!-- Sidebar content -->
        <Sidebar></Sidebar>
        <!-- /sidebar content -->

    </div>
    <!-- /main sidebar -->

    <!-- Main content -->
    <div class="content-wrapper">

        <!-- Page header -->
        <Header></Header>
        <!-- /page header -->

        <!-- Inner content -->
        <div class="content-inner">

            <!-- Content area -->
            <div class="content">

                <!-- Basic card -->
                <div class="card">
                    <div class="card-header">
                        <h5 class="mb-0">Basic card</h5>
                    </div>
                    <div class="card-body">
                        <router-view></router-view>
                    </div>
                </div>
                <!-- /basic card -->

            </div>
            <!-- /content area -->

            <!-- Footer -->
            <Footer></Footer>
            <!-- /footer -->

        </div>
        <!-- /inner content -->

    </div>
    <!-- /main content -->
</template>

<script>
    import Footer from './partials/Footer.vue'
    import Sidebar from './partials/Sidebar.vue'
    import Header from './partials/Header.vue'

    export default {
        name: "App",

        components: {
            Footer, Sidebar, Header,
        }
    }
</script>

