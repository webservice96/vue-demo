<script setup>
import {ref} from 'vue';
const activeIndex = ref(0)
const faqs = [
    {
        title: "What are the advantages of your service?",
        text: "1 If you go over your organisations or user limit, a member of the team will reach out about bespoke pricing. In the meantime, our collaborative features won't appear in accounts or users that are over the 100-account or 1,000-user limit.",
    },
    {
        title: "Are there any fees or commissions in addition to the monthly subscription?",
        text: "2 If you go over your organisations or user limit, a member of the team will reach out about bespoke pricing. In the meantime, our collaborative features won't appear in accounts or users that are over the 100-account or 1,000-user limit.",
    },
    {
        title: "You really don't charge per user? Why not?",
        text: "3 If you go over your organisations or user limit, a member of the team will reach out about bespoke pricing. In the meantime, our collaborative features won't appear in accounts or users that are over the 100-account or 1,000-user limit.",
    },
    {
        title: "What happens when I go over my monthly active limit?",
        text: "4 If you go over your organisations or user limit, a member of the team will reach out about bespoke pricing. In the meantime, our collaborative features won't appear in accounts or users that are over the 100-account or 1,000-user limit.",
    },
    {
        title: "Can your service help me understand how to work with my product?",
        text: "5 If you go over your organisations or user limit, a member of the team will reach out about bespoke pricing. In the meantime, our collaborative features won't appear in accounts or users that are over the 100-account or 1,000-user limit.",
    },
    {
        title: "Which third-party application do you integrate with?",
        text: "6 If you go over your organisations or user limit, a member of the team will reach out about bespoke pricing. In the meantime, our collaborative features won't appear in accounts or users that are over the 100-account or 1,000-user limit.",
    },
    {
        title: "I have another question!",
        text: "If you go over your organisations or user limit, a member of the team will reach out about bespoke pricing. In the meantime, our collaborative features won't appear in accounts or users that are over the 100-account or 1,000-user limit.",
    },
]
</script>
 
<template>
    <div>
        <div class="divide-y divide-slate-200">
            <!-- Accordion item -->
            <div class="py-2" v-for="(faq, index) in faqs" :key="index">
                <h2>
                    <button @click="activeIndex=index" id="faqs-title-01" type="button" class="flex items-center justify-between w-full text-left font-semibold py-2">
                        <span class="font-semibold mb-2"> {{ faq.title }}</span>
                        <svg class="fill-indigo-500 shrink-0 ml-8" width="16" height="16" xmlns="http://www.w3.org/2000/svg">
                            <rect y="7" width="16" height="2" rx="1"  class="transform origin-center transition duration-200 ease-out" :class="{'rotate-90':activeIndex!=index}" />
                            <rect y="7" width="16" height="2" rx="1" class="transform origin-center transition duration-200 ease-out" :class="{'rotate-180':activeIndex==index}" />
                        </svg>
                    </button>
                </h2>
                <div id="faqs-text-01" role="region" class="grid text-sm text-slate-600 overflow-hidden transition-all duration-300 ease-in-out">
                    <p class="pb-3" :class="{'hidden':activeIndex!=index}" >
                    <!-- <p class="pb-3" :class="activeIndex!=index?'hidden':''" > -->
                        {{ faq.text }}
                    </p>
                </div>
            </div>

            <!-- repeat -->

        </div>
    </div>
</template>
 
<style scoped></style>