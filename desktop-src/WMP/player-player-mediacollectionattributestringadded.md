---
title: Evento Player. MediaCollectionAttributeStringAdded
description: El evento MediaCollectionAttributeStringAdded se produce cuando se agrega un valor de atributo a la biblioteca. | Evento Player. MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Media Player MediaCollectionAttributeStringAdded de eventos de Windows
- Evento MediaCollectionAttributeStringAdded de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaCollectionAttributeStringAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709134"
---
# <a name="playermediacollectionattributestringadded-event"></a><span data-ttu-id="60f35-107">Evento Player. MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="60f35-107">Player.MediaCollectionAttributeStringAdded event</span></span>

<span data-ttu-id="60f35-108">El evento **MediaCollectionAttributeStringAdded** se produce cuando se agrega un valor de atributo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="60f35-108">The **MediaCollectionAttributeStringAdded** event occurs when an attribute value is added to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f35-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60f35-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="60f35-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60f35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f35-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="60f35-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="60f35-112">**Cadena** que especifica el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="60f35-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="60f35-113">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="60f35-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="60f35-114">*bstrAttribVal*</span><span class="sxs-lookup"><span data-stu-id="60f35-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="60f35-115">**Cadena** que especifica el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="60f35-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f35-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60f35-116">Return value</span></span>

<span data-ttu-id="60f35-117">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="60f35-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60f35-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60f35-118">Remarks</span></span>

<span data-ttu-id="60f35-119">Cuando se agrega un elemento multimedia a la biblioteca, sus metadatos se agregan al objeto **MediaCollection** y este evento se desencadena para cada atributo agregado.</span><span class="sxs-lookup"><span data-stu-id="60f35-119">When a media item is added to the library its metadata is added to the **MediaCollection** object and this event is fired for each attribute added.</span></span>

<span data-ttu-id="60f35-120">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="60f35-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="60f35-121">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="60f35-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="60f35-122">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="60f35-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f35-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60f35-123">Requirements</span></span>



| <span data-ttu-id="60f35-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="60f35-124">Requirement</span></span> | <span data-ttu-id="60f35-125">Value</span><span class="sxs-lookup"><span data-stu-id="60f35-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60f35-126">Versión</span><span class="sxs-lookup"><span data-stu-id="60f35-126">Version</span></span><br/> | <span data-ttu-id="60f35-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="60f35-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="60f35-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60f35-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="60f35-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60f35-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60f35-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="60f35-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f35-131">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="60f35-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="60f35-132">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="60f35-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="60f35-133">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="60f35-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





