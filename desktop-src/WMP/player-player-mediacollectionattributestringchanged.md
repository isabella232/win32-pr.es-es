---
title: Evento Player. MediaCollectionAttributeStringChanged
description: El evento MediaCollectionAttributeStringChanged se produce cuando se cambia un valor de atributo en la biblioteca. | Evento Player. MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Media Player MediaCollectionAttributeStringChanged de eventos de Windows
- Evento MediaCollectionAttributeStringChanged de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaCollectionAttributeStringChanged
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708304"
---
# <a name="playermediacollectionattributestringchanged-event"></a><span data-ttu-id="62dcb-107">Evento Player. MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="62dcb-107">Player.MediaCollectionAttributeStringChanged event</span></span>

<span data-ttu-id="62dcb-108">El evento **MediaCollectionAttributeStringChanged** se produce cuando se cambia un valor de atributo en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="62dcb-108">The **MediaCollectionAttributeStringChanged** event occurs when an attribute value in the library is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="62dcb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62dcb-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="62dcb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62dcb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62dcb-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="62dcb-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="62dcb-112">**Cadena** que especifica el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="62dcb-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="62dcb-113">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="62dcb-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="62dcb-114">*bstrOldAttribVal*</span><span class="sxs-lookup"><span data-stu-id="62dcb-114">*bstrOldAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="62dcb-115">**Cadena** que especifica el valor anterior del atributo.</span><span class="sxs-lookup"><span data-stu-id="62dcb-115">**String** specifying the old value of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="62dcb-116">*bstrNewAttribVal*</span><span class="sxs-lookup"><span data-stu-id="62dcb-116">*bstrNewAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="62dcb-117">**Cadena** que especifica el nuevo valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="62dcb-117">**String** specifying the new value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62dcb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62dcb-118">Return value</span></span>

<span data-ttu-id="62dcb-119">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="62dcb-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62dcb-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62dcb-120">Remarks</span></span>

<span data-ttu-id="62dcb-121">Cuando un usuario modifica los metadatos de la biblioteca, el objeto **MediaCollection** se actualiza y este evento se desencadena para cada atributo modificado.</span><span class="sxs-lookup"><span data-stu-id="62dcb-121">When a user modifies library metadata, the **MediaCollection** object is updated and this event fires for each attribute changed.</span></span>

<span data-ttu-id="62dcb-122">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="62dcb-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="62dcb-123">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="62dcb-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="62dcb-124">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="62dcb-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="62dcb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62dcb-125">Requirements</span></span>



| <span data-ttu-id="62dcb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="62dcb-126">Requirement</span></span> | <span data-ttu-id="62dcb-127">Value</span><span class="sxs-lookup"><span data-stu-id="62dcb-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62dcb-128">Versión</span><span class="sxs-lookup"><span data-stu-id="62dcb-128">Version</span></span><br/> | <span data-ttu-id="62dcb-129">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="62dcb-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="62dcb-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62dcb-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="62dcb-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62dcb-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62dcb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="62dcb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62dcb-133">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="62dcb-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="62dcb-134">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="62dcb-134">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="62dcb-135">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="62dcb-135">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





