---
description: Si el servicio Web XML al que desea tener acceso se ha creado mediante la exposición de una aplicación COM+, considere la posibilidad de tener acceso a él en modo de objeto activado en el cliente (CAO), lo que evita la generación en tiempo de ejecución de un proxy y aumenta el rendimiento mediante conexiones persistentes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Obtener acceso a los servicios Web XML en el modo de CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686437"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a><span data-ttu-id="e77d1-103">Obtener acceso a los servicios Web XML en el modo de CAO</span><span class="sxs-lookup"><span data-stu-id="e77d1-103">Accessing XML Web Services in CAO Mode</span></span>

<span data-ttu-id="e77d1-104">Si el servicio Web XML al que desea tener acceso se ha creado mediante la exposición de una aplicación COM+, considere la posibilidad de tener acceso a él en modo de objeto activado en el cliente (CAO), lo que evita la generación en tiempo de ejecución de un proxy y aumenta el rendimiento mediante conexiones persistentes.</span><span class="sxs-lookup"><span data-stu-id="e77d1-104">If the XML web service you want to access was created by exposing a COM+ application, consider accessing it in client-activated object (CAO) mode, which avoids the run-time generation of a proxy and increases performance by using persistent connections.</span></span> <span data-ttu-id="e77d1-105">Para tener acceso a un servicio Web XML en modo de CAO, primero [exporte](exporting-a-soap-enabled-application.md) la aplicación habilitada para SOAP correspondiente del servidor en modo proxy y, a continuación, [importe](importing-a-soap-enabled-application.md) la aplicación en el cliente desde el que desea obtener acceso a la aplicación como un servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="e77d1-105">To access an XML web service in CAO mode, first [export](exporting-a-soap-enabled-application.md) the corresponding SOAP-enabled application from your server in proxy mode and then [import](importing-a-soap-enabled-application.md) the application into the client from which you want to access the application as an XML web service.</span></span> <span data-ttu-id="e77d1-106">A continuación, se pueden crear instancias de los componentes de la aplicación en el cliente, al igual que los componentes de las aplicaciones locales, por ejemplo, mediante **GetObject** e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="e77d1-106">The application's components can then be instantiated on the client just like the components of local applications—for example, using **GetObject** and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="user-interface"></a><span data-ttu-id="e77d1-107">Interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="e77d1-107">User Interface</span></span>

<span data-ttu-id="e77d1-108">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="e77d1-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="e77d1-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e77d1-109">Visual Basic</span></span>

<span data-ttu-id="e77d1-110">En el siguiente fragmento de código de Visual Basic se muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio Web XML en modo de CAO.</span><span class="sxs-lookup"><span data-stu-id="e77d1-110">The following Visual Basic code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a><span data-ttu-id="e77d1-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="e77d1-111">C/C++</span></span>

<span data-ttu-id="e77d1-112">En el fragmento de código siguiente se muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio Web XML en modo de CAO.</span><span class="sxs-lookup"><span data-stu-id="e77d1-112">The following code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a><span data-ttu-id="e77d1-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e77d1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e77d1-114">Obtener acceso a los servicios Web XML en modo WKO</span><span class="sxs-lookup"><span data-stu-id="e77d1-114">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="e77d1-115">Introducción al servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="e77d1-115">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="e77d1-116">Crear servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="e77d1-116">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="e77d1-117">Proteger los servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="e77d1-117">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 
