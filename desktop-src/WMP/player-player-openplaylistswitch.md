---
title: Evento Player. OpenPlaylistSwitch
description: El evento OpenPlaylistSwitch se produce cuando comienza a reproducirse un título en un DVD. | Evento Player. OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Media Player OpenPlaylistSwitch de eventos de Windows
- Evento OpenPlaylistSwitch de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento OpenPlaylistSwitch
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708662"
---
# <a name="playeropenplaylistswitch-event"></a><span data-ttu-id="04668-107">Evento Player. OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="04668-107">Player.OpenPlaylistSwitch event</span></span>

<span data-ttu-id="04668-108">El evento **OpenPlaylistSwitch** se produce cuando comienza a reproducirse un título en un DVD.</span><span class="sxs-lookup"><span data-stu-id="04668-108">The **OpenPlaylistSwitch** event occurs when a title on a DVD begins playing.</span></span>

## <a name="syntax"></a><span data-ttu-id="04668-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04668-109">Syntax</span></span>


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a><span data-ttu-id="04668-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04668-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04668-111">*pItem*</span><span class="sxs-lookup"><span data-stu-id="04668-111">*pItem*</span></span> 
</dt> <dd>

<span data-ttu-id="04668-112">Objeto de **lista de reproducción** que representa el título.</span><span class="sxs-lookup"><span data-stu-id="04668-112">**Playlist** object representing the title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04668-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04668-113">Return value</span></span>

<span data-ttu-id="04668-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="04668-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04668-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04668-115">Remarks</span></span>

<span data-ttu-id="04668-116">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="04668-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="04668-117">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="04668-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="04668-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04668-118">Requirements</span></span>



| <span data-ttu-id="04668-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04668-119">Requirement</span></span> | <span data-ttu-id="04668-120">Value</span><span class="sxs-lookup"><span data-stu-id="04668-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04668-121">Versión</span><span class="sxs-lookup"><span data-stu-id="04668-121">Version</span></span><br/> | <span data-ttu-id="04668-122">Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="04668-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="04668-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04668-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="04668-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04668-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04668-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="04668-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04668-126">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="04668-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





