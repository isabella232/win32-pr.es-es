---
description: La propiedad IsLocal del objeto SWbemProperty es un valor booleano que se puede usar para determinar si esta propiedad es local. Un valor de FALSE indica que esta propiedad se ha heredado de otra clase. Esta propiedad es de solo lectura.
ms.assetid: eda1f962-03b5-4322-bb06-c27aedf94be1
ms.tgt_platform: multiple
title: Propiedad SWbemProperty. IsLocal (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.IsLocal
- ISWbemProperty.IsLocal
- ISWbemProperty.get_IsLocal
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 187613a0111c7ad482c55e3d294d77fddb5b0941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910274"
---
# <a name="swbempropertyislocal-property"></a><span data-ttu-id="8807c-105">Propiedad SWbemProperty. IsLocal</span><span class="sxs-lookup"><span data-stu-id="8807c-105">SWbemProperty.IsLocal property</span></span>

<span data-ttu-id="8807c-106">La propiedad **IsLocal** del objeto [**SWbemProperty**](swbemproperty.md) es un valor booleano que se puede usar para determinar si esta propiedad es local.</span><span class="sxs-lookup"><span data-stu-id="8807c-106">The **IsLocal** property of the [**SWbemProperty**](swbemproperty.md) object is a Boolean value that can be used to determine if this property is local.</span></span> <span data-ttu-id="8807c-107">Un valor de **false** indica que esta propiedad se ha heredado de otra clase.</span><span class="sxs-lookup"><span data-stu-id="8807c-107">A value of **FALSE** indicates that this property has been inherited from another class.</span></span> <span data-ttu-id="8807c-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8807c-108">This property is read-only.</span></span>

<span data-ttu-id="8807c-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8807c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="8807c-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8807c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8807c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8807c-111">Syntax</span></span>


```VB
SWbemProperty.IsLocal As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8807c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8807c-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="8807c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8807c-113">Requirements</span></span>



| <span data-ttu-id="8807c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8807c-114">Requirement</span></span> | <span data-ttu-id="8807c-115">Value</span><span class="sxs-lookup"><span data-stu-id="8807c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8807c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8807c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8807c-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8807c-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8807c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8807c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8807c-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8807c-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8807c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8807c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8807c-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8807c-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8807c-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8807c-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="8807c-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8807c-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8807c-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8807c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8807c-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8807c-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8807c-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="8807c-126">CLSID</span></span><br/>                    | <span data-ttu-id="8807c-127">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="8807c-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="8807c-128">IID</span><span class="sxs-lookup"><span data-stu-id="8807c-128">IID</span></span><br/>                      | <span data-ttu-id="8807c-129">\_ISWBEMPROPERTY IID</span><span class="sxs-lookup"><span data-stu-id="8807c-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




