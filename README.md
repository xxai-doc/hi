<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

निर्देशिका में प्रवेश करने के बाद पहले नोडज, [direnv](https://direnv.net) , [बन](https://github.com/oven-sh/bun) , और फिर `direnv allow` स्थापित करने की अनुशंसा की जाती है (निर्देशिका में प्रवेश करने के बाद [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) स्वचालित रूप से निष्पादित हो जाएगा)।

अर्थ है: जापानी, कोरियाई, अंग्रेजी में चीनी अनुवाद, अन्य सभी भाषाओं में अंग्रेजी अनुवाद। यदि आप केवल चीनी और अंग्रेजी का समर्थन करना चाहते हैं, तो आप केवल `zh: en` लिख सकते हैं।

## फ्रंट-एंड कोड

* [फ्रंट-एंड कोड](https://github.com/xxai-art/web)
* [पूरी साइट के लिए भाषा पैक](https://github.com/xxai-art/web/tree/main/i18n)
* [लॉगिन मॉड्यूल के लिए भाषा पैक](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [वेबसाइट बहुभाषी दस्तावेज़ीकरण](https://github.com/xxai-doc)

फ्रंट-एंड प्रोग्रामिंग भाषा [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) है, जो कॉफ़ीस्क्रिप्ट सिंटैक्स के आधार पर कुछ सुविधाएँ जोड़ती है, देखें [./coffee_plus.md](./coffee_plus.md) ।

## वेबसाइटों और दस्तावेजों का अंतर्राष्ट्रीयकरण

निम्नलिखित 3 परियोजनाओं पर निर्माण करें

* [@w5/एमडीटी](https://www.npmjs.com/package/@w5/mdt)

  प्रत्यय `.mdt` है, आप बाहरी फ़ाइलों को संदर्भित करने के लिए `<+ ./coffee_plus/import.js>` के समान सिंटैक्स का उपयोग कर सकते हैं, और प्रत्यय `.md` के साथ मार्कडाउन उत्पन्न कर सकते हैं।

* [@w5/टीआरएमडी](https://www.npmjs.com/package/@w5/trmd)

  मार्कडाउन अनुवाद कोड और लिंक का अनुवाद नहीं करेगा, और अनुवादित वाक्यों को कैश करेगा। यदि अनुवाद संशोधित किया गया है लेकिन मूल पाठ संशोधित नहीं किया गया है, तो इसे फिर से क्रियान्वित करने से अनुवाद के संशोधन को अधिलेखित नहीं किया जाएगा।

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  `yaml` जनरेट की गई वेबसाइटों के अनुवाद के लिए भाषा फ़ाइलें।

### दस्तावेज़ अनुवाद स्वचालन निर्देश

कोड रिपॉजिटरी [xxai-art/doc](https://github.com/xxai-art/doc) देखें

निर्देशिका में प्रवेश करने के बाद पहले नोडज, [direnv](https://direnv.net) , [बन](https://github.com/oven-sh/bun) , और फिर `direnv allow` स्थापित करने की अनुशंसा की जाती है (निर्देशिका में प्रवेश करने के बाद [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) स्वचालित रूप से निष्पादित हो जाएगा)।

सैकड़ों भाषाओं में अनुवादित बड़े कोड आधार से बचने के लिए, मैंने प्रत्येक भाषा के लिए एक अलग कोड आधार बनाया और कोड आधार को संग्रहीत करने के लिए एक संगठन बनाया

पर्यावरण चर `GITHUB_ACCESS_TOKEN` सेट करना और फिर [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) चलाना स्वचालित रूप से कोड रिपॉजिटरी बना देगा।

बेशक, आप इसे कोड बेस में भी डाल सकते हैं।

अनुवाद स्क्रिप्ट संदर्भ [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

स्क्रिप्ट कोड की व्याख्या इस प्रकार की जाती है:

[बंक्स](https://bun.sh/docs/cli/bunx) एनपीएक्स के लिए एक प्रतिस्थापन है, जो तेज है। बेशक, यदि आपके पास बन इंस्टॉल नहीं है, तो आप इसके बजाय `npx` उपयोग कर सकते हैं।

`bunx mdt zh` `.mdt` `.md` के रूप में zh निर्देशिका में प्रस्तुत करता है, नीचे दी गई 2 लिंक की गई फ़ाइलें देखें

* [Coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [Coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` अनुवाद के लिए मुख्य कोड है (यदि आपके पास केवल `nodejs` स्थापित हैं, लेकिन `bun` और `direnv` स्थापित नहीं हैं, तो आप अनुवाद करने के लिए `npx i18n` भी चला सकते हैं)।

यह [i18n.yml को](https://github.com/xxai-art/doc/blob/main/i18n.yml) पार्स करेगा, इस दस्तावेज़ में `i18n.yml` का विन्यास इस प्रकार है:

```
en:
zh: ja ko en
```

अर्थ है: जापानी, कोरियाई, अंग्रेजी में चीनी अनुवाद, अन्य सभी भाषाओं में अंग्रेजी अनुवाद। यदि आप केवल चीनी और अंग्रेजी का समर्थन करना चाहते हैं, तो आप केवल `zh: en` लिख सकते हैं।

अंतिम [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) है, जो मुख्य शीर्षक और प्रत्येक भाषा के `README.md` के पहले उपशीर्षक के बीच की सामग्री को एक प्रविष्टि `README.md` उत्पन्न करने के लिए निकालता है। कोड बहुत सरल है, आप इसे स्वयं देख सकते हैं।

Google API का उपयोग निःशुल्क अनुवाद के लिए किया जाता है। यदि आप Google तक नहीं पहुंच सकते हैं, तो कृपया कॉन्फ़िगर करें और एक प्रॉक्सी सेट करें, जैसे:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

अनुवाद स्क्रिप्ट `.i18n` निर्देशिका में एक अनुवादित कैश उत्पन्न करेगी, कृपया इसे `git status` से जांचें और बार-बार अनुवाद से बचने के लिए इसे कोड रिपॉजिटरी में जोड़ें।

कैश को अपडेट करने के लिए हर बार जब आप अनुवाद को संशोधित करते हैं तो कृपया `bunx i18n` चलाएं।

यदि मूल पाठ और अनुवाद एक ही समय में संशोधित किए जाते हैं, तो कैश भ्रमित हो जाएगा, इसलिए यदि आप संशोधित करना चाहते हैं, तो आप केवल एक को संशोधित कर सकते हैं, और फिर कैश को अपडेट करने के लिए `bunx i18n` चला सकते हैं।
