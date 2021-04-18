---
description: La propiedad SWbemRefreshableItem. IsSet es un valor booleano que indica si el objeto SWbemRefreshableItem representa un solo objeto o un conjunto de objetos. El objeto SWbemRefreshableItem representa un único objeto o un conjunto de objetos.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Propiedad SWbemRefreshableItem. IsSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697927"
---
# <a name="swbemrefreshableitemisset-property"></a><span data-ttu-id="46afa-103">Propiedad SWbemRefreshableItem. IsSet</span><span class="sxs-lookup"><span data-stu-id="46afa-103">SWbemRefreshableItem.IsSet property</span></span>

<span data-ttu-id="46afa-104">La propiedad **SWbemRefreshableItem. IsSet** es un valor booleano que indica si el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) representa un solo objeto o un conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="46afa-104">The **SWbemRefreshableItem.IsSet** property is a Boolean value that indicates whether the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object represents a single object or an object set.</span></span>

<span data-ttu-id="46afa-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="46afa-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="46afa-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="46afa-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="46afa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46afa-107">Syntax</span></span>


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a><span data-ttu-id="46afa-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="46afa-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="46afa-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46afa-109">Remarks</span></span>

<span data-ttu-id="46afa-110">Si **SWbemRefreshableItem. IsSet** es **true**, el elemento representa un objeto [**SWbemObjectSet**](swbemobjectset.md) y la propiedad del [**objeto**](swbemrefreshableitem-object.md) será **null**.</span><span class="sxs-lookup"><span data-stu-id="46afa-110">If **SWbemRefreshableItem.IsSet** is **TRUE**, then the item represents an [**SWbemObjectSet**](swbemobjectset.md) object and the [**Object**](swbemrefreshableitem-object.md) property will be **NULL**.</span></span> <span data-ttu-id="46afa-111">Si es **false**, el elemento representa un objeto [**SWbemObject**](swbemobject.md) y la propiedad del **objeto** es **null**.</span><span class="sxs-lookup"><span data-stu-id="46afa-111">If **FALSE**, the item represents an [**SWbemObject**](swbemobject.md) object and the **Object** property is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46afa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46afa-112">Requirements</span></span>



| <span data-ttu-id="46afa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="46afa-113">Requirement</span></span> | <span data-ttu-id="46afa-114">Value</span><span class="sxs-lookup"><span data-stu-id="46afa-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46afa-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46afa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="46afa-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46afa-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46afa-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46afa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="46afa-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46afa-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46afa-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46afa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="46afa-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="46afa-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="46afa-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="46afa-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="46afa-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46afa-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46afa-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46afa-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46afa-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46afa-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="46afa-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="46afa-125">CLSID</span></span><br/>                    | <span data-ttu-id="46afa-126">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="46afa-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="46afa-127">IID</span><span class="sxs-lookup"><span data-stu-id="46afa-127">IID</span></span><br/>                      | <span data-ttu-id="46afa-128">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="46afa-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="46afa-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="46afa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46afa-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="46afa-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="46afa-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="46afa-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




