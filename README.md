<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.कला

वेबसाइट कोड का एक हिस्सा खुला स्रोत है, अनुवाद को अनुकूलित करने में सहायता के लिए आपका स्वागत है।

## फ्रंट-एंड कोड

* [फ्रंट-एंड कोड](https://github.com/xxai-art/web)
* [पूरी साइट के लिए भाषा पैक](https://github.com/xxai-art/web/tree/main/i18n)
* [लॉगिन मॉड्यूल के लिए भाषा पैक](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [वेबसाइट बहुभाषी दस्तावेज़ीकरण](https://github.com/xxai-doc)

फ्रंट-एंड प्रोग्रामिंग भाषा [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) है, जो कॉफ़ीस्क्रिप्ट सिंटैक्स के आधार पर कुछ सुविधाएँ जोड़ती है, देखें [./coffee_plus.md](./coffee_plus.md) ।

## वेबसाइटों और दस्तावेजों का अंतर्राष्ट्रीयकरण

निम्नलिखित 3 परियोजनाओं पर निर्माण करें

### [@w5/एमडीटी](https://www.npmjs.com/package/@w5/mdt)

प्रत्यय `.mdt` के साथ मार्कडाउन टेम्प्लेट, `<+ ./coffee_plus/import.js>` के समान सिंटैक्स वाली बाहरी फ़ाइलों को संदर्भित कर सकता है।

[@w5/टीआरएमडी](https://www.npmjs.com/package/@w5/trmd)

मार्कडाउन अनुवाद कोड और लिंक का अनुवाद नहीं करेगा, और अनुवादित वाक्यों को कैश करेगा। यदि अनुवाद संशोधित किया गया है लेकिन मूल पाठ संशोधित नहीं किया गया है, तो इसे फिर से क्रियान्वित करने से अनुवाद के संशोधन को अधिलेखित नहीं किया जाएगा।

[@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

`yaml` जनरेट की गई वेबसाइटों के अनुवाद के लिए भाषा फ़ाइलें।
