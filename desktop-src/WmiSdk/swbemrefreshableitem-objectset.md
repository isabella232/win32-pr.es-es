---
description: La propiedad SWbemRefreshableItem. ObjectSet representa el conjunto de objetos que se va a actualizar.
ms.assetid: f52101b1-bb6e-4798-b20f-d6efd31cf7c1
ms.tgt_platform: multiple
title: Propiedad SWbemRefreshableItem. ObjectSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.get_ObjectSet
- ISWbemRefreshableItem.put_ObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbc611bb9e1a72f53e2178039b0ad76411e39a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361876"
---
# <a name="swbemrefreshableitemobjectset-property"></a><span data-ttu-id="38454-103">Propiedad SWbemRefreshableItem. ObjectSet</span><span class="sxs-lookup"><span data-stu-id="38454-103">SWbemRefreshableItem.ObjectSet property</span></span>

<span data-ttu-id="38454-104">La propiedad **SWbemRefreshableItem. ObjectSet** representa el conjunto de objetos que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="38454-104">The **SWbemRefreshableItem.ObjectSet** property represents the object set to be refreshed.</span></span> <span data-ttu-id="38454-105">La propiedad **ObjectSet** es un enumerador o un elemento de colección contenido en un objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="38454-105">The **ObjectSet** property is either an enumerator or a collection item that is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="38454-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="38454-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="38454-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="38454-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="38454-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38454-108">Syntax</span></span>


```VB
SWbemRefreshableItem.ObjectSet As Object
```



## <a name="property-value"></a><span data-ttu-id="38454-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="38454-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="38454-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38454-110">Remarks</span></span>

<span data-ttu-id="38454-111">Esta propiedad es **null** a menos que [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) sea **true**.</span><span class="sxs-lookup"><span data-stu-id="38454-111">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="38454-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38454-112">Requirements</span></span>



| <span data-ttu-id="38454-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="38454-113">Requirement</span></span> | <span data-ttu-id="38454-114">Value</span><span class="sxs-lookup"><span data-stu-id="38454-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38454-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38454-115">Minimum supported client</span></span><br/> | <span data-ttu-id="38454-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38454-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38454-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38454-117">Minimum supported server</span></span><br/> | <span data-ttu-id="38454-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38454-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38454-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38454-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="38454-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="38454-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="38454-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="38454-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="38454-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="38454-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="38454-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38454-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38454-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38454-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="38454-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="38454-125">CLSID</span></span><br/>                    | <span data-ttu-id="38454-126">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="38454-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="38454-127">IID</span><span class="sxs-lookup"><span data-stu-id="38454-127">IID</span></span><br/>                      | <span data-ttu-id="38454-128">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="38454-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="38454-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="38454-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38454-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="38454-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="38454-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="38454-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




