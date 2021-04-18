---
title: DownloadCollection. Item (método)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método Item recupera un objeto de descarga pendiente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase DownloadCollection
- Clase DownloadCollection Windows Media Player, método Item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700086"
---
# <a name="downloadcollectionitem-method"></a><span data-ttu-id="e5f35-108">DownloadCollection. Item (método)</span><span class="sxs-lookup"><span data-stu-id="e5f35-108">DownloadCollection.item method</span></span>

> [!Note]  
> <span data-ttu-id="e5f35-109">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="e5f35-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e5f35-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e5f35-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e5f35-111">El método **Item** recupera un objeto de descarga pendiente.</span><span class="sxs-lookup"><span data-stu-id="e5f35-111">The **item** method retrieves a pending download object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f35-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5f35-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a><span data-ttu-id="e5f35-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5f35-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5f35-114">*Itemid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e5f35-114">*itemId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f35-115">**Número** (**largo**) que especifica el índice del **DownloadItem** que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e5f35-115">**Number** (**long**) specifying the index of the **DownloadItem** to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5f35-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5f35-116">Return value</span></span>

<span data-ttu-id="e5f35-117">Este método devuelve un objeto **DownloadItem** .</span><span class="sxs-lookup"><span data-stu-id="e5f35-117">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5f35-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5f35-118">Remarks</span></span>

<span data-ttu-id="e5f35-119">El valor de *itemID* está basado en cero.</span><span class="sxs-lookup"><span data-stu-id="e5f35-119">The *itemID* value is zero-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5f35-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5f35-120">Requirements</span></span>



| <span data-ttu-id="e5f35-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5f35-121">Requirement</span></span> | <span data-ttu-id="e5f35-122">Value</span><span class="sxs-lookup"><span data-stu-id="e5f35-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f35-123">Versión</span><span class="sxs-lookup"><span data-stu-id="e5f35-123">Version</span></span><br/> | <span data-ttu-id="e5f35-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e5f35-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="e5f35-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e5f35-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5f35-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5f35-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5f35-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5f35-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5f35-128">**Objeto DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="e5f35-128">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="e5f35-129">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="e5f35-129">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





