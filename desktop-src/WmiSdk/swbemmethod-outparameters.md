---
description: La propiedad parameters del objeto SWbemMethod es un objeto SWbemObject cuyas propiedades definen los parámetros out y el tipo de valor devuelto de este método. Esta propiedad es de solo lectura.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Propiedad SWbemMethod. Parameters (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697315"
---
# <a name="swbemmethodoutparameters-property"></a><span data-ttu-id="f2704-104">SWbemMethod. Parameters (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f2704-104">SWbemMethod.OutParameters property</span></span>

<span data-ttu-id="f2704-105">La propiedad **Parameters** del objeto [**SWbemMethod**](swbemmethod.md) es un objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros out y el tipo de valor devuelto de este método.</span><span class="sxs-lookup"><span data-stu-id="f2704-105">The **OutParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span> <span data-ttu-id="f2704-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f2704-106">This property is read-only.</span></span>

<span data-ttu-id="f2704-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f2704-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f2704-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f2704-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2704-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2704-109">Syntax</span></span>


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="f2704-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f2704-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f2704-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2704-111">Remarks</span></span>

<span data-ttu-id="f2704-112">Para obtener más información sobre cómo usar esta propiedad para obtener los parámetros de salida de los métodos de proveedor, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f2704-112">For more information about how to use this property to obtain output parameters from provider methods, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="f2704-113">Tenga en cuenta que los cambios realizados en este objeto no se reflejan en la definición del método subyacente.</span><span class="sxs-lookup"><span data-stu-id="f2704-113">Note that any changes made to this object are not reflected in the underlying method definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2704-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2704-114">Requirements</span></span>



| <span data-ttu-id="f2704-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2704-115">Requirement</span></span> | <span data-ttu-id="f2704-116">Value</span><span class="sxs-lookup"><span data-stu-id="f2704-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2704-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2704-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2704-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2704-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2704-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2704-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2704-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2704-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2704-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2704-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2704-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2704-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2704-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f2704-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2704-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2704-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2704-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2704-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2704-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2704-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2704-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="f2704-127">CLSID</span></span><br/>                    | <span data-ttu-id="f2704-128">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="f2704-128">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="f2704-129">IID</span><span class="sxs-lookup"><span data-stu-id="f2704-129">IID</span></span><br/>                      | <span data-ttu-id="f2704-130">\_ISWBEMMETHOD IID</span><span class="sxs-lookup"><span data-stu-id="f2704-130">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="f2704-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2704-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2704-132">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="f2704-132">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="f2704-133">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="f2704-133">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="f2704-134">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f2704-134">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="f2704-135">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="f2704-135">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="f2704-136">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="f2704-136">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




