---
title: DownloadCollection. removeItem (método)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método removeItem quita un elemento de descarga de una colección de descargas.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- método removeItem Media Player Windows
- método removeItem Windows Media Player, clase DownloadCollection
- Clase DownloadCollection Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700348"
---
# <a name="downloadcollectionremoveitem-method"></a><span data-ttu-id="5b3d1-108">DownloadCollection. removeItem (método)</span><span class="sxs-lookup"><span data-stu-id="5b3d1-108">DownloadCollection.removeItem method</span></span>

> [!Note]  
> <span data-ttu-id="5b3d1-109">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="5b3d1-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5b3d1-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="5b3d1-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5b3d1-111">El método **RemoveItem** quita un elemento de descarga de una colección de descargas.</span><span class="sxs-lookup"><span data-stu-id="5b3d1-111">The **removeItem** method removes a download item from a download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3d1-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b3d1-112">Syntax</span></span>


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a><span data-ttu-id="5b3d1-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b3d1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b3d1-114">*itemID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b3d1-114">*itemID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3d1-115">**Número** (**largo**) que especifica el índice del **DownloadItem** que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="5b3d1-115">**Number** (**long**) specifying the index of the **DownloadItem** to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b3d1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b3d1-116">Return value</span></span>

<span data-ttu-id="5b3d1-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5b3d1-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3d1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b3d1-118">Remarks</span></span>

<span data-ttu-id="5b3d1-119">Si la descarga representada por *itemID* está en curso, este método cancela la descarga.</span><span class="sxs-lookup"><span data-stu-id="5b3d1-119">If the download represented by *itemID* is in progress, this method cancels the download.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3d1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b3d1-120">Requirements</span></span>



| <span data-ttu-id="5b3d1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b3d1-121">Requirement</span></span> | <span data-ttu-id="5b3d1-122">Value</span><span class="sxs-lookup"><span data-stu-id="5b3d1-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3d1-123">Versión</span><span class="sxs-lookup"><span data-stu-id="5b3d1-123">Version</span></span><br/> | <span data-ttu-id="5b3d1-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="5b3d1-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="5b3d1-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b3d1-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b3d1-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b3d1-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b3d1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b3d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3d1-128">**DownloadCollection. Item**</span><span class="sxs-lookup"><span data-stu-id="5b3d1-128">**DownloadCollection.item**</span></span>](downloadcollection-item.md)
</dt> <dt>

[<span data-ttu-id="5b3d1-129">**Objeto DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="5b3d1-129">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





