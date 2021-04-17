---
title: Evento Player. MediaCollectionAttributeStringRemoved
description: El evento MediaCollectionAttributeStringRemoved se produce cuando se quita un valor de atributo de la biblioteca. | Evento Player. MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Media Player MediaCollectionAttributeStringRemoved de eventos de Windows
- Evento MediaCollectionAttributeStringRemoved de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaCollectionAttributeStringRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708164"
---
# <a name="playermediacollectionattributestringremoved-event"></a><span data-ttu-id="88648-107">Evento Player. MediaCollectionAttributeStringRemoved</span><span class="sxs-lookup"><span data-stu-id="88648-107">Player.MediaCollectionAttributeStringRemoved event</span></span>

<span data-ttu-id="88648-108">El evento **MediaCollectionAttributeStringRemoved** se produce cuando se quita un valor de atributo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="88648-108">The **MediaCollectionAttributeStringRemoved** event occurs when an attribute value is removed from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="88648-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88648-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="88648-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88648-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88648-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="88648-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="88648-112">**Cadena** que especifica el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="88648-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="88648-113">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="88648-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="88648-114">*bstrAttribVal*</span><span class="sxs-lookup"><span data-stu-id="88648-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="88648-115">**Cadena** que especifica el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="88648-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88648-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88648-116">Return value</span></span>

<span data-ttu-id="88648-117">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="88648-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88648-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88648-118">Remarks</span></span>

<span data-ttu-id="88648-119">Cuando se quita un elemento multimedia de la biblioteca, sus metadatos se quitan del objeto **MediaCollection** y este evento se desencadena para cada atributo que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="88648-119">When a media item is removed from the library, its metadata is removed from the **MediaCollection** object and this event is fired for each attribute removed.</span></span>

<span data-ttu-id="88648-120">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="88648-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="88648-121">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="88648-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="88648-122">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="88648-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="88648-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88648-123">Requirements</span></span>



| <span data-ttu-id="88648-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="88648-124">Requirement</span></span> | <span data-ttu-id="88648-125">Value</span><span class="sxs-lookup"><span data-stu-id="88648-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88648-126">Versión</span><span class="sxs-lookup"><span data-stu-id="88648-126">Version</span></span><br/> | <span data-ttu-id="88648-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="88648-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="88648-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88648-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="88648-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88648-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88648-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="88648-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88648-131">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="88648-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="88648-132">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="88648-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="88648-133">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="88648-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





