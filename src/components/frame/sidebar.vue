<template>
  <sidebar-menu :menu="menu"/>
</template>
<style scoped>
.v-sidebar-menu{
    height: 93%;
    margin-top: 56px;
}
</style>
 
 <script>
 import AUTH from 'services/auth'
    export default {
        data() {
            return {
                auth: AUTH,
                menu: [
                    {
                        header: true,
                        title: 'Main Navigation',
                        hiddenOnCollapse: true,
                    
                    },
                    {
                        href: '/dashboard',
                        title: 'Dashboard',
                        icon: 'fa user'
                    },
                    {
                        href: '/personalinformation',
                        title: 'Personal Information',
                        icon: 'fa user',
                        child: [
                            {
                                href: '/edit',
                                title: 'Edit Profile'
                            }
                        ]
                    },
                    {
                        href: '/courses',
                        title: 'Add Course & Subjects',
                        icon: 'fa book',
                    },
                    {
                        href: '/confirmLogout',
                        title: 'Log Out',
                        icon: 'fa user',
                    }
                ]
            }
        }
    }
</script> 
   