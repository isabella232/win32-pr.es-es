---
description: La propiedad parameters del objeto SWbemMethod es un objeto SWbemObject cuyas propiedades definen los parámetros de entrada para este método.
ms.assetid: fba1bb97-29f9-41d3-8ecc-f283989118c1
ms.tgt_platform: multiple
title: Propiedad SWbemMethod. Parameters (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.InParameters
- ISWbemMethod.InParameters
- ISWbemMethod.get_InParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8df897f876673f6b4afe875e718401ae4c217e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696797"
---
# <a name="swbemmethodinparameters-property"></a><span data-ttu-id="c5e7d-103">SWbemMethod. Parameters (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c5e7d-103">SWbemMethod.InParameters property</span></span>

<span data-ttu-id="c5e7d-104">La propiedad **Parameters** del objeto [**SWbemMethod**](swbemmethod.md) es un objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros de entrada para este método.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-104">The **InParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span> <span data-ttu-id="c5e7d-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-105">This property is read-only.</span></span> <span data-ttu-id="c5e7d-106">Tenga en cuenta que los cambios que se realicen en este objeto no se reflejarán en la definición del método subyacente.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-106">Note that any changes that are made to this object are not reflected in the underlying method definition.</span></span>

<span data-ttu-id="c5e7d-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c5e7d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c5e7d-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5e7d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e7d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5e7d-109">Syntax</span></span>


```VB
SWbemMethod.InParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="c5e7d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c5e7d-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c5e7d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5e7d-111">Remarks</span></span>

<span data-ttu-id="c5e7d-112">Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c5e7d-112">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e7d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5e7d-113">Requirements</span></span>



| <span data-ttu-id="c5e7d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e7d-114">Requirement</span></span> | <span data-ttu-id="c5e7d-115">Value</span><span class="sxs-lookup"><span data-stu-id="c5e7d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e7d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5e7d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e7d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5e7d-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5e7d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5e7d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e7d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5e7d-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5e7d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5e7d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e7d-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5e7d-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5e7d-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c5e7d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5e7d-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5e7d-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5e7d-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5e7d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5e7d-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5e7d-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5e7d-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="c5e7d-126">CLSID</span></span><br/>                    | <span data-ttu-id="c5e7d-127">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="c5e7d-127">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="c5e7d-128">IID</span><span class="sxs-lookup"><span data-stu-id="c5e7d-128">IID</span></span><br/>                      | <span data-ttu-id="c5e7d-129">\_ISWBEMMETHOD IID</span><span class="sxs-lookup"><span data-stu-id="c5e7d-129">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c5e7d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5e7d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e7d-131">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="c5e7d-131">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="c5e7d-132">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="c5e7d-132">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="c5e7d-133">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="c5e7d-133">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="c5e7d-134">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="c5e7d-134">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="c5e7d-135">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="c5e7d-135">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




