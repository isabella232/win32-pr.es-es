---
description: La propiedad SWbemRefreshableItem. Object representa una instancia de SWbemObject única que se actualiza. El elemento está contenido en un objeto SWbemRefresher. Instancia de SWbemObject que se actualiza. El elemento está contenido en un objeto SWbemRefresher.
ms.assetid: 91a693c0-cde4-4cf6-b85a-662cfd0333e9
ms.tgt_platform: multiple
title: Propiedad SWbemRefreshableItem. Object (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Object
- ISWbemRefreshableItem.Object
- ISWbemRefreshableItem.get_Object
- ISWbemRefreshableItem.put_Object
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b8456422088e9914562b87b2b114629bd80003c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003358"
---
# <a name="swbemrefreshableitemobject-property"></a><span data-ttu-id="82900-105">Propiedad SWbemRefreshableItem. Object</span><span class="sxs-lookup"><span data-stu-id="82900-105">SWbemRefreshableItem.Object property</span></span>

<span data-ttu-id="82900-106">La propiedad **SWbemRefreshableItem. Object** representa una instancia de [**SWbemObject**](swbemobject.md) única que se actualiza.</span><span class="sxs-lookup"><span data-stu-id="82900-106">The **SWbemRefreshableItem.Object** property represents a single [**SWbemObject**](swbemobject.md) instance that is refreshed.</span></span> <span data-ttu-id="82900-107">El elemento está contenido en un objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="82900-107">The item is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="82900-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="82900-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="82900-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="82900-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="82900-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82900-110">Syntax</span></span>


```VB
SWbemRefreshableItem.Object As Object
```



## <a name="property-value"></a><span data-ttu-id="82900-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="82900-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="82900-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82900-112">Remarks</span></span>

<span data-ttu-id="82900-113">Esta propiedad es **null** a menos que [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) sea **false**.</span><span class="sxs-lookup"><span data-stu-id="82900-113">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="82900-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82900-114">Requirements</span></span>



| <span data-ttu-id="82900-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="82900-115">Requirement</span></span> | <span data-ttu-id="82900-116">Value</span><span class="sxs-lookup"><span data-stu-id="82900-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82900-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82900-117">Minimum supported client</span></span><br/> | <span data-ttu-id="82900-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82900-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82900-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82900-119">Minimum supported server</span></span><br/> | <span data-ttu-id="82900-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82900-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82900-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82900-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="82900-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="82900-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="82900-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="82900-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="82900-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="82900-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="82900-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82900-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82900-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82900-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="82900-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="82900-127">CLSID</span></span><br/>                    | <span data-ttu-id="82900-128">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="82900-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="82900-129">IID</span><span class="sxs-lookup"><span data-stu-id="82900-129">IID</span></span><br/>                      | <span data-ttu-id="82900-130">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="82900-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="82900-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="82900-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82900-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="82900-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="82900-133">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="82900-133">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




