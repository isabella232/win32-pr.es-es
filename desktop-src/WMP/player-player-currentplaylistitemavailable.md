---
title: Evento Player. CurrentPlaylistItemAvailable
description: El evento CurrentPlaylistItemAvailable se produce cuando la lista de reproducción actual está disponible. | Evento Player. CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Media Player CurrentPlaylistItemAvailable de eventos de Windows
- Evento CurrentPlaylistItemAvailable de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CurrentPlaylistItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708925"
---
# <a name="playercurrentplaylistitemavailable-event"></a><span data-ttu-id="b5f49-107">Evento Player. CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="b5f49-107">Player.CurrentPlaylistItemAvailable event</span></span>

<span data-ttu-id="b5f49-108">El evento **CurrentPlaylistItemAvailable** se produce cuando la lista de reproducción actual está disponible.</span><span class="sxs-lookup"><span data-stu-id="b5f49-108">The **CurrentPlaylistItemAvailable** event occurs when the current playlist becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f49-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5f49-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="b5f49-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5f49-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f49-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="b5f49-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f49-112">**Cadena** que contiene el nombre del elemento de lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="b5f49-112">**String** containing the name of the current playlist item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f49-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5f49-113">Return value</span></span>

<span data-ttu-id="b5f49-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="b5f49-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f49-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5f49-115">Remarks</span></span>

<span data-ttu-id="b5f49-116">El nombre de la lista de reproducción actual se puede usar para recuperar el objeto de **lista de reproducción** correspondiente mediante *PlaylistCollection*. método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="b5f49-116">The name of the current playlist can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="b5f49-117">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="b5f49-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="b5f49-118">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b5f49-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="b5f49-119">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="b5f49-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f49-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5f49-120">Requirements</span></span>



| <span data-ttu-id="b5f49-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f49-121">Requirement</span></span> | <span data-ttu-id="b5f49-122">Value</span><span class="sxs-lookup"><span data-stu-id="b5f49-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f49-123">Versión</span><span class="sxs-lookup"><span data-stu-id="b5f49-123">Version</span></span><br/> | <span data-ttu-id="b5f49-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b5f49-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b5f49-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5f49-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5f49-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5f49-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f49-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5f49-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f49-128">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="b5f49-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="b5f49-129">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="b5f49-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="b5f49-130">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="b5f49-130">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





