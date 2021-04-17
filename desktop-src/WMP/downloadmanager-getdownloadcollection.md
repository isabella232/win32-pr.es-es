---
title: DownloadManager. getDownloadCollection, método
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método getDownloadCollection recupera la colección de descarga especificada.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- método getDownloadCollection de Windows Media Player
- método getDownloadCollection de Windows Media Player, clase DownloadManager
- Clase DownloadManager Windows Media Player, método getDownloadCollection
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699417"
---
# <a name="downloadmanagergetdownloadcollection-method"></a><span data-ttu-id="3202b-108">DownloadManager. getDownloadCollection, método</span><span class="sxs-lookup"><span data-stu-id="3202b-108">DownloadManager.getDownloadCollection method</span></span>

> [!Note]  
> <span data-ttu-id="3202b-109">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="3202b-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3202b-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="3202b-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3202b-111">El método **getDownloadCollection** recupera la colección de descarga especificada.</span><span class="sxs-lookup"><span data-stu-id="3202b-111">The **getDownloadCollection** method retrieves the specified download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3202b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3202b-112">Syntax</span></span>


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a><span data-ttu-id="3202b-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3202b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3202b-114">*collectionId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3202b-114">*collectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3202b-115">**Número** (**largo**) que especifica el identificador de la colección de descarga que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3202b-115">**Number** (**long**) specifying the ID of the download collection to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3202b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3202b-116">Return value</span></span>

<span data-ttu-id="3202b-117">Este método devuelve un objeto **DownloadCollection** .</span><span class="sxs-lookup"><span data-stu-id="3202b-117">This method returns a **DownloadCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3202b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3202b-118">Remarks</span></span>

<span data-ttu-id="3202b-119">Primero debe llamar a *Downloadmanager*. **createDownloadCollection** para crear una nueva colección y recuperar su valor de identificador.</span><span class="sxs-lookup"><span data-stu-id="3202b-119">You must first call *DownloadManager*.**createDownloadCollection** to create a new collection and retrieve its ID value.</span></span>

<span data-ttu-id="3202b-120">Una colección de descargas existente puede contener elementos marcados como cancelados.</span><span class="sxs-lookup"><span data-stu-id="3202b-120">An existing download collection may contain items that have been marked as cancelled.</span></span>

<span data-ttu-id="3202b-121">Los elementos de descarga en tiempo real no completados en una sesión anterior no se recuperan como parte de la colección.</span><span class="sxs-lookup"><span data-stu-id="3202b-121">Real-time download items not completed in a prior session are not retrieved as part of the collection.</span></span> <span data-ttu-id="3202b-122">Las descargas en segundo plano que se completaron antes de la sesión actual permanecen en la colección de descargas hasta que se quitan.</span><span class="sxs-lookup"><span data-stu-id="3202b-122">Background downloads that were completed prior to the current session remain in the download collection until removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3202b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3202b-123">Requirements</span></span>



| <span data-ttu-id="3202b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3202b-124">Requirement</span></span> | <span data-ttu-id="3202b-125">Value</span><span class="sxs-lookup"><span data-stu-id="3202b-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3202b-126">Versión</span><span class="sxs-lookup"><span data-stu-id="3202b-126">Version</span></span><br/> | <span data-ttu-id="3202b-127">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3202b-127">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="3202b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3202b-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="3202b-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3202b-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3202b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3202b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3202b-131">**Objeto DownloadManager**</span><span class="sxs-lookup"><span data-stu-id="3202b-131">**DownloadManager Object**</span></span>](downloadmanager-object.md)
</dt> <dt>

[<span data-ttu-id="3202b-132">**DownloadManager. createDownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="3202b-132">**DownloadManager. createDownloadCollection**</span></span>](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="3202b-133">**Objeto DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="3202b-133">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





