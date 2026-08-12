import streamlit as st

# 1. إعدادات الصفحة
st.set_page_config(
    page_title="مولد الإيميلات الاحترافي",
    page_icon="📧",
    layout="centered"
)

# 2. التنسيق والخطوط
st.markdown("""
    <style>
    @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap');
    html, body, [class*="css"]  {
        font-family: 'Cairo', sans-serif;
    }
    .main-title {
        color: #1E88E5;
        text-align: center;
        font-weight: bold;
    }
    </style>
""", unsafe_allow_html=True)

# 3. واجهة الموقع
st.markdown('<h1 class="main-title">📧 مولد الإيميلات المهنية</h1>', unsafe_allow_html=True)
st.write("أهلاً بكِ! احصلي على إيميل احترافي متكامل في ثوانٍ معدودة.")

# 4. خيارات التحديد المتقدمة
col1, col2 = st.columns(2)
with col1:
    email_type = st.selectbox(
        "نوع الإيميل:",
        ("رسمي (Formal)", "ودي (Casual)", "اعتذار (Apology)", "متابعة (Follow-up)")
    )

with col2:
    tone = st.selectbox(
        "اللهجة:",
        ("مهنية (Professional)", "مباشرة (Direct)", "لطيفة (Polite)")
    )

# 5. خانة إدخال الفكرة
user_idea = st.text_area(
    "اكتبي فكرة الإيميل باختصار:",
    placeholder="مثلاً: طلب تأجيل موعد تسليم المشروع إلى يوم الخميس القادم...",
    height=150
)

# 6. زر التوليد والنتيجة
if st.button("✨ توليد الإيميل باحترافية", type="primary", use_container_width=True):
    if not user_idea.strip():
        st.warning("⚠️ برجاء كتابة الفكرة أولاً في الخانة المخصصة.")
    else:
        with st.spinner("جاري صياغة الإيميل بأعلى دقة..."):
            
            if "رسمي" in email_type:
                result_text = f"""الموضوع: بخصوص {user_idea[:35]}...

السيد/المدير المحترم،

تحية طيبة وبعد،

بالإشارة إلى الموضوع أعلاه، أود إفادتكم بأننا نعمل على الأمر باهتمام بالغ، وحسب ما ترونه مناسباً بخصوص: {user_idea}، فإننا نتطلع لتوجيهاتكم الكريمة بشأنه.

شاكراً لكم حسن تعاونكم ودعمكم المستمر،

مع فائق الاحترام والتقدير،
[اسم المرسل]"""

            elif "اعتذار" in email_type:
                result_text = f"""الموضوع: اعتذار بخصوص {user_idea[:35]}...

السيد/العميل العزيز،

تحية طيبة وبعد،

أكتب إليكم لأتقدم بخالص الاعتذار عن أي إزعاج أو تأخير حدث بخصوص: {user_idea}، ونؤكد حرصنا الكامل على تدارك الأمر فوراً وضمان عدم تكراره.

نتشرف دائماً بخدمتكم، ونقدر تفهمكم،

مع أطيب التحيات،
[اسم المرسل]"""

            else:
                result_text = f"""الموضوع: تحديث بخصوص: {user_idea[:35]}...

تحية طيبة،

أود التواصل معكم بخصوص الفكرة أو الطلب المتعلق بـ: "{user_idea}"، ونحن جاهزون لمناقشة كافة التفاصيل والخطوات القادمة في أسرع وقت.

شكراً لتعاونكم المستمر،

مع أطيب التحيات،
[اسم المرسل]"""

            st.success("✅ تم توليد الإيميل بنجاح وبدقة عالية!")
            st.markdown("### النص الجاهز:")
            st.code(result_text, language="markdown")
            st.info("💡 يمكنك الآن نسخ النص مباشرة واستخدامه في أي بريد إلكتروني.")

# تذييل الصفحة
st.markdown("---")
st.caption("تم تطوير هذا النظام لخدمة إعداد الرسائل بدقة واحترافية.")

