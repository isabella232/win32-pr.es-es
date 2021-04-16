---
title: MediaCollection. getStringCollectionByQuery, método
description: El método getStringCollectionByQuery recupera un objeto StringCollection que contiene todas las cadenas que coinciden con las condiciones de la consulta.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- método getStringCollectionByQuery de Windows Media Player
- método getStringCollectionByQuery de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getStringCollectionByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690296"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a><span data-ttu-id="8fe39-106">MediaCollection. getStringCollectionByQuery, método</span><span class="sxs-lookup"><span data-stu-id="8fe39-106">MediaCollection.getStringCollectionByQuery method</span></span>

<span data-ttu-id="8fe39-107">El método **getStringCollectionByQuery** recupera un objeto **StringCollection** que contiene todas las cadenas que coinciden con las condiciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8fe39-107">The **getStringCollectionByQuery** method retrieves a **StringCollection** object containing all strings that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe39-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fe39-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="8fe39-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fe39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe39-110">*atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8fe39-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe39-111">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="8fe39-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="8fe39-112">*consulta* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8fe39-112">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe39-113">Objeto de **consulta** .</span><span class="sxs-lookup"><span data-stu-id="8fe39-113">**Query** object.</span></span>

</dd> <dt>

<span data-ttu-id="8fe39-114">*mediaType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fe39-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe39-115">**Cadena** que contiene el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8fe39-115">**String** containing the media type.</span></span> <span data-ttu-id="8fe39-116">Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".</span><span class="sxs-lookup"><span data-stu-id="8fe39-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="8fe39-117">*sortAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fe39-117">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe39-118">**Cadena** que contiene el nombre del atributo utilizado para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="8fe39-118">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="8fe39-119">Una cadena vacía ("") significa que no se aplica ninguna ordenación.</span><span class="sxs-lookup"><span data-stu-id="8fe39-119">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="8fe39-120">*sortAscending* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fe39-120">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe39-121">**Boolean**, true, que indica que el objeto **StringCollection** debe estar ordenado en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="8fe39-121">**Boolean**, true indicating that the **StringCollection** must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe39-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fe39-122">Return value</span></span>

<span data-ttu-id="8fe39-123">Este método devuelve un objeto **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="8fe39-123">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fe39-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fe39-124">Remarks</span></span>

<span data-ttu-id="8fe39-125">Las consultas compuestas que usan la **consulta** no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8fe39-125">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="8fe39-126">Cuando la consulta compuesta especificada por el parámetro de *consulta* contiene una condición generada en el atributo **mediatype** , se omite esa condición.</span><span class="sxs-lookup"><span data-stu-id="8fe39-126">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="8fe39-127">Siempre se usa el valor del parámetro *mediaType* .</span><span class="sxs-lookup"><span data-stu-id="8fe39-127">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="8fe39-128">Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *mediatype* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8fe39-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe39-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fe39-129">Requirements</span></span>



| <span data-ttu-id="8fe39-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fe39-130">Requirement</span></span> | <span data-ttu-id="8fe39-131">Value</span><span class="sxs-lookup"><span data-stu-id="8fe39-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe39-132">Versión</span><span class="sxs-lookup"><span data-stu-id="8fe39-132">Version</span></span><br/> | <span data-ttu-id="8fe39-133">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8fe39-133">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="8fe39-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8fe39-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="8fe39-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe39-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe39-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fe39-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe39-137">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="8fe39-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="8fe39-138">**MediaType (atributo)**</span><span class="sxs-lookup"><span data-stu-id="8fe39-138">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="8fe39-139">**Query (objeto)**</span><span class="sxs-lookup"><span data-stu-id="8fe39-139">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





