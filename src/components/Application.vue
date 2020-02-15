<template>
  <div>
    <div class="container">
      <div>
        <div class="article-content">
          <p style="text-align:center;line-height:2.9em;">
            <strong><span style="font-family:方正大标宋简体;font-size:1.2rem;">在外人员返汉申请表</span></strong>
          </p>
          <div class="form">
            <div class="form-row">
              <div class="form-label">姓名</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.name" placeholder="填写您的姓名(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">性别
                <input id="sex1" class="form-radio" type="radio" value="男" v-model="formData.sex">
                <span for="sex1" class="form-radio-label">男</span>
                <input id="sex2" class="form-radio" type="radio" value="女" v-model="formData.sex">
                <span for="sex2" class="form-radio-label">女</span>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">身份证号</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.card_id" placeholder="填写您的身份证号(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">拟返回地（居住地址）</div>
              <div class="form-group">
                <flexbox>
                  <flexbox-item>
                    <input type="text" class="form-input" v-model="formData.back_address_zone" placeholder="区(必填)">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="text" class="form-input" v-model="formData.back_address_street" placeholder="街道或乡镇(必填)">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="text" class="form-input" v-model="formData.back_address_community" placeholder="社区或村(必填)">
                  </flexbox-item>
                </flexbox>
                <div class="form-group-padding">
                  <input type="text" class="form-input" v-model="formData.back_address_detail" placeholder="详细地址(必填)">
                </div>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">目前所在地</div>
              <div class="form-group">
                <flexbox>
                  <flexbox-item>
                    <input type="text" class="form-input" v-model="formData.location_province" placeholder="省(必填)">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="text" class="form-input" v-model="formData.location_city" placeholder="市(必填)">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="text" class="form-input" v-model="formData.location_zone" placeholder="县或市区(必填)">
                  </flexbox-item>
                </flexbox>
                <flexbox class="form-group-padding">
                  <flexbox-item>
                    <input type="text" class="form-input" v-model="formData.location_street" placeholder="街或乡镇">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="text" class="form-input" v-model="formData.location_community" placeholder="社区或村">
                  </flexbox-item>
                </flexbox>
                <div class="form-group-padding">
                  <input type="text" class="form-input" v-model="formData.location_detail" placeholder="详细地址(必填)">
                </div>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">工作单位及职务</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.workplace" placeholder="填写您的工作单位及职务(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">联系手机</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.mobile" placeholder="填写您的联系手机(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">紧急联系人手机</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.emergency_contact_mobile" placeholder="填写您的紧急联系人手机(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">申请返回理由</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.back_reason" placeholder="填写您的申请返回理由(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">离开武汉时间</div>
              <div class="form-group">
                <flexbox>
                  <flexbox-item>
                    <input type="number" class="form-input" v-model="formData.leave_time_year" placeholder="年(必填)">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="number" class="form-input" v-model="formData.leave_time_month" placeholder="月(必填)">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="number" class="form-input" v-model="formData.leave_time_day" placeholder="日(必填)">
                  </flexbox-item>
                </flexbox>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">拟返汉时间</div>
              <div class="form-group">
                <flexbox>
                  <flexbox-item>
                    <input type="number" class="form-input" v-model="formData.back_time_year" placeholder="年(必填)">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="number" class="form-input" v-model="formData.back_time_month" placeholder="月(必填)">
                  </flexbox-item>
                  <flexbox-item>
                    <input type="number" class="form-input" v-model="formData.back_time_day" placeholder="日(必填)">
                  </flexbox-item>
                </flexbox>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">身体状况</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.physical_physical" placeholder="填写您的身体状况(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">体温</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.temperature" placeholder="填写您的体温(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">是否干咳
                <input id="is_cough1" class="form-radio" type="radio" value="是" v-model="formData.is_cough">
                <span for="is_cough1" class="form-radio-label">是</span>
                <input id="is_cough2" class="form-radio" type="radio" value="否" v-model="formData.is_cough">
                <span for="is_cough2" class="form-radio-label">否</span>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">是否气喘
                <input id="is_asthma1" class="form-radio" type="radio" value="是" v-model="formData.is_asthma">
                <span for="is_asthma1" class="form-radio-label">是</span>
                <input id="is_asthma2" class="form-radio" type="radio" value="否" v-model="formData.is_asthma">
                <span for="is_asthma2" class="form-radio-label">否</span>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">是否亲密接触感染者
                <input id="is_contact_with_infected_person1" class="form-radio" type="radio" value="是" v-model="formData.is_contact_with_infected_person">
                <span for="is_contact_with_infected_person1" class="form-radio-label">是</span>
                <input id="is_contact_with_infected_person2" class="form-radio" type="radio" value="否" v-model="formData.is_contact_with_infected_person">
                <span for="is_contact_with_infected_person2" class="form-radio-label">否</span>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">是否进行隔离
                <input id="is_quarantine1" class="form-radio" type="radio" value="是" v-model="formData.is_quarantine">
                <span for="is_quarantine1" class="form-radio-label">是</span>
                <input id="is_quarantine2" class="form-radio" type="radio" value="否" v-model="formData.is_quarantine">
                <span for="is_quarantine2" class="form-radio-label">否</span>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">隔离天数</div>
              <div class="form-group">
                <input type="number" class="form-input" v-model="formData.quarantine_days" placeholder="填写您的隔离天数">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">拟返程方式</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.back_type" placeholder="填写您的返程方式(必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">同行人员</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.together_person" placeholder="填写您的同行人员(多个用逗号隔开,非必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">航班、车次信息</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.back_type_message" placeholder="填写您的航班、车次信息(非必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">自驾（乘坐）私家车车牌号</div>
              <div class="form-group">
                <input type="text" class="form-input" v-model="formData.car_number" placeholder="填写您的自驾（乘坐）私家车车牌号(非必填)">
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">拟返程路线</div>
              <div class="form-group">
                <textarea type="text" class="form-input form-textarea" v-model="formData.back_route" placeholder="填写您的拟返程路线(非必填)"></textarea>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">进入武汉边界地点，到达车站、机场</div>
              <div class="form-group">
                <textarea type="text" class="form-input form-textarea" v-model="formData.arrive_place" placeholder="填写您的进入武汉边界地点，到达车站、机场(非必填)"></textarea>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">备注</div>
              <div class="form-group">
                <textarea type="text" class="form-input form-textarea" v-model="formData.remark" placeholder="填写您的备注(非必填)"></textarea>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">申请人所在地防疫指挥部出具的健康证明</div>
              <div class="form-group">
                <div class="file-container" v-if="formData.file">
                  <a target="_blank" class="file-name" :href="fileurl">{{ filename }}</a>
                  <span class="file-delete" @click="fileDelete">删除</span>
                </div>
                <div class="upload-container" v-else>
                  <x-button mini plain type="primary" @click.native.stop="openFile">上传</x-button>
                  <input type="file" @change="fileChanged" style="display: none" ref="fileInput">
                </div>
              </div>
            </div>
            <div class="form-row">
              <div class="form-label">注：以家庭为单位的返汉人员，按一人一表填报，除了个人化信息外，其他内容可与户主一致。</div>
            </div>
            <div class="form-row botton-box">
              <x-button type="primary" @click.native.stop="submit">提交申请</x-button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import OSS from 'ali-oss'
  import Dayjs from 'dayjs'
  import { XHeader, Flexbox, FlexboxItem, XButton } from 'vux'
  export default {
    components: { XHeader, Flexbox, FlexboxItem, XButton },
    data() {
      return {
        fileurl: '',
        filename: '',
        formData: {
          name: '',
          sex: '',
          card_id: '',
          back_address_zone: '',
          back_address_street: '',
          back_address_community: '',
          back_address_detail: '',
          location_province: '',
          location_city: '',
          location_zone: '',
          location_street: '',
          location_community: '',
          location_detail: '',
          workplace: '',
          mobile: '',
          emergency_contact_mobile: '',
          back_reason: '',
          leave_time_year: '',
          leave_time_month: '',
          leave_time_day: '',
          back_time_year: '',
          back_time_month: '',
          back_time_day: '',
          physical_physical: '',
          temperature: '',
          is_cough: '',
          is_asthma: '',
          is_contact_with_infected_person: '',
          is_quarantine: '',
          quarantine_days: '',
          back_type: '',
          together_person: '',
          back_type_message: '',
          car_number: '',
          back_route: '',
          arrive_place: '',
          remark: '',
          file: ''
        }
      }
    },
    methods: {
      submit() {
        if (this.formData.name == '') {
            this.$vux.toast.text("请填写姓名");
            return false;
        }
        if (this.formData.sex == '') {
            this.$vux.toast.text("请选择性别");
            return false;
        }
        if (this.formData.card_id.length != 18) {
            this.$vux.toast.text("请填写正确的18位身份证号");
            return false;
        }
        if (this.formData.back_address_zone == '') {
            this.$vux.toast.text("请填写拟返回地区");
            return false;
        }
        if (this.formData.back_address_street == '') {
            this.$vux.toast.text("请填写拟返回地街道或乡镇");
            return false;
        }
        if (this.formData.back_address_community == '') {
            this.$vux.toast.text("请填写拟返回地社区或村");
            return false;
        }
        if (this.formData.back_address_detail == '') {
            this.$vux.toast.text("请填写拟返回地详细地址");
            return false;
        }
        if (this.formData.back_type == '') {
            this.$vux.toast.text("填写您的返程方式");
            return false;
        }
        if (this.formData.location_province == '') {
            this.$vux.toast.text("请填写目前所在地省");
            return false;
        }
        if (this.formData.location_city == '') {
            this.$vux.toast.text("请填写目前所在地市");
            return false;
        }
        if (this.formData.location_zone == '') {
            this.$vux.toast.text("请填写目前所在地区");
            return false;
        }
        if (this.formData.location_detail == '') {
            this.$vux.toast.text("请填写目前所在地详细地址");
            return false;
        }
        if (this.formData.workplace == '') {
            this.$vux.toast.text("请填写工作单位及职务");
            return false;
        }
        if (this.formData.mobile.length != 11) {
            this.$vux.toast.text("请填写正确的11位联系手机号");
            return false;
        }
        if (this.formData.emergency_contact_mobile.length != 11) {
            this.$vux.toast.text("请填写正确的11位紧急联系人手机号");
            return false;
        }
        if (this.formData.back_reason == '') {
            this.$vux.toast.text("请填写申请返回理由");
            return false;
        }
        if (this.formData.leave_time_year == '' || this.formData.leave_time_month == '' || this.formData.leave_time_day == '') {
            this.$vux.toast.text("请填写完整离开武汉时间");
            return false;
        }
        if (this.formData.back_time_year == '' || this.formData.back_time_month == '' || this.formData.back_time_day == '') {
            this.$vux.toast.text("请填写完整拟返汉时间");
            return false;
        }
        if (this.formData.physical_physical == '') {
            this.$vux.toast.text("请填写身体状况");
            return false;
        }
        if (this.formData.temperature == '') {
          this.$vux.toast.text("请填写体温");
          return false;
        }
        if (this.formData.is_cough == '') {
            this.$vux.toast.text("请选择是否干咳");
            return false;
        }
        if (this.formData.is_asthma == '') {
            this.$vux.toast.text("请选择是否气喘");
            return false;
        }
        if (this.formData.is_contact_with_infected_person == '') {
            this.$vux.toast.text("请选择亲密接触感染者");
            return false;
        }
        if (this.formData.is_quarantine == '') {
            this.$vux.toast.text("请选择进行隔离");
            return false;
        }
        if (this.formData.is_quarantine == '是' && !this.formData.quarantine_days){
            this.$vux.toast.text("请填写您的隔离天数");
            return false;
        }
        if (this.formData.file == '') {
          this.$vux.toast.text("请上传所在地防疫指挥部出具的健康证明");
          return false;
        }
        
        console.log(this.formData)
      },
      openFile() {
          this.$refs.fileInput.click();
      },
      fileDelete() {
        this.fileurl = ''
        this.filename = ''
        this.formData.file = ''
      },
      async fileChanged(event) {
        const accessKeyId = 'LTAI4Fk54tvnWbu6WDsAqFRo'
        const accessKeySecret = '7IL83GqXco6z5QvV3QwJSQ5HSrisWS'

        let client = new OSS({
          region: 'oss-cn-hangzhou',
          accessKeyId: accessKeyId,
          accessKeySecret: accessKeySecret,
          bucket: 'back-wuhan-upload'
        });
        const file = event.target.files[0]
        const date = Dayjs().format('yyyy-MM-dd')

        const filename = 'application/' + date + '/' + new Date().getTime() + '.' + file.name.split('.').pop();

        await client.multipartUpload(filename, file, {
          progress: async function (p) {
            console.log(p)
          }
        }).then(({res}) => {
          if (res.statusCode === 200) {
              this.fileurl = 'https://back-wuhan-upload.oss-cn-hangzhou.aliyuncs.com/' + filename
              this.filename = file.name
              this.formData.file = filename
          } else {
            this.$vux.toast.text("上传失败");
          }
        }).catch(error => {
          this.$vux.toast.text("上传失败，请重试");
        });

      }
    }
  }
</script>

<style>
  img {
    max-width: 100%;
  }
  .banner img{
    border-radius: 10px;
  }
  .action-bar {
    padding-top: 10px;
    padding-bottom: 10px;
  }
  .container {
    padding: 15px;
  }
  .article-content {
    color: #666;
    font-size: 14px;
  }
  .form-label {
    font-size: 14px;
    color: rgb(66,66,66);
    padding-top: 10px;
  }
  .form-input {
    box-shadow: inset 0 1px 1px rgba(0,0,0,.075);
    height: 36px;
    padding: 6px 8px;
    border: 1px solid #ccc;
    color: #555;
    background-color: #fff;
    font-size: 12px;
    width: 100%;
    border-color: rgb(240, 239, 239);
    box-sizing: border-box;
    transition: none;
  }
  .form-input:focus {
    outline: none;
    box-shadow: inset 0 1px 1px rgba(102,175,233,.3);
    border-color: rgba(102,175,233,.6);
  }
  .form-textarea {
    height: 100px;
    resize: none;
  }
  .form-radio {
    vertical-align: text-bottom;
    margin-bottom: 1px;
  }
  .form-label > .form-radio:first-child {
    margin-left: 20px;
  }
  .form-radio-label {
    padding-right: 10px;
  }
  .form-group-padding {
    padding-top: 7px;
  }
  .botton-box {
    padding-top: 20px;
    padding-bottom: 40px;
  }
  .file-delete {
    text-decoration: underline;
  }
</style>
