---
description: La \_ propiedad path del objeto SWbemObject devuelve un objeto SWbemObjectPath que representa la ruta de acceso del objeto de la clase o la instancia actual. Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277508"
---
# <a name="swbemobjectpath_-property"></a><span data-ttu-id="0d8db-104">SWbemObject. Path \_ (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0d8db-104">SWbemObject.Path\_ property</span></span>

<span data-ttu-id="0d8db-105">La **propiedad \_ path** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="0d8db-105">The **Path\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="0d8db-106">Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="0d8db-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="0d8db-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0d8db-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0d8db-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0d8db-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8db-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d8db-109">Syntax</span></span>


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="0d8db-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0d8db-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8db-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d8db-111">Remarks</span></span>

<span data-ttu-id="0d8db-112">Solo se puede modificar la propiedad de [**clase**](swbemobjectpath-class.md) de la instancia de [**SWbemObjectPath**](swbemobjectpath.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="0d8db-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="0d8db-113">Si intenta modificar cualquier otra propiedad o intenta llamar a los métodos [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton**](swbemobjectpath-setassingleton.md), obtendrá un error **wbemErrReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="0d8db-113">If you try to modify any other property, or try to call the methods [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md), you will get a **wbemErrReadOnly** error.</span></span>

<span data-ttu-id="0d8db-114">Por este motivo, no se puede modificar el objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que es el valor de la propiedad [**Keys**](swbemobjectpath-keys.md) de la instancia de [**SWbemObjectPath**](swbemobjectpath.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="0d8db-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="0d8db-115">Si intenta llamar a los métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) en este valor, recibirá un error wbemErrReadOnly.</span><span class="sxs-lookup"><span data-stu-id="0d8db-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you will get a wbemErrReadOnly error.</span></span> <span data-ttu-id="0d8db-116">Además, no se puede modificar ningún [**SWbemNamedValue**](swbemnamedvalue.md) Obtenido de esta colección.</span><span class="sxs-lookup"><span data-stu-id="0d8db-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="0d8db-117">Los intentos de modificar la propiedad **Value** devuelven el mismo código de error.</span><span class="sxs-lookup"><span data-stu-id="0d8db-117">Attempts to modify the **Value** property return the same error code.</span></span>

<span data-ttu-id="0d8db-118">Sin embargo, si llama a [**SWbemObject. \_ Clone**](swbemobject-clone-.md) para crear una copia, la propiedad [**SWbemObjectPath. Path**](swbemobjectpath-path.md) de la copia es totalmente modificable.</span><span class="sxs-lookup"><span data-stu-id="0d8db-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**SWbemObjectPath.Path**](swbemobjectpath-path.md) property of the copy is fully modifiable.</span></span>

## <a name="examples"></a><span data-ttu-id="0d8db-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0d8db-119">Examples</span></span>

<span data-ttu-id="0d8db-120">El siguiente ejemplo de código, tomado de la [lista de todas las clases de WMI cimv2](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) en la galería de TechNet, usa la \_ propiedad path para enumerar todas las clases de WMI cimv2.</span><span class="sxs-lookup"><span data-stu-id="0d8db-120">The following code sample, taken from [List All the WMI cimV2 Classes](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in the TechNet Gallery, uses the Path\_ property to list all the WMI cimV2 classes.</span></span>


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a><span data-ttu-id="0d8db-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d8db-121">Requirements</span></span>



| <span data-ttu-id="0d8db-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d8db-122">Requirement</span></span> | <span data-ttu-id="0d8db-123">Value</span><span class="sxs-lookup"><span data-stu-id="0d8db-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8db-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d8db-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0d8db-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d8db-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d8db-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d8db-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0d8db-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d8db-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d8db-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d8db-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d8db-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d8db-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d8db-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0d8db-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d8db-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d8db-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d8db-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d8db-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d8db-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d8db-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d8db-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="0d8db-134">CLSID</span></span><br/>                    | <span data-ttu-id="0d8db-135">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="0d8db-135">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="0d8db-136">IID</span><span class="sxs-lookup"><span data-stu-id="0d8db-136">IID</span></span><br/>                      | <span data-ttu-id="0d8db-137">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="0d8db-137">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




