---
description: Use la propiedad Count del objeto SWbemObjectSet para determinar el número de elementos que hay en una colección SWbemObjectSet. Esta propiedad es de solo lectura.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Propiedad SWbemObjectSet. Count (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707265"
---
# <a name="swbemobjectsetcount-property"></a><span data-ttu-id="6ec5c-104">SWbemObjectSet. Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6ec5c-104">SWbemObjectSet.Count property</span></span>

<span data-ttu-id="6ec5c-105">Use la propiedad **Count** del objeto [**SWbemObjectSet**](swbemobjectset.md) para determinar el número de elementos que hay en una colección **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="6ec5c-105">Use the **Count** property of the [**SWbemObjectSet**](swbemobjectset.md) object to determine how many items are in an **SWbemObjectSet** collection.</span></span> <span data-ttu-id="6ec5c-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-106">This property is read-only.</span></span>

<span data-ttu-id="6ec5c-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6ec5c-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6ec5c-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec5c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ec5c-109">Syntax</span></span>


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a><span data-ttu-id="6ec5c-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6ec5c-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec5c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ec5c-111">Remarks</span></span>

<span data-ttu-id="6ec5c-112">Hay que tener cuidado al usar Count es que WMI no mantiene un recuento en ejecución del número de elementos de una colección.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-112">One thing to be careful of when using Count is that WMI does not keep a running tally of the number of items in a collection.</span></span> <span data-ttu-id="6ec5c-113">Si solicita recuento para una colección, WMI no puede responder de forma instantánea con un número; en su lugar, debe contar literalmente los elementos, enumerando la colección completa.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-113">If you request Count for a collection, WMI cannot instantly respond with a number; instead, it must literally count the items, enumerating the entire collection.</span></span> <span data-ttu-id="6ec5c-114">En el caso de una colección que tiene relativamente pocos elementos, como los servicios, esta enumeración probablemente tarda menos de un segundo.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-114">For a collection that has relatively few items, such as services, this enumeration likely takes less than a second.</span></span> <span data-ttu-id="6ec5c-115">No obstante, el recuento del número de eventos de una colección de registros de eventos puede tardar bastante tiempo.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-115">Counting the number of events in an event log collection, however, can take considerably longer.</span></span>

<span data-ttu-id="6ec5c-116">Y, a continuación, supongamos que desea mostrar los valores de propiedad de cada evento de la colección.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-116">And then suppose you want to display the property values for every event in the collection.</span></span> <span data-ttu-id="6ec5c-117">En ese caso, WMI tendrá que enumerar toda la colección por segunda vez.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-117">If so, WMI will have to enumerate the entire collection a second time.</span></span>

> [!Note]  
> <span data-ttu-id="6ec5c-118">Si intenta obtener esta propiedad de un objeto [**SWbemObjectSet**](swbemobjectset.md) que se devuelve desde un método en el que las marcas especificadas se incluyen en la marca wbemFlagForwardOnly, recibirá un error wbemErrFailed.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-118">If you attempt to get this property from an [**SWbemObjectSet**](swbemobjectset.md) object that is returned from a method where the specified flags are included the wbemFlagForwardOnly flag, you will get an wbemErrFailed error.</span></span>

 

## <a name="examples"></a><span data-ttu-id="6ec5c-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6ec5c-119">Examples</span></span>

<span data-ttu-id="6ec5c-120">En su mayor parte, lo único que tendrá que hacer con un SWbemObjectSet es enumerar todos los objetos contenidos en la propia colección.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-120">For the most part, the only thing you will ever do with an SWbemObjectSet is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="6ec5c-121">Sin embargo, el recuento de recuentos puede ser útil en el scripting de administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-121">However, the Count Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="6ec5c-122">Como implica el nombre, Count indica el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-122">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="6ec5c-123">Por ejemplo, este script recupera una colección de todos los servicios instalados en un equipo y, a continuación, devuelve el número total de servicios encontrados:</span><span class="sxs-lookup"><span data-stu-id="6ec5c-123">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



<span data-ttu-id="6ec5c-124">Lo que hace que Count sea útil es que puede indicar si una instancia específica está disponible en un equipo.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-124">What makes Count useful is that it can tell you whether a specific instance is available on a computer.</span></span> <span data-ttu-id="6ec5c-125">Por ejemplo, este script recupera una colección de todos los servicios de un equipo que tienen el nombre W3SVC.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-125">For example, this script retrieves a collection of all the services on a computer that have the Name W3SVC.</span></span> <span data-ttu-id="6ec5c-126">Si el recuento es 0 (y es válido para que las recopilaciones no tengan ninguna instancia), significa que el servicio W3SVC no está instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-126">If the Count is 0 (and it is valid for collections to have no instances), that means the W3SVC service is not installed on the computer.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a><span data-ttu-id="6ec5c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec5c-127">Requirements</span></span>



| <span data-ttu-id="6ec5c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec5c-128">Requirement</span></span> | <span data-ttu-id="6ec5c-129">Value</span><span class="sxs-lookup"><span data-stu-id="6ec5c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec5c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec5c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec5c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ec5c-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ec5c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec5c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec5c-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ec5c-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ec5c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ec5c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec5c-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec5c-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ec5c-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ec5c-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ec5c-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ec5c-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ec5c-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ec5c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec5c-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec5c-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ec5c-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="6ec5c-140">CLSID</span></span><br/>                    | <span data-ttu-id="6ec5c-141">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ec5c-141">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="6ec5c-142">IID</span><span class="sxs-lookup"><span data-stu-id="6ec5c-142">IID</span></span><br/>                      | <span data-ttu-id="6ec5c-143">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="6ec5c-143">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




