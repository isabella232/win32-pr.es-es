---
title: Evento Player. MediaChange
description: El evento MediaChange se produce cuando cambia un elemento multimedia. | Evento Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Media Player MediaChange de eventos de Windows
- Evento MediaChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaChange
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709135"
---
# <a name="playermediachange-event"></a><span data-ttu-id="0ea90-107">Evento Player. MediaChange</span><span class="sxs-lookup"><span data-stu-id="0ea90-107">Player.MediaChange event</span></span>

<span data-ttu-id="0ea90-108">El evento **MediaChange** se produce cuando cambia un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="0ea90-108">The **MediaChange** event occurs when a media item changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea90-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ea90-109">Syntax</span></span>


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a><span data-ttu-id="0ea90-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ea90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea90-111">*Elemento*</span><span class="sxs-lookup"><span data-stu-id="0ea90-111">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="0ea90-112">Objeto **multimedia** que representa el elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="0ea90-112">**Media** object representing the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea90-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ea90-113">Return value</span></span>

<span data-ttu-id="0ea90-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="0ea90-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea90-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ea90-115">Remarks</span></span>

<span data-ttu-id="0ea90-116">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="0ea90-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="0ea90-117">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0ea90-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="0ea90-118">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="0ea90-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="0ea90-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0ea90-119">Examples</span></span>

<span data-ttu-id="0ea90-120">En el siguiente ejemplo de JScript se usa un elemento HTML DIV, denominado MEDIANAME, para mostrar el nombre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="0ea90-120">The following JScript example uses an HTML DIV element, named MediaName, to display the name of the current media item.</span></span> <span data-ttu-id="0ea90-121">El código actualiza el texto en el DIV con cada aparición del evento **mediaChange** .</span><span class="sxs-lookup"><span data-stu-id="0ea90-121">The code updates the text in the DIV with each occurrence of the **mediaChange** event.</span></span> <span data-ttu-id="0ea90-122">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0ea90-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="0ea90-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ea90-123">Requirements</span></span>



| <span data-ttu-id="0ea90-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ea90-124">Requirement</span></span> | <span data-ttu-id="0ea90-125">Value</span><span class="sxs-lookup"><span data-stu-id="0ea90-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea90-126">Versión</span><span class="sxs-lookup"><span data-stu-id="0ea90-126">Version</span></span><br/> | <span data-ttu-id="0ea90-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0ea90-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0ea90-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ea90-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="0ea90-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ea90-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea90-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ea90-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea90-131">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="0ea90-131">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





