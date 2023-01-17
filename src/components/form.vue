<template>
    <div class="container mt-4">
        <div class="row">
            <div class="col">
                <slot name="logo"></slot>
            </div>
            <div class="col-7 d-flex justify-content-center align-items-center">
                <slot name="topic"></slot>
            </div>
            <div class="col d-flex justify-content-center ">
                <h6>
                    <slot name="code"></slot>
                </h6>
            </div>
        </div>
        <div class="d-flex justify-content-end mt-4">
            <div>
                <div class="">
                    <slot name="date"></slot>
                </div>
                <div class="">
                    <slot name="input_date"></slot>
                </div>
            </div>
        </div>
        <div class="d-flex mt-5">
            <div>
                <slot name="fl_name_th"></slot>
            </div>
            <div>
                <slot name="stu_id"></slot>
            </div>
        </div>
        <div class="d-flex mt-2">
            <div>
                <slot name="fl_name_eg"></slot>
            </div>
            <div>
                <slot name="card_id"></slot>
            </div>
        </div>
        <div class="d-flex mt-2">
            <div>
                <slot name="branch"></slot>
            </div>
            <div>
                <slot name="faculty"></slot>
            </div>
        </div>
        <div class="mt-2">
            <slot name="phone"></slot>
        </div>
        <div class="mt-3">
            <slot name="ch_b1"></slot>
        </div>
        <div class="mt-3 container">
            <div class="row">
                <div class="col-7">
                    <slot name="ch_b2"></slot>
                </div>
                <div class="col">
                    <slot name="photo"></slot>
                </div>
            </div>
        </div>
        <div class="mt-3">
            <slot name="signin"></slot>
        </div>
        <div class="mt-5 mb-5">
            <div>
            <slot name="modal"></slot>
            </div>
        </div>
        <div class="mb-5">
        </div>
    </div>
</template>
<style scope>

</style>