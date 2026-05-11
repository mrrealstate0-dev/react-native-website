export default function AmlakRealEstateApp() {
  const apartments = [
    {
      id: 1,
      unit: 'شقة 1',
      buyer: 'أحمد محمد',
      phone: '01000000000',
      nationalId: '29801011234567',
      address: 'مدينة العبور',
      area: '180 متر',
      paymentType: 'تقسيط',
      installmentPlan: '3 سنوات',
      totalPrice: '2,500,000',
      downPayment: '500,000',
      remaining: '2,000,000',
      paymentSchedule: 'شهري',
      paid: '300,000',
      due: '1,700,000',
      status: 'منتظم'
    },
    {
      id: 2,
      unit: 'شقة 2',
      buyer: 'محمد رمضان',
      phone: '01111111111',
      nationalId: '29902021234567',
      address: 'القاهرة',
      area: '210 متر',
      paymentType: 'كاش',
      installmentPlan: '-',
      totalPrice: '3,000,000',
      downPayment: '3,000,000',
      remaining: '0',
      paymentSchedule: '-',
      paid: '3,000,000',
      due: '0',
      status: 'تم السداد'
    }
  ]

  return (
    <div className="min-h-screen bg-gray-100 p-6">
      <div className="max-w-7xl mx-auto">
        <div className="bg-white rounded-3xl shadow-lg p-6 mb-6">
          <h1 className="text-4xl font-bold text-center mb-2">تطبيق أملاك العقارية</h1>
          <p className="text-center text-gray-600">تطبيق موبايل لإدارة العقارات والشقق والأقساط والعملاء</p>
        </div>

        <div className="bg-green-100 border border-green-300 rounded-2xl p-4 mb-6 text-center text-lg font-bold">
          📱 تطبيق أملاك العقارية جاهز للعمل على الموبايل Android و iPhone
        </div>

        <div className="grid grid-cols-1 md:grid-cols-4 gap-4 mb-6">
          <div className="bg-white rounded-2xl shadow p-5 text-center">
            <h2 className="text-lg font-bold">عدد الشقق</h2>
            <p className="text-3xl font-bold mt-2">10</p>
          </div>

          <div className="bg-white rounded-2xl shadow p-5 text-center">
            <h2 className="text-lg font-bold">الشقق المباعة</h2>
            <p className="text-3xl font-bold mt-2">8</p>
          </div>

          <div className="bg-white rounded-2xl shadow p-5 text-center">
            <h2 className="text-lg font-bold">إجمالي التحصيل</h2>
            <p className="text-3xl font-bold mt-2">5.3M</p>
          </div>

          <div className="bg-white rounded-2xl shadow p-5 text-center">
            <h2 className="text-lg font-bold">المتبقي</h2>
            <p className="text-3xl font-bold mt-2">1.7M</p>
          </div>
        </div>

        <div className="bg-white rounded-3xl shadow-lg overflow-hidden">
          <div className="p-5 border-b">
            <h2 className="text-2xl font-bold">بيانات الشقق والعملاء</h2>
          </div>

          <div className="overflow-x-auto">
            <table className="w-full text-sm text-right">
              <thead className="bg-gray-200">
                <tr>
                  <th className="p-3">الوحدة</th>
                  <th className="p-3">اسم المشتري</th>
                  <th className="p-3">الموبايل</th>
                  <th className="p-3">الرقم القومي</th>
                  <th className="p-3">العنوان</th>
                  <th className="p-3">المساحة</th>
                  <th className="p-3">نوع الدفع</th>
                  <th className="p-3">مدة التقسيط</th>
                  <th className="p-3">إجمالي السعر</th>
                  <th className="p-3">المقدم</th>
                  <th className="p-3">المتبقي</th>
                  <th className="p-3">نظام الدفع</th>
                  <th className="p-3">المسدّد</th>
                  <th className="p-3">المستحق</th>
                  <th className="p-3">الحالة</th>
                </tr>
              </thead>

              <tbody>
                {apartments.map((apartment) => (
                  <tr key={apartment.id} className="border-b hover:bg-gray-50">
                    <td className="p-3 font-bold">{apartment.unit}</td>
                    <td className="p-3">{apartment.buyer}</td>
                    <td className="p-3">{apartment.phone}</td>
                    <td className="p-3">{apartment.nationalId}</td>
                    <td className="p-3">{apartment.address}</td>
                    <td className="p-3">{apartment.area}</td>
                    <td className="p-3">{apartment.paymentType}</td>
                    <td className="p-3">{apartment.installmentPlan}</td>
                    <td className="p-3">{apartment.totalPrice}</td>
                    <td className="p-3">{apartment.downPayment}</td>
                    <td className="p-3">{apartment.remaining}</td>
                    <td className="p-3">{apartment.paymentSchedule}</td>
                    <td className="p-3">{apartment.paid}</td>
                    <td className="p-3 text-red-600 font-bold">{apartment.due}</td>
                    <td className="p-3">
                      <span className={`px-3 py-1 rounded-full text-white ${apartment.status === 'تم السداد' ? 'bg-green-500' : 'bg-orange-500'}`}>
                        {apartment.status}
                      </span>
                    </td>
                  </tr>
                ))}
              </tbody>
            </table>
          </div>
        </div>

        <div className="bg-white rounded-3xl shadow-lg p-6 mt-6 mb-6">
            <h2 className="text-2xl font-bold mb-4">مميزات النظام</h2>
            <div className="grid grid-cols-1 md:grid-cols-3 gap-4 text-lg">
              <div className="bg-gray-100 rounded-2xl p-4">✔ إدارة العملاء والعقود</div>
              <div className="bg-gray-100 rounded-2xl p-4">✔ متابعة الأقساط والتنبيهات</div>
              <div className="bg-gray-100 rounded-2xl p-4">✔ تقارير الأرباح والمبيعات</div>
              <div className="bg-gray-100 rounded-2xl p-4">✔ تسجيل الدفعات تلقائياً</div>
              <div className="bg-gray-100 rounded-2xl p-4">✔ إدارة العمارات والشقق</div>
              <div className="bg-gray-100 rounded-2xl p-4">✔ واجهة احترافية لشركة أملاك</div>
            </div>
          </div>

          <div className="grid grid-cols-1 md:grid-cols-2 gap-6 mt-6">
          <div className="bg-white rounded-3xl shadow-lg p-6">
            <h2 className="text-2xl font-bold mb-4">أنظمة السداد</h2>
            <ul className="space-y-3 text-lg">
              <li>✔ كاش</li>
              <li>✔ تقسيط سنة</li>
              <li>✔ تقسيط سنة ونصف</li>
              <li>✔ تقسيط سنتين</li>
              <li>✔ تقسيط 3 سنوات</li>
              <li>✔ دفع شهري أو كل 3 شهور</li>
            </ul>
          </div>

          <div className="bg-white rounded-3xl shadow-lg p-6">
            <h2 className="text-2xl font-bold mb-4">التقارير المتوفرة</h2>
            <ul className="space-y-3 text-lg">
              <li>📊 تقرير الأقساط المستحقة</li>
              <li>📊 تقرير العملاء المتأخرين</li>
              <li>📊 تقرير المبيعات</li>
              <li>📊 تقرير المدفوع والمتبقي</li>
              <li>📊 تقرير الشقق المتاحة</li>
              <li>📲 إشعارات الأقساط والتنبيهات</li>
              <li>📄 طباعة العقود والفواتير PDF</li></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  )
}
---
id: environment-setup
title: Get Started with React Native
hide_table_of_contents: true
---

import PlatformSupport from '@site/src/theme/PlatformSupport';
import BoxLink from '@site/src/theme/BoxLink';

**React Native allows developers who know React to create native apps.** At the same time, native developers can use React Native to gain parity between native platforms by writing common features once.

We believe that the best way to experience React Native is through a **Framework**, a toolbox with all the necessary APIs to let you build production ready apps.

You can also use React Native without a Framework, however we’ve found that most developers benefit from using a React Native Framework like [Expo](https://expo.dev). Expo provides features like file-based routing, high-quality universal libraries, and the ability to write plugins that modify native code without having to manage native files.

<details>
<summary>Can I use React Native without a Framework?</summary>

Yes. You can use React Native without a Framework. **However, if you’re building a new app with React Native, we recommend using a Framework.**

In short, you’ll be able to spend time writing your app instead of writing an entire Framework yourself in addition to your app.

The React Native community has spent years refining approaches to navigation, accessing native APIs, dealing with native dependencies, and more. Most apps need these core features. A React Native Framework provides them from the start of your app.

Without a Framework, you’ll either have to write your own solutions to implement core features, or you’ll have to piece together a collection of pre-existing libraries to create a skeleton of a Framework. This takes real work, both when starting your app, then later when maintaining it.

If your app has unusual constraints that are not served well by a Framework, or you prefer to solve these problems yourself, you can make a React Native app without a Framework using Android Studio, Xcode. If you’re interested in this path, learn how to [set up your environment](set-up-your-environment) and how to [get started without a framework](getting-started-without-a-framework).

</details>

## Start a new React Native project with Expo

<PlatformSupport platforms={['android', 'ios', 'tv', 'web']} />

Expo is a production-grade React Native Framework. Expo provides developer tooling that makes developing apps easier, such as file-based routing, a standard library of native modules, and much more.

Expo's Framework is free and open source, with an active community on [GitHub](https://github.com/expo) and [Discord](https://chat.expo.dev). The Expo team works in close collaboration with the React Native team at Meta to bring the latest React Native features to the Expo SDK.

The team at Expo also provides Expo Application Services (EAS), an optional set of services that complements Expo, the Framework, in each step of the development process.

To create a new Expo project, run the following in your terminal:

```shell
npx create-expo-app@latest
```

Once you’ve created your app, check out the rest of Expo’s getting started guide to start developing your app.

<BoxLink href="https://docs.expo.dev/get-started/set-up-your-environment">Continue with Expo</BoxLink>
