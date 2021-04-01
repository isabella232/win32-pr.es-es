---
description: La \_ propiedad path del objeto SWbemLastError devuelve un objeto SWbemObjectPath que representa la ruta de acceso del objeto de la clase o la instancia actual. Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: Propiedad SWbemLastError.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082864"
---
# <a name="swbemlasterrorpath_-property"></a><span data-ttu-id="49695-104">SWbemLastError. Path \_ (propiedad)</span><span class="sxs-lookup"><span data-stu-id="49695-104">SWbemLastError.Path\_ property</span></span>

<span data-ttu-id="49695-105">La **propiedad \_ path** del objeto [**SWbemLastError**](swbemlasterror.md) devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="49695-105">The **Path\_** property of the [**SWbemLastError**](swbemlasterror.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="49695-106">Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="49695-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="49695-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="49695-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="49695-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="49695-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="49695-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49695-109">Syntax</span></span>


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="49695-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="49695-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="49695-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49695-111">Remarks</span></span>

<span data-ttu-id="49695-112">Solo se puede modificar la propiedad de [**clase**](swbemobjectpath-class.md) de la instancia de [**SWbemObjectPath**](swbemobjectpath.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="49695-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="49695-113">Si intenta modificar cualquier otra propiedad o intenta llamar a los métodos [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton**](swbemobjectpath-setassingleton.md) , obtendrá un error de **wbemErrReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="49695-113">If you try to modify any other property, or try to call the [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md) methods, you get an error of **wbemErrReadOnly**.</span></span>

<span data-ttu-id="49695-114">Por este motivo, no se puede modificar el objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que es el valor de la propiedad [**Keys**](swbemobjectpath-keys.md) de la instancia de [**SWbemObjectPath**](swbemobjectpath.md) devuelta.</span><span class="sxs-lookup"><span data-stu-id="49695-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="49695-115">Si intenta llamar a los métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) en este valor, obtendrá un error **wbemErrReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="49695-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you get a **wbemErrReadOnly** error.</span></span> <span data-ttu-id="49695-116">Además, no se puede modificar ningún [**SWbemNamedValue**](swbemnamedvalue.md) Obtenido de esta colección.</span><span class="sxs-lookup"><span data-stu-id="49695-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="49695-117">Los intentos de modificar la propiedad [**Value**](swbemnamedvalue-value.md) devuelven el mismo código de error.</span><span class="sxs-lookup"><span data-stu-id="49695-117">Attempts to modify the [**Value**](swbemnamedvalue-value.md) property return the same error code.</span></span>

<span data-ttu-id="49695-118">Sin embargo, si llama a [**SWbemObject. \_ Clone**](swbemobject-clone-.md) para crear una copia, la propiedad [**\_ path**](swbemobject-path-.md) de la copia es totalmente modificable.</span><span class="sxs-lookup"><span data-stu-id="49695-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**Path\_**](swbemobject-path-.md) property of the copy is fully modifiable.</span></span>

## <a name="requirements"></a><span data-ttu-id="49695-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49695-119">Requirements</span></span>



| <span data-ttu-id="49695-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="49695-120">Requirement</span></span> | <span data-ttu-id="49695-121">Value</span><span class="sxs-lookup"><span data-stu-id="49695-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49695-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49695-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49695-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49695-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49695-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49695-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49695-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49695-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49695-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49695-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="49695-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="49695-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="49695-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="49695-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="49695-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="49695-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="49695-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49695-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49695-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49695-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="49695-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="49695-132">CLSID</span></span><br/>                    | <span data-ttu-id="49695-133">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="49695-133">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="49695-134">IID</span><span class="sxs-lookup"><span data-stu-id="49695-134">IID</span></span><br/>                      | <span data-ttu-id="49695-135">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="49695-135">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




