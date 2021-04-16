---
description: Si usa la API de scripting para WMI para recuperar o almacenar información de clase localizada, especifique la configuración regional como parte de un moniker.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Recuperación de clases modificadas mediante la API de scripting para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706092"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a><span data-ttu-id="36b43-103">Recuperación de clases modificadas mediante la API de scripting para WMI</span><span class="sxs-lookup"><span data-stu-id="36b43-103">Retrieving Amended Classes Using the Scripting API for WMI</span></span>

<span data-ttu-id="36b43-104">Si usa la API de scripting para WMI para recuperar o almacenar información de clase localizada, especifique la configuración regional como parte de un moniker.</span><span class="sxs-lookup"><span data-stu-id="36b43-104">If you are using the Scripting API for WMI to retrieve or store localized class information, specify the locale as part of a moniker.</span></span> <span data-ttu-id="36b43-105">O bien, puede proporcionar el nombre de la configuración regional en el parámetro *strLocale* al método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="36b43-105">Or, you can supply the locale name in the *strLocale* parameter to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span> <span data-ttu-id="36b43-106">Al leer o escribir clases modificadas, indique que quiere usar las definiciones de clase localizadas especificando [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) como una marca para el parámetro *iFlags* del método al que llama.</span><span class="sxs-lookup"><span data-stu-id="36b43-106">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) as a flag for the *iFlags* parameter of the method you call.</span></span> <span data-ttu-id="36b43-107">En el caso de PowerShell, puede usar el parámetro *-locale* en [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) para especificar la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="36b43-107">For PowerShell, you can use the *-locale* parameter on [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) to specify the locale.</span></span>

<span data-ttu-id="36b43-108">En el ejemplo de código siguiente se muestra cómo recuperar una clase localizada mediante un moniker de scripting de WMI o el parámetro-locale.</span><span class="sxs-lookup"><span data-stu-id="36b43-108">The following code example shows how to retrieve a localized class by using a WMI scripting moniker or the -locale parameter.</span></span>


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





<span data-ttu-id="36b43-109">En el ejemplo de código siguiente se muestra cómo establecer el parámetro de configuración regional y utilizar la marca [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="36b43-109">The following code example shows how to set the locale parameter and use the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> <span data-ttu-id="36b43-110">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="36b43-110">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="36b43-111">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="36b43-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="36b43-112">En la tabla siguiente se enumeran los métodos que aceptan la marca [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="36b43-112">The following table lists the methods that accept the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>



| <span data-ttu-id="36b43-113">Método sincrónico</span><span class="sxs-lookup"><span data-stu-id="36b43-113">Synchronous Method</span></span>                                                 | <span data-ttu-id="36b43-114">Método asincrónico</span><span class="sxs-lookup"><span data-stu-id="36b43-114">Asynchronous Method</span></span>                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="36b43-115">**SWbemServices. subclasses**</span><span class="sxs-lookup"><span data-stu-id="36b43-115">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)   | [<span data-ttu-id="36b43-116">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="36b43-116">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)   |
| [<span data-ttu-id="36b43-117">**SWbemObject. subclases\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-117">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)        | [<span data-ttu-id="36b43-118">**SWbemObject.SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-118">**SWbemObject.SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)        |
| [<span data-ttu-id="36b43-119">**SWbemServices. instances**</span><span class="sxs-lookup"><span data-stu-id="36b43-119">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)     | [<span data-ttu-id="36b43-120">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="36b43-120">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)     |
| [<span data-ttu-id="36b43-121">**SWbemObject. instances\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-121">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)          | [<span data-ttu-id="36b43-122">**SWbemObject.InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-122">**SWbemObject.InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)          |
| [<span data-ttu-id="36b43-123">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="36b43-123">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)         | [<span data-ttu-id="36b43-124">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="36b43-124">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)         |
| [<span data-ttu-id="36b43-125">**SWbemServices. get**</span><span class="sxs-lookup"><span data-stu-id="36b43-125">**SWbemServices.Get**</span></span>](swbemservices-get.md)                     | [<span data-ttu-id="36b43-126">**SWbemServices. GetAsync**</span><span class="sxs-lookup"><span data-stu-id="36b43-126">**SWbemServices.GetAsync**</span></span>](swbemservices-getasync.md)                     |
| [<span data-ttu-id="36b43-127">**SWbemObject. put\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-127">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)                      | [<span data-ttu-id="36b43-128">**SWbemObject.PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-128">**SWbemObject.PutAsync\_**</span></span>](swbemobject-putasync-.md)                      |
| [<span data-ttu-id="36b43-129">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="36b43-129">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)   | [<span data-ttu-id="36b43-130">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="36b43-130">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)   |
| [<span data-ttu-id="36b43-131">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-131">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)        | [<span data-ttu-id="36b43-132">**SWbemObject.ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-132">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)        |
| [<span data-ttu-id="36b43-133">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="36b43-133">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md) | [<span data-ttu-id="36b43-134">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="36b43-134">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md) |
| [<span data-ttu-id="36b43-135">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-135">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)      | [<span data-ttu-id="36b43-136">**SWbemObject.AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="36b43-136">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)      |



 

 

 
