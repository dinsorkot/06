<script setup>
import Form from './form.vue';
import { ref } from 'vue';

const previewSrc = ref('')

function showPreview(event) {
    if (event.target.files.length > 0) {
        var src = URL.createObjectURL(event.target.files[0])
        previewSrc.value = src
    }
}

function resetPage() {
      location.reload();
    }

var rq_stu = ref(
    {
        rq_date: '',
        th_name: '',
        stu_ID: '',
        eg_name: '',
        card_ID: '',
        br_ch: '',
        fac_ch: '',
        ph:'',
        nonATM:'',
        ATM:'',
        picrture: previewSrc,
        lostC:'',
        cantC:'',
        newC:'',
        brokeC:'',
        nameC:'',
        endC:'',
        moveBC:'',
        firstUC:'',
        endUC:'',
        signIn:''
    }
)
console.log(rq_stu);
</script>
<template>
    <Form style="width: 70%;">
        <template #logo>
            <img src="../assets/img/MJU_LOGO.svg.png" alt="logo" style="height: 100px;">
        </template>
        <template #topic>
            แบบฟอร์มขอทำบัตรประจำตัวนักศึกษา
        </template>
        <template #code>
            มจท.03
        </template>
        <template #date>
            เขียนที่&nbsp;&nbsp;&nbsp;&nbsp;มหาวิทยาลัยแม่โจ้
        </template>
        <template #input_date>
            <input type="date" v-model="rq_stu.rq_date" required
                style="width: 185px; text-align:center; font-size: 14px;">
        </template>

        <template #fl_name_th>
            &nbsp;&nbsp;&nbsp;&nbsp;
            &nbsp;&nbsp;&nbsp;&nbsp;
            ข้าพเจ้า ชื่อภาษาไทย
            &nbsp;&nbsp;
            <input v-model="rq_stu.th_name" required style="width: 17rem;">
        </template>
        <template #stu_id>
            &nbsp;&nbsp;&nbsp;&nbsp;
            รหัสนักศึกษา (student ID)
            &nbsp;
            <input type="number" v-model="rq_stu.stu_ID" required style="width: 15.2rem;">
        </template>

        <template #fl_name_eg>
            ชื่อภาษาอังกฤษ (ตัวพิมใหญ่)
            <input type="text" v-model="rq_stu.eg_name" required style="width: 15rem;">
        </template>
        <template #card_id>
            &nbsp;&nbsp;&nbsp;&nbsp;
            เลขประจำตัวประชาชน
            &nbsp;
            <input type="number" v-model="rq_stu.card_ID" required style="width: 18.4rem;">
        </template>

        <template #branch>
            <label>
                สาขาวิชา
            </label>
            &nbsp;
            <select v-model="rq_stu.br_ch" style="width: 22.5rem; height:30px;">
                <option value="เกษตรศาสตร์">เกษตรศาสตร์</option>
                <option value="พืชสวน">พืชสวน</option>
                <option value="เทคโนโลยีอาหาร">เทคโนโลยีอาหาร</option>
                <option value="เทคโนโลยีอุสาหการ การผลิต">เทคโนโลยีอุสาหการ การผลิต</option>
                <option value="เทคโนโลยีพอลิเมอร์">เทคโนโลยีพอลิเมอร์</option>
                <option value="วิศวกรรมเกษตร">วิศวกรรมเกษตร</option>
                <option value="วิศวกรรมอาหาร">วิศวกรรมอาหาร</option>
                <option value="คณิตศาสตร์">คณิตศาสตร์</option>
                <option value="เคมี">เคมี</option>
                <option value="เทคโนโลยีชีวภาพ">เทคโนโลยีชีวภาพ</option>
                <option value="ฟิสิกส์">ฟิสิกส์</option>
                <option value="วัสดุศาสตรฺ">วัสดุศาสตรฺ</option>
                <option value="สถิติ">สถิติ</option>
                <option value="เทคโนโลยีสารสนเทศ">เทคโนโลยีสารสนเทศ</option>
                <option value="วิทยาการคอมพิวเตอร์">วิทยาการคอมพิวเตอร์</option>
                <option value="รัฐประศาสนศาสตร์">รัฐประศาสนศาสตร์</option>
                <option value="รัฐศาสตร์">รัฐศาสตร์</option>
                <option value="การเงิน">การเงิน</option>
                <option value="การจัดการ">การจัดการ</option>
                <option value="การบัญชี">การบัญชี</option>
                <option value="การตลาด">การตลาด</option>
                <option value="ระบบสารสนเทศ">ระบบสารสนเทศ</option>
                <option value="การท่องเที่ยวและการโรงแรม">การท่องเที่ยวและการโรงแรม</option>
                <option value="ประมง">ประมง</option>
                <option value="เศรษฐศาสตร์">เศรษฐศาสตร์</option>
                <option value="นิเทศศาสตร์">นิเทศศาสตร์</option>
                <option value="อังกฤษ">อังกฤษ</option>
                <option value="วิศวกรรมพลังงาน">วิศวกรรมพลังงาน</option>
                <option value="ดิจิทัล">ดิจิทัล</option>
                <option value="ภูมิสถาปัตยกรรม">ภูมิสถาปัตยกรรม</option>
                <option value="วางแผนภาคและเมือง">วางแผนภาคและเมือง</option>
                <option value="สถาปัตยกรรม">สถาปัตยกรรม</option>
                <option value="สัตวศาสตร์">สัตวศาสตร์</option>
                <option value="วนศาสตร์">วนศาสตร์</option>
                <option value="สังคมศาสตร์และพฤติกรรมศาสตร์">
                    สังคมศาสตร์และพฤติกรรมศาสตร์
                </option>
                <option value="การปกครอง">การปกครอง</option>
            </select>
        </template>
        <template #faculty>
            &nbsp;&nbsp;&nbsp;&nbsp;
            <label>
                คณะ
            </label>
            &nbsp;
            <select v-model="rq_stu.fac_ch" style="width: 26.1rem; height:30px;">
                <option value="คณะผลิตกรรมการเกษตร">คณะผลิตกรรมการเกษตร</option>
                <option value="คณะวิศวกรรมและอุตสาหกรรมเกษตร">คณะวิศวกรรมและอุตสาหกรรมเกษตร</option>
                <option value="คณะวิทยาศาสตร์">คณะวิทยาศาสตร์</option>
                <option value="คณะบริหารธุรกิจ">คณะบริหารธุรกิจ</option>
                <option value="คณะพัฒนาการท่องเที่ยว">คณะพัฒนาการท่องเที่ยว</option>
                <option value="คณะเทคโนโลยีการประมงและทรัพยากรทางน้ำ">คณะเทคโนโลยีการประมงและทรัพยากรทางน้ำ</option>
                <option value="คณะเศรษฐศาสตร์">คณะเศรษฐศาสตร์</option>
                <option value="คณะศิลปศาสตร์">คณะศิลปศาสตร์</option>
                <option value="วิทยาลัยพลังงานทดแทน">วิทยาลัยพลังงานทดแทน</option>
                <option value="คณะสารสนเทศและการสื่อสาร">คณะสารสนเทศและการสื่อสาร</option>
                <option value="คณะสถาปัตยกรรมศาสตร์และการออกแบบสิ่งแวดล้อม">คณะสถาปัตยกรรมศาสตร์และการออกแบบสิ่งแวดล้อม
                </option>
                <option value="คณะสัตวศาสตร์และเทคโนโลยี">คณะสัตวศาสตร์และเทคโนโลยี</option>
            </select>
        </template>
        <template #phone>
            เบอร์โทรศัพท์
            &nbsp;
            <input type="text" v-model="rq_stu.ph" style="width: 21rem;">
            &nbsp;
            มีความประสงค์ขอทำบัตรประจำตัวนักศึกษา
        </template>
        <template #ch_b1>
            <div class="container">
                <div class="row ">
                    <div class="form-check col-6 d-flex justify-content-center align-items-center"
                        style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1" v-model="rq_stu.nonATM"
                            style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            บัตรรูปแบบของมหาวิทยาลัย (ไม่ใช่ ATM)
                        </label>
                    </div>
                    <div class="col-6 d-flex align-items-center">
                        <label class="form-check-label" for="defaultCheck1">
                            ระยะเวลาการดำเนินการไม่เกิน 1 สัปดาห์
                        </label>
                    </div>
                </div>
            </div>
            <div class="container">
                <div class="row ">
                    <div class="form-check col-6 d-flex justify-content-center align-items-center"
                        style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1" v-model="rq_stu.ATM"
                            style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            บัตรรูปแบบของมหาธนาคาร(A.T.M)
                            &nbsp;&nbsp;&nbsp;&nbsp;
                            &nbsp;&nbsp;&nbsp;&nbsp;
                        </label>
                    </div>
                    <div class="col-6 d-flex align-items-center">
                        <label class="form-check-label" for="defaultCheck1">
                            ระยะเวลาการดำเนินการไม่เกิน 1 เดือน
                        </label>
                    </div>
                </div>
            </div>
        </template>
        <template #ch_b2>
            โดยมีเหตุผลดังนี้
            <div class="container">
                <div class="row ">
                    <div class="form-check col-6 d-flex justify-content-center align-items-center"
                        style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1" v-model="rq_stu.lostC"
                            style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            บัตรเดิมสูยหาย
                        </label>
                    </div>
                    <div class="form-check col-6 d-flex justify-content-start align-items-center" style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1" v-model="rq_stu.cantC"
                            style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            บัตรถูกอายัติ
                        </label>
                    </div>
                </div>
                <div class="row">
                    <div class="form-check col d-flex justify-content-end align-items-center" style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1" v-model="rq_stu.newC"
                            style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            กรณีที่นักศึกษามารายงานตัวเข้าเป็นนักศึกษาใหม่หลังกำหนด
                        </label>
                    </div>
                </div>
                <div class="row d-flex justify-content-center">
                    ในกรณีต่อไปนี้นักศึกาาต้องแนบบัตรประจำตัวนักศึกษาเดิม
                </div>
                <div class="row">
                    <div class="form-check col d-flex justify-content-center align-items-center" style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1" v-model="rq_stu.brokeC"
                            style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            บัตรชำรุด
                            &emsp;&emsp;
                        </label>
                    </div>
                    <div class="form-check col d-flex justify-content-start align-items-center" style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1" v-model="rq_stu.nameC"
                            style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            เปลี่ยนชื่อ - นามสกุล
                        </label>
                    </div>
                </div>
                <div class="row">
                    <div class="form-check col d-flex justify-content-center align-items-center" style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1"
                        v-model="rq_stu.endC"    style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            บัตรหมดอายุ
                            &emsp;
                        </label>
                    </div>
                    <div class="form-check col d-flex justify-content-start align-items-center" style="height: 40px;">
                        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1"
                        v-model="rq_stu.moveBC"    style="height: 30px; width:30px;">
                        <label class="form-check-label" for="defaultCheck1">
                            &nbsp;
                            โอนย้ายสาขา
                        </label>
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        วันออกบัตร
                        &nbsp;
                        <input type="date" name="" id=""  v-model="rq_stu.firstUC"
                            style="width: 130px; text-align:center; font-size: 14px;">
                    </div>
                    <div class="col">
                        วันหมดอายุ
                        &nbsp;
                        <input type="date" name="" id=""  v-model="rq_stu.endUC"
                            style="width: 130px; text-align:center; font-size: 14px;">
                    </div>
                </div>
            </div>
        </template>
        <template #photo>
            <div class="container ">
                <div class="row d-flex justify-content-center align-items-center">
                    <div class="card d-flex justify-content-center align-items-center"
                        style="height:230px; width:180px;">
                        <img :src="previewSrc" v-if="previewSrc" style="display:block; height:220px; width:168px;" />
                    </div>
                    <label for="formFile" class="form-label mt-2 text-center">(ชุดนักศึกษาหรือ ชุดสูทเท่านั้น)</label>
                    <input class="form-control" type="file" @change="showPreview" />

                </div>
            </div>
        </template>
        <template #signin>
            <div class="row d-flex align-items-center">
                <div class="col text-end">ลงชื่อ</div>
                <div class="col-8 d-flex align-items-center">
                    (&nbsp;
                    <input class="form-control" type="text" v-model="signIn"
                        style="width: 300px;" />
                    &nbsp;)

                </div>
            </div>
            <div class="row d-flex align-items-center justify-content-center">
                นักศึกษา
            </div>
        </template>
        <template #modal>
            <div>
                <div class="modal fade" id="exampleModalToggle" aria-hidden="true"
                    aria-labelledby="exampleModalToggleLabel" tabindex="-1">
                    <div class="modal-dialog modal-dialog-centered">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h5 class="modal-title" id="exampleModalToggleLabel">รายการลงชื่อ</h5>
                                <button type="button" class="btn-close" data-bs-dismiss="modal"
                                    aria-label="Close"></button>
                            </div>
                            <div class="modal-body">
                                <div>
                                    <ul>
                                        <li v-for="(value, key) in rq_stu">{{ key }}: {{ value }}</li>
                                    </ul>
                                </div>
                            </div>
                            <div class="modal-footer">
                                <button class="btn btn-primary" data-bs-target="#exampleModalToggle2" data-bs-toggle="modal" data-bs-dismiss="modal" @click="resetPage">ยืนยัน</button>
                              </div>
                        </div>
                    </div>
                </div>
                <div class="d-flex justify-content-center">
                    <a class="btn btn-primary" data-bs-toggle="modal" href="#exampleModalToggle" role="button"
                    >บันทึก</a>
                </div>

            </div>
        </template>
    </Form>
</template>

<style scoped>

</style>