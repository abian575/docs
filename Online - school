<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="المدرسة الإلكترونية - منصة تعليمية متكاملة تقدم دروسًا تفاعلية لجميع المراحل الدراسية في اليمن.">
    <meta name="keywords" content="التعليم, المدرسة الإلكترونية, مناهج دراسية, دروس, تعليم اليمن, تعليم عن بعد">
    <meta name="author" content="المدرسة الإلكترونية">
    <meta name="robots" content="index, follow">
    <meta property="og:title" content="المدرسة الإلكترونية - أفضل منصة تعليمية في اليمن">
    <meta property="og:description" content="منصة تعليمية متكاملة تقدم دروسًا تفاعلية لجميع المراحل الدراسية.">
    <meta property="og:image" content="https://yourwebsite.com/logo.png">
    <meta property="og:url" content="https://yourwebsite.com">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="المدرسة الإلكترونية">
    <meta name="twitter:description" content="منصة تعليمية متكاملة تقدم دروسًا تفاعلية لجميع المراحل الدراسية.">
    <meta name="twitter:image" content="https://yourwebsite.com/logo.png">
    <link rel="canonical" href="https://yourwebsite.com">
    <link rel="icon" href="https://yourwebsite.com/favicon.ico" type="image/x-icon">
    <title>المدرسة الإلكترونية - المنهج التعليمي لطلاب اليمن</title>
    <script type="application/ld+json">
    {
      "@context": "http://schema.org",
      "@type": "EducationalOrganization",
      "name": "المدرسة الإلكترونية",
      "description": "منصة تعليمية متكاملة تقدم دروسًا تفاعلية لجميع المراحل الدراسية في اليمن.",
      "url": "https://yourwebsite.com",
      "logo": "https://yourwebsite.com/logo.png",
      "sameAs": [
        "https://facebook.com/yourpage",
        "https://twitter.com/yourpage"
      ]
    }
    </script>
    <style>
        :root {
            --primary-color: #007bff;
            --hover-color: #0056b3;
            --background-color: #f5f5f5;
            --success-color: #28a745;
            --error-color: #dc3545;
        }
        body {
            font-family: Arial, sans-serif;
            background-color: var(--background-color);
            text-align: center;
            direction: rtl;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 20px auto;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        .toggle-btn {
            display: block;
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border: none;
            background-color: var(--primary-color);
            color: white;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        .toggle-btn:hover {
            background-color: var(--hover-color);
        }
        .hidden {
            display: none;
        }
        .visible {
            display: block;
        }
        .lesson-container, .question-container {
            margin-top: 10px;
            padding: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background: #f9f9f9;
        }
        .lesson-container h3 {
            margin-top: 0;
        }
        .toast {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: var(--success-color);
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            display: none;
        }
        .toast.error {
            background-color: var(--error-color);
        }
        video, embed {
            width: 100%;
            max-width: 600px;
            height: auto;
            margin-top: 10px;
            border-radius: 5px;
        }
        .file-name {
            margin-top: 10px;
            font-size: 14px;
            color: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>مرحبًا بكم في المدرسة الإلكترونية</h1>
        <!-- المراحل الدراسية -->
        <div class="level">
            <button class="toggle-btn" onclick="toggleSection('primary')">المرحلة الابتدائية ⬇</button>
            <div id="primary" class="grades hidden"></div>
        </div>

        <div class="level">
            <button class="toggle-btn" onclick="toggleSection('middle')">المرحلة الإعدادية ⬇</button>
            <div id="middle" class="grades hidden"></div>
        </div>

        <div class="level">
            <button class="toggle-btn" onclick="toggleSection('highschool')">المرحلة الثانوية ⬇</button>
            <div id="highschool" class="grades hidden"></div>
        </div>
    </div>

    <!-- رسائل Toast -->
    <div id="toast" class="toast"></div>

    <script>
        // وظيفة لإظهار رسائل toast
        function showToast(message, isError = false) {
            const toast = document.getElementById('toast');
            toast.textContent = message;
            toast.className = `toast ${isError ? 'error' : ''}`;
            toast.style.display = 'block';
            setTimeout(() => {
                toast.style.display = 'none';
            }, 3000);
        }

        // وظيفة لإظهار أو إخفاء الأقسام
        function toggleSection(id) {
            const section = document.getElementById(id);
            section.classList.toggle('hidden');
            section.classList.toggle('visible');
        }

        // وظيفة لإنشاء أقسام الصفوف والمواد
        function createGradeSection(levelId, startGrade, endGrade, subjects) {
            const levelDiv = document.getElementById(levelId);
            for (let i = startGrade; i <= endGrade; i++) {
                const gradeDiv = document.createElement('div');
                gradeDiv.innerHTML = `<button class="toggle-btn" onclick="toggleSection('grade${i}')">الصف ${i} ⬇</button>
                                      <div id="grade${i}" class="subjects hidden"></div>`;
                levelDiv.appendChild(gradeDiv);

                const gradeSection = document.getElementById(`grade${i}`);
                subjects.forEach((subject, index) => {
                    const subjectDiv = document.createElement('div');
                    subjectDiv.innerHTML = `<button class="toggle-btn" onclick="toggleSection('subject${i}-${index}')">${subject} ⬇</button>
                                            <div id="subject${i}-${index}" class="subject-details hidden">
                                                <div id="lessons-${subject}-${i}"></div>
                                            </div>`;
                    gradeSection.appendChild(subjectDiv);

                    // إنشاء الدرس الأول تلقائيًا
                    createLesson(subject, i, 1);
                });
            }
        }

        // وظيفة لإنشاء درس جديد
        function createLesson(subject, grade, lessonNumber) {
            const lessonContainer = document.getElementById(`lessons-${subject}-${grade}`);
            const lessonDiv = document.createElement('div');
            lessonDiv.className = 'lesson-container';
            lessonDiv.id = `lesson-${subject}-${grade}-${lessonNumber}`;
            lessonDiv.innerHTML = `
                <h3>${subject} - الصف ${grade} - الدرس ${lessonNumber}</h3>
                <input type="text" placeholder="عنوان الدرس" id="title-${lessonNumber}">
                <textarea placeholder="اكتب شرح الدرس هنا..." id="text-${lessonNumber}"></textarea>
                <button onclick="saveLesson('${subject}', ${grade}, ${lessonNumber})">حفظ</button>
                <button onclick="editLesson('${lessonNumber}')">تعديل</button>
                <button onclick="confirmDeleteLesson('${subject}', ${grade}, ${lessonNumber})">حذف</button>
                <button onclick="copyLesson('${lessonNumber}')">نسخ الشرح</button>
                <input type="file" accept="video/*" id="video-${lessonNumber}" onchange="handleVideoUpload('${subject}', ${grade}, ${lessonNumber})">
                <div id="video-container-${lessonNumber}"></div>
                <input type="file" accept=".pdf" id="pdf-${lessonNumber}" onchange="handlePDFUpload('${subject}', ${grade}, ${lessonNumber})">
                <div id="pdf-container-${lessonNumber}"></div>
                <button onclick="addQuestion('${lessonNumber}')">إضافة سؤال</button>
                <div id="questions-${lessonNumber}"></div>
                <button class="toggle-btn hidden" id="next-${lessonNumber}" onclick="createLesson('${subject}', ${grade}, ${lessonNumber + 1})">إنشاء الدرس ${lessonNumber + 1}</button>
            `;
            lessonContainer.appendChild(lessonDiv);
        }

        // وظيفة لحفظ الدرس
        function saveLesson(subject, grade, lessonNumber) {
            showToast("تم حفظ الدرس " + lessonNumber);
            document.getElementById(`next-${lessonNumber}`).classList.remove('hidden');
        }

        // وظيفة لتعديل الدرس
        function editLesson(lessonNumber) {
            const titleInput = document.getElementById(`title-${lessonNumber}`);
            const textInput = document.getElementById(`text-${lessonNumber}`);
            titleInput.readOnly = !titleInput.readOnly;
            textInput.readOnly = !textInput.readOnly;
            showToast("تم تفعيل وضع التعديل للدرس " + lessonNumber);
        }

        // وظيفة لحذف الدرس مع تأكيد
        function confirmDeleteLesson(subject, grade, lessonNumber) {
            if (confirm("هل أنت متأكد من حذف هذا الدرس؟")) {
                deleteLesson(subject, grade, lessonNumber);
            }
        }

        // وظيفة لحذف الدرس
        function deleteLesson(subject, grade, lessonNumber) {
            document.getElementById(`lesson-${subject}-${grade}-${lessonNumber}`).remove();
            showToast("تم حذف الدرس " + lessonNumber, true);
        }

        // وظيفة لنسخ الشرح
        function copyLesson(lessonNumber) {
            const text = document.getElementById(`text-${lessonNumber}`).value;
            navigator.clipboard.writeText(text).then(() => {
                showToast("تم نسخ محتوى الدرس " + lessonNumber);
            });
        }

        // وظيفة لإضافة سؤال
        function addQuestion(lessonNumber) {
            const questionsDiv = document.getElementById(`questions-${lessonNumber}`);
            if (!questionsDiv) {
                showToast("حدث خطأ في إضافة السؤال!", true);
                return;
            }

            const questionDiv = document.createElement('div');
            questionDiv.className = 'question-container';
            questionDiv.innerHTML = `
                <input type="text" placeholder="اكتب السؤال هنا">
                <input type="text" placeholder="الإجابة الصحيحة">
                <input type="text" placeholder="إجابة خاطئة 1">
                <input type="text" placeholder="إجابة خاطئة 2">
                <button onclick="checkAnswers('${lessonNumber}')">تحقق</button>
                <button onclick="this.parentElement.remove()">حذف السؤال</button>
            `;
            questionsDiv.appendChild(questionDiv);
            showToast("تم إضافة سؤال جديد!");
        }

        // وظيفة للتحقق من الإجابات
        function checkAnswers(lessonNumber) {
            showToast("تم التحقق من الإجابات للدرس " + lessonNumber);
        }

        // وظيفة لتحميل وعرض الفيديو
        function handleVideoUpload(subject, grade, lessonNumber) {
            const videoInput = document.getElementById(`video-${lessonNumber}`);
            const videoContainer = document.getElementById(`video-container-${lessonNumber}`);
            if (videoInput.files && videoInput.files[0]) {
                const videoURL = URL.createObjectURL(videoInput.files[0]);
                videoContainer.innerHTML = `
                    <video controls><source src="${videoURL}" type="video/mp4"></video>
                    <div class="file-name">${videoInput.files[0].name}</div>
                `;
                showToast("تم تحميل الفيديو بنجاح!");
            } else {
                showToast("لم يتم اختيار ملف فيديو!", true);
            }
        }

        // وظيفة لتحميل وعرض PDF
        function handlePDFUpload(subject, grade, lessonNumber) {
            const pdfInput = document.getElementById(`pdf-${lessonNumber}`);
            const pdfContainer = document.getElementById(`pdf-container-${lessonNumber}`);
            if (pdfInput.files && pdfInput.files[0]) {
                const pdfURL = URL.createObjectURL(pdfInput.files[0]);
                pdfContainer.innerHTML = `
                    <embed src="${pdfURL}" width="100%" height="600px" type="application/pdf">
                    <div class="file-name">${pdfInput.files[0].name}</div>
                `;
                showToast("تم تحميل ملف PDF بنجاح!");
            } else {
                showToast("لم يتم اختيار ملف PDF!", true);
            }
        }

        // إنشاء الأقسام الدراسية
        createGradeSection('primary', 1, 6, ["القرآن الكريم", "التربية الإسلامية", "اللغة العربية", "الرياضيات", "العلوم", "الدراسات الاجتماعية"]);
        createGradeSection('middle', 7, 9, ["القرآن الكريم", "التربية الإسلامية", "اللغة العربية", "الرياضيات", "العلوم", "الدراسات الاجتماعية", "اللغة الإنجليزية"]);
        createGradeSection('highschool', 10, 12, ["القرآن الكريم", "التربية الإسلامية", "اللغة العربية", "الرياضيات", "الفيزياء", "الكيمياء", "الأحياء", "اللغة الإنجليزية"]);
    </script>
</body>
</html>
