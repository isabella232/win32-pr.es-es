---
title: MediaCollection. getPlaylistByQuery, método
description: El método getPlaylistByQuery recupera un objeto de lista de reproducción que contiene objetos multimedia que coinciden con las condiciones de la consulta.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- método getPlaylistByQuery de Windows Media Player
- método getPlaylistByQuery de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getPlaylistByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690297"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a><span data-ttu-id="841e9-106">MediaCollection. getPlaylistByQuery, método</span><span class="sxs-lookup"><span data-stu-id="841e9-106">MediaCollection.getPlaylistByQuery method</span></span>

<span data-ttu-id="841e9-107">El método **getPlaylistByQuery** recupera un objeto de **lista de reproducción** que contiene objetos **multimedia** que coinciden con las condiciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="841e9-107">The **getPlaylistByQuery** method retrieves a **Playlist** object containing **Media** objects that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="841e9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="841e9-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="841e9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="841e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="841e9-110">*consulta* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="841e9-110">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="841e9-111">Objeto de **consulta** que define las condiciones utilizadas para crear la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="841e9-111">**Query** object that defines the conditions used to create the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="841e9-112">*mediaType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="841e9-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="841e9-113">**Cadena** que contiene el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="841e9-113">**String** containing the media type.</span></span> <span data-ttu-id="841e9-114">Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".</span><span class="sxs-lookup"><span data-stu-id="841e9-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="841e9-115">*sortAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="841e9-115">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="841e9-116">**Cadena** que contiene el nombre del atributo utilizado para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="841e9-116">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="841e9-117">Una cadena vacía ("") significa que no se aplica ninguna ordenación.</span><span class="sxs-lookup"><span data-stu-id="841e9-117">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="841e9-118">*sortAscending* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="841e9-118">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="841e9-119">**Boolean**, true, que indica que la lista de reproducción debe estar ordenada de forma ascendente.</span><span class="sxs-lookup"><span data-stu-id="841e9-119">**Boolean**, true indicating that the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="841e9-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="841e9-120">Return value</span></span>

<span data-ttu-id="841e9-121">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="841e9-121">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="841e9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="841e9-122">Remarks</span></span>

<span data-ttu-id="841e9-123">Las consultas compuestas que usan la **consulta** no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="841e9-123">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="841e9-124">Cuando la consulta compuesta especificada por el parámetro de *consulta* contiene una condición generada en el atributo **mediatype** , se omite esa condición.</span><span class="sxs-lookup"><span data-stu-id="841e9-124">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="841e9-125">Siempre se usa el valor del parámetro *mediaType* .</span><span class="sxs-lookup"><span data-stu-id="841e9-125">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="841e9-126">Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *mediatype* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="841e9-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="841e9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="841e9-127">Requirements</span></span>



| <span data-ttu-id="841e9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="841e9-128">Requirement</span></span> | <span data-ttu-id="841e9-129">Value</span><span class="sxs-lookup"><span data-stu-id="841e9-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="841e9-130">Versión</span><span class="sxs-lookup"><span data-stu-id="841e9-130">Version</span></span><br/> | <span data-ttu-id="841e9-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="841e9-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="841e9-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="841e9-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="841e9-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="841e9-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="841e9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="841e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841e9-135">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="841e9-135">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="841e9-136">**MediaType (atributo)**</span><span class="sxs-lookup"><span data-stu-id="841e9-136">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="841e9-137">**Query (objeto)**</span><span class="sxs-lookup"><span data-stu-id="841e9-137">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





