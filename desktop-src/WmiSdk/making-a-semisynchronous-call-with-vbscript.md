---
description: Proporciona la funcionalidad de acceso semisincrónico y un ejemplo de código para crear una llamada de método semisincrónico.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Realización de una llamada semisincrónica con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697417"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a><span data-ttu-id="76c58-103">Realización de una llamada semisincrónica con VBScript</span><span class="sxs-lookup"><span data-stu-id="76c58-103">Making a Semisynchronous Call with VBScript</span></span>

<span data-ttu-id="76c58-104">Algunos métodos WMI pueden devolver colecciones grandes, lo que hace que los scripts dejen de responder.</span><span class="sxs-lookup"><span data-stu-id="76c58-104">Some WMI methods can return large collections, causing scripts to stop responding.</span></span> <span data-ttu-id="76c58-105">En el script, el acceso semisincrónico es el valor predeterminado y Instrumental de administración de Windows (WMI) establece **wbemFlagReturnImmediately** para llamadas que pueden devolver colecciones de objetos grandes como los siguientes métodos [**SWbemServices**](swbemservices.md) : [**instances**](swbemservices-instancesof.md), [**subclasses**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md)y [**referenceto**](swbemservices-referencesto.md).</span><span class="sxs-lookup"><span data-stu-id="76c58-105">In script, semisynchronous access is the default, and Windows Management Instrumentation (WMI) sets **wbemFlagReturnImmediately** for calls that can return large object collections such as the following [**SWbemServices**](swbemservices.md) methods: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md), and [**ReferencesTo**](swbemservices-referencesto.md).</span></span>

<span data-ttu-id="76c58-106">El acceso semisincrónico que usa **wbemFlagReturnImmediately** establecido en el *parámetro IFlags* también es el valor predeterminado para las llamadas que pueden devolver conjuntos de objetos grandes para los siguientes métodos de [**SWbemObject**](swbemobject.md) : [**\_ instancias**](swbemobject-instances-.md), [**subclases \_**](swbemobject-subclasses-.md), [**asociadores \_**](swbemobject-associators-.md)y [**referencias \_**](swbemobject-references-.md).</span><span class="sxs-lookup"><span data-stu-id="76c58-106">Semisynchronous access that uses **wbemFlagReturnImmediately** set in the *IFlags* parameter is also the default for calls that can return large object sets for the following [**SWbemObject**](swbemobject.md) methods: [**Instances\_**](swbemobject-instances-.md), [**Subclasses\_**](swbemobject-subclasses-.md), [**Associators\_**](swbemobject-associators-.md), and [**References\_**](swbemobject-references-.md).</span></span>

<span data-ttu-id="76c58-107">Para reducir el uso de recursos de memoria de WMI al procesar una gran colección de objetos, incluya el valor de **wbemFlagForwardOnly** en el parámetro *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="76c58-107">To reduce the WMI memory resource usage when processing a large collection of objects, include the value of **wbemFlagForwardOnly** in the *IFlags* parameter.</span></span> <span data-ttu-id="76c58-108">El uso de **wbemFlagForwardOnly** hace que WMI cree un enumerador de solo avance que no permite rebobinar la colección y obtener acceso a los elementos de nuevo.</span><span class="sxs-lookup"><span data-stu-id="76c58-108">Using **wbemFlagForwardOnly** causes WMI to create a forward-only enumerator that does not allow rewinding the collection and accessing items again.</span></span>

<span data-ttu-id="76c58-109">WMI elimina la memoria de cada objeto, ya que la instrucción **for each** procesa un objeto.</span><span class="sxs-lookup"><span data-stu-id="76c58-109">WMI eliminates the memory for each object as the **For Each** statement processes an object.</span></span> <span data-ttu-id="76c58-110">No se puede llamar al método **Count** para una colección cuando se estableció la marca **wbemFlagForwardOnly** en la llamada que obtuvo la colección.</span><span class="sxs-lookup"><span data-stu-id="76c58-110">You cannot call the **Count** method for a collection when the **wbemFlagForwardOnly** flag was set on the call that obtained the collection.</span></span> <span data-ttu-id="76c58-111">Tenga en cuenta que el parámetro *IFlags* tiene **wbemFlagReturnImmediately** y **wbemFlagForwardOnly** establecido de forma predeterminada para el método [**cNotificationQuerySWbemServices.Exe**](swbemservices-execnotificationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="76c58-111">Note that the *IFlags* parameter has **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** set by default for the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method.</span></span>

<span data-ttu-id="76c58-112">En el procedimiento siguiente se describe cómo usar VBScript para crear una llamada semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="76c58-112">The following procedure describes how to use VBScript to make a semisynchronous call.</span></span>

<span data-ttu-id="76c58-113">**Para hacer una llamada semisincrónica en VBScript**</span><span class="sxs-lookup"><span data-stu-id="76c58-113">**To make a semisynchronous call in VBScript**</span></span>

1.  <span data-ttu-id="76c58-114">Establezca el parámetro *IFlags* en el valor de [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="76c58-114">Set the *IFlags* parameter to the value of [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>
2.  <span data-ttu-id="76c58-115">Realice la llamada sincrónica normal para [**SWbemServices.ExecQuery**](swbemservices-execquery.md) o [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) con el valor *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="76c58-115">Make the normal synchronous call for [**SWbemServices.ExecQuery**](swbemservices-execquery.md) or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) with the *iFlags* value.</span></span>
3.  <span data-ttu-id="76c58-116">Si desea tratar los objetos devueltos por la llamada como una colección, use una sintaxis de enumeración como VBScript **para cada uno**.</span><span class="sxs-lookup"><span data-stu-id="76c58-116">If you want to treat the objects returned by the call as a collection, use an enumeration syntax such as VBScript **For Each**.</span></span> <span data-ttu-id="76c58-117">A medida que se devuelve cada objeto, se procesa como el elemento siguiente de la colección.</span><span class="sxs-lookup"><span data-stu-id="76c58-117">As each object is returned, it is processed as the next item in the collection.</span></span>
4.  <span data-ttu-id="76c58-118">Cree un enumerador de solo avance combinando el valor de **wbemFlagReturnImmediately** con el valor de **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="76c58-118">Create a forward-only enumerator by combining the value of **wbemFlagReturnImmediately** with the value of **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="76c58-119">El valor decimal de esta operación OR es 48.</span><span class="sxs-lookup"><span data-stu-id="76c58-119">The decimal value of this OR operation is 48.</span></span> <span data-ttu-id="76c58-120">Estas constantes se definen en la biblioteca de tipos wbemdisp. tlb para Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="76c58-120">These constants are defined in the wbemdisp.tlb type library for Visual Basic.</span></span> <span data-ttu-id="76c58-121">La mayoría de los lenguajes de scripting usan el valor numérico o definen una constante.</span><span class="sxs-lookup"><span data-stu-id="76c58-121">Most scripting languages use the numeric value or define a constant.</span></span> <span data-ttu-id="76c58-122">Para obtener más información, vea [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="76c58-122">For more information, see [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>

<span data-ttu-id="76c58-123">En el ejemplo de código siguiente se muestra cómo hacer una llamada de método semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="76c58-123">The following code example shows how to make a semisynchronous method call.</span></span> <span data-ttu-id="76c58-124">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="76c58-124">For more information, see [Calling a Method](calling-a-method.md).</span></span>


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a><span data-ttu-id="76c58-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76c58-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76c58-126">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="76c58-126">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 



