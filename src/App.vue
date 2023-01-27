<script setup >
import { ref } from "vue";

const stuName = ref("");
const stuLname = ref("");
const stuID = ref("");

</script>

<template>
  <h1>แบบฟอร์ม คำร้องขอโอนย้ายสาขขาวิชาต่างคณะ</h1>
  <br />
  <div>สำหรับหลักสูตร 4 ปี และ หลักสูตร 4 ปีเทียบเข้าเรียน(2ปี)</div>

  <form class="" action="index.html" method="post">
    <div>
      <div>
        วันที่
        <input type="date" required />
        คณะใหม่
        <select name="">
          <option value="">===กรุณาเลือกคณะ===</option>
          <option value="">วิทยาศาสตร์</option>
          <option value="">บริหาร</option>
          <option value="">ท่องเที่ยว</option>
          <option value="">ศิลปศาสตร์</option>
        </select>
      </div>

      <div>
        ชื่อ
        <input
          type="text"
          name="array[]"
          v-model="stuName"
          maxlength="20"
          required >

        นามสกุล
        <input
          type="text"
          name="array[]"
          v-model="stuLname"
          maxlength="20"
          required >
      </div>

      <div>
        รหัสนศ.
        <input type="text" v-model="stuID" name="array[]" required />
        หมายเลขโทรศัพท์
        <input type="text" required />
      </div>

      <div>
        หลักสูตร
        <select>
          <option value="">===กรุณาเลือกหลักสูตร===</option>
          <option value="">หลักสูตร4-5ปี</option>
          <option value="">หลักสูตร4ปีเทียบเข้าเรียน(2ปี)</option>
        </select>
      </div>

      <div>
        สาขาวิชา
        <input type="text" required />
        คณะ
        <input type="text" required />
      </div>

      <div>
        มีความประสงค์ที่จะขอโอนย้ายไปสาขาวิชา
        <input type="text" required />
        เนื่องจาก
        <input type="text" required />
      </div>
      <br />

      <button type="button" name="button" onclick="">Submit</button>
    </div>
  </form>
  <br />

  <p id="par"></p>
 
  {{ stuID }} {{ stuName }} {{ stuLname }}
</template>
