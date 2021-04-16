---
title: MediaCollection. getByAttributeAndMediaType, método
description: El método getByAttributeAndMediaType recupera un objeto de lista de reproducción que contiene objetos multimedia que tienen el atributo y el tipo de medio especificados.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- método getByAttributeAndMediaType de Windows Media Player
- método getByAttributeAndMediaType de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649957"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a><span data-ttu-id="0f140-106">MediaCollection. getByAttributeAndMediaType, método</span><span class="sxs-lookup"><span data-stu-id="0f140-106">MediaCollection.getByAttributeAndMediaType method</span></span>

<span data-ttu-id="0f140-107">El método **getByAttributeAndMediaType** recupera un objeto de **lista de reproducción** que contiene objetos **multimedia** que tienen el atributo y el tipo de medio especificados.</span><span class="sxs-lookup"><span data-stu-id="0f140-107">The **getByAttributeAndMediaType** method retrieves a **Playlist** object containing **Media** objects having the specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f140-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f140-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="0f140-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f140-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f140-110">*atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0f140-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f140-111">**Cadena** que contiene el atributo.</span><span class="sxs-lookup"><span data-stu-id="0f140-111">**String** containing the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="0f140-112">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0f140-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f140-113">**Cadena** que contiene el valor.</span><span class="sxs-lookup"><span data-stu-id="0f140-113">**String** containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="0f140-114">*mediaType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f140-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f140-115">**Cadena** que contiene el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="0f140-115">**String** containing the media type.</span></span> <span data-ttu-id="0f140-116">Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".</span><span class="sxs-lookup"><span data-stu-id="0f140-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f140-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f140-117">Return value</span></span>

<span data-ttu-id="0f140-118">Este método devuelve un objeto de **lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="0f140-118">This method returns a **Playlist** object</span></span>

## <a name="requirements"></a><span data-ttu-id="0f140-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f140-119">Requirements</span></span>



| <span data-ttu-id="0f140-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f140-120">Requirement</span></span> | <span data-ttu-id="0f140-121">Value</span><span class="sxs-lookup"><span data-stu-id="0f140-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f140-122">Versión</span><span class="sxs-lookup"><span data-stu-id="0f140-122">Version</span></span><br/> | <span data-ttu-id="0f140-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0f140-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="0f140-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f140-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f140-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f140-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f140-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f140-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f140-127">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="0f140-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="0f140-128">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="0f140-128">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="0f140-129">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="0f140-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





