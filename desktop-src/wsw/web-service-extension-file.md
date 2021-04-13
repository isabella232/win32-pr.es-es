---
title: Archivo de extensión de servicio Web
description: En esta sección se describe el archivo de extensión de servicio Web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Servicios Web de archivo de extensión de servicio web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359533"
---
# <a name="web-service-extension-file"></a><span data-ttu-id="caecc-106">Archivo de extensión de servicio Web</span><span class="sxs-lookup"><span data-stu-id="caecc-106">Web Service Extension File</span></span>

<span data-ttu-id="caecc-107">En esta sección se describe el archivo de extensión de servicio Web.</span><span class="sxs-lookup"><span data-stu-id="caecc-107">This section outlines Web Service extension file.</span></span>


<span data-ttu-id="caecc-108">El archivo WSX (extensión de servicio WCF) es el archivo de extensión que permite a la aplicación manipular comportamientos locales que no afectan a la representación de los datos de conexión.</span><span class="sxs-lookup"><span data-stu-id="caecc-108">WSX file (WCF service extension) is our extension file to allow application to manipulate local behaviors that do not affect wire data representation.</span></span> <span data-ttu-id="caecc-109">Debe ser extensible que podamos agregar nuevas características en el futuro sin interrumpir la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="caecc-109">It should be extensible that we can add new features in the future without breaking interoperability.</span></span>

<span data-ttu-id="caecc-110">La estructura general de WSX imitaría la estructura del archivo XSD o WSDL, que es un archivo XML que mantiene la misma estructura que el archivo de entrada principal.</span><span class="sxs-lookup"><span data-stu-id="caecc-110">The overall structure of WSX would mimic the structure of XSD or WSDL file, which is a XML file that maintains the same structure as the main input file.</span></span> <span data-ttu-id="caecc-111">Los atributos adicionales en el mismo token con nombre en el archivo principal especificarían los atributos que la aplicación desea controlar sobre el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="caecc-111">Extra attributes on the same named token in main file would specify the attributes that application wants to control over the default behavior.</span></span>

<span data-ttu-id="caecc-112">Es posible que no haga nada aquí en m3.</span><span class="sxs-lookup"><span data-stu-id="caecc-112">We might not do anything here in M3.</span></span> <span data-ttu-id="caecc-113">En la versión 1, se puede ver que se admiten los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="caecc-113">In V1, I can see we support the following attributes:</span></span>

<span data-ttu-id="caecc-114">Uso que especifica el argumento Count o el campo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="caecc-114">Usage Specifying count argument/parameter field.</span></span>

<span data-ttu-id="caecc-115">Se trata de un atributo de elemento, pero aplicable solo al tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="caecc-115">This is an element attribute but applicable to array type only.</span></span> <span data-ttu-id="caecc-116">El atributo IsCountOf especifica el elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="caecc-116">IsCountOf attribute specifies the array element.</span></span> <span data-ttu-id="caecc-117">El campo/parámetro de recuento no aparece en el cable.</span><span class="sxs-lookup"><span data-stu-id="caecc-117">The count field/parameter does not appear on wire.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

<span data-ttu-id="caecc-118">Especificar una devolución de llamada de lectura/escritura para el tipo personalizado</span><span class="sxs-lookup"><span data-stu-id="caecc-118">Specifying read/write callback for custom type</span></span>

<span data-ttu-id="caecc-119">Estos atributos fuerzan wsutil.exe para generar el [**\_ \_ tipo personalizado de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para el tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="caecc-119">These attributes force wsutil.exe to generate [**WS\_CUSTOM\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) for specified type.</span></span> <span data-ttu-id="caecc-120">\_el atributo ReadCallBack personalizado especifica la rutina de [**devolución de llamada de lectura**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) y writecallback personalizado \_ especifica la rutina de [**devolución de llamada de escritura**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .</span><span class="sxs-lookup"><span data-stu-id="caecc-120">custom\_readcallback attribute specifies the [**read callback**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) routine, and custom\_writecallback specifies the [**write callback**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) routine.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

<span data-ttu-id="caecc-121">Podemos tener un archivo WSX coincidente para describir su comportamiento local:</span><span class="sxs-lookup"><span data-stu-id="caecc-121">We can have a matching WSX file to describe its local behavior:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

<span data-ttu-id="caecc-122">WsUtil.exe genera el siguiente prototipo para la estructura:</span><span class="sxs-lookup"><span data-stu-id="caecc-122">WsUtil.exe generates the following prototype for the structure:</span></span>

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




