---
description: Puede obtener acceso y utilizar cualquier servicio Web XML, incluso si ese servicio Web XML no se creó con COM+ o incluso Microsoft Windows, siempre y cuando el servicio Web XML publique una descripción WSDL de su sintaxis.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Obtener acceso a los servicios Web XML en modo WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807297"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a><span data-ttu-id="877ce-103">Obtener acceso a los servicios Web XML en modo WKO</span><span class="sxs-lookup"><span data-stu-id="877ce-103">Accessing XML Web Services in WKO Mode</span></span>

<span data-ttu-id="877ce-104">Puede obtener acceso y utilizar cualquier servicio Web XML, incluso si ese servicio Web XML no se creó con COM+ o incluso Microsoft Windows, siempre y cuando el servicio Web XML publique una descripción WSDL de su sintaxis.</span><span class="sxs-lookup"><span data-stu-id="877ce-104">You can access and use any XML web service, even if that XML web service was not created using COM+ or even Microsoft Windows, as long as the XML Web Service publishes a WSDL description of its syntax.</span></span> <span data-ttu-id="877ce-105">Basta con crear una instancia del componente mediante el moniker SOAP: WSDL = URL, donde URL es la dirección URL de la descripción WSDL del servicio Web XML al que desea obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="877ce-105">Just create an instance of the component by using the soap:wsdl=URL moniker, where URL is the URL of the WSDL description of the XML web service you want to access.</span></span> <span data-ttu-id="877ce-106">Este es el modo de objeto conocido (WKO) de tener acceso a los servicios Web XML.</span><span class="sxs-lookup"><span data-stu-id="877ce-106">This is the well-known object (WKO) mode of accessing XML web services.</span></span>

<span data-ttu-id="877ce-107">Se puede llamar a los métodos del objeto sin ninguna consideración especial.</span><span class="sxs-lookup"><span data-stu-id="877ce-107">The object's methods can be called without any special considerations.</span></span> <span data-ttu-id="877ce-108">Se tiene acceso al servicio Web XML a través de una consulta SOAP y la respuesta se interpreta de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="877ce-108">The XML web service is accessed via a SOAP query, and the response is interpreted transparently.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="877ce-109">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="877ce-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="877ce-110">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="877ce-110">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="877ce-111">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="877ce-111">Visual Basic</span></span>

<span data-ttu-id="877ce-112">En el siguiente fragmento de código de Microsoft Visual Basic se muestra el uso de un servicio Web XML en modo WKO.</span><span class="sxs-lookup"><span data-stu-id="877ce-112">The following Microsoft Visual Basic code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



<span data-ttu-id="877ce-113">En este fragmento de código, que muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio Web XML, ServerName es el nombre de dominio completo del servidor que ofrece el servicio Web XML. vroot es el directorio raíz virtual de IIS desde el que se expone el servicio Web XML. y progID es el ProgID del componente que desea usar.</span><span class="sxs-lookup"><span data-stu-id="877ce-113">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="cc"></a><span data-ttu-id="877ce-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="877ce-114">C/C++</span></span>

<span data-ttu-id="877ce-115">En el fragmento de código siguiente se muestra el uso de un servicio Web XML en modo WKO.</span><span class="sxs-lookup"><span data-stu-id="877ce-115">The following code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



<span data-ttu-id="877ce-116">En este fragmento de código, que muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio Web XML, ServerName es el nombre de dominio completo del servidor que ofrece el servicio Web XML. vroot es el directorio raíz virtual de IIS desde el que se expone el servicio Web XML. y progID es el ProgID del componente que desea usar.</span><span class="sxs-lookup"><span data-stu-id="877ce-116">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="877ce-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="877ce-117">Remarks</span></span>

<span data-ttu-id="877ce-118">Cuando se obtiene acceso por primera vez a un servicio Web XML en el modo WKO, COM+ genera un cliente proxy y lo compila en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="877ce-118">When an XML web service is first accessed in WKO mode, COM+ generates a proxy client and compiles it in the background.</span></span> <span data-ttu-id="877ce-119">Esta generación en tiempo de ejecución y la falta de conexiones persistentes en modo WKO producen un rendimiento significativamente menor en comparación con el modo de CAO.</span><span class="sxs-lookup"><span data-stu-id="877ce-119">This run-time generation and the lack of persistent connections in WKO mode results in significantly reduced performance in comparison to CAO mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="877ce-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="877ce-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877ce-121">Obtener acceso a los servicios Web XML en el modo de CAO</span><span class="sxs-lookup"><span data-stu-id="877ce-121">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="877ce-122">Introducción al servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="877ce-122">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="877ce-123">Crear servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="877ce-123">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="877ce-124">Proteger los servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="877ce-124">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



