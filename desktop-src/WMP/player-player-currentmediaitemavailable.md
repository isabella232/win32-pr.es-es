---
title: Evento Player. CurrentMediaItemAvailable
description: El evento CurrentMediaItemAvailable se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible. | Evento Player. CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Media Player CurrentMediaItemAvailable de eventos de Windows
- Evento CurrentMediaItemAvailable de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CurrentMediaItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708677"
---
# <a name="playercurrentmediaitemavailable-event"></a><span data-ttu-id="b88a2-107">Evento Player. CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="b88a2-107">Player.CurrentMediaItemAvailable event</span></span>

<span data-ttu-id="b88a2-108">El evento **CurrentMediaItemAvailable** se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible.</span><span class="sxs-lookup"><span data-stu-id="b88a2-108">The **CurrentMediaItemAvailable** event occurs when a graphic metadata item in the current media item becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88a2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b88a2-109">Syntax</span></span>


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="b88a2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b88a2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88a2-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="b88a2-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="b88a2-112">**Cadena** que contiene el nombre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="b88a2-112">**String** containing the name of the current media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88a2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b88a2-113">Return value</span></span>

<span data-ttu-id="b88a2-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="b88a2-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b88a2-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b88a2-115">Remarks</span></span>

<span data-ttu-id="b88a2-116">Dado que la reproducción puede comenzar antes de que un elemento multimedia se descargue por completo, es posible que los gráficos de metadatos contenidos en el elemento multimedia (por ejemplo, la portada del álbum) no estén disponibles cuando comience a reproducirse.</span><span class="sxs-lookup"><span data-stu-id="b88a2-116">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="b88a2-117">Este evento le avisa cuando termina la descarga de un elemento de gráfico de metadatos.</span><span class="sxs-lookup"><span data-stu-id="b88a2-117">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="b88a2-118">A continuación, puede recuperar el objeto **multimedia** pasando el valor de *bstrItemName* a *MediaCollection*. método **getByName** , después del cual se puede tener acceso al elemento gráfico de metadatos mediante el uso de *medios*. **getItemInfoByType** y especificando **WM/imagen** para el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="b88a2-118">You can then retrieve the **Media** object by passing the value of *bstrItemName* to the *MediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *Media*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

<span data-ttu-id="b88a2-119">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="b88a2-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="b88a2-120">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b88a2-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="b88a2-121">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="b88a2-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b88a2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b88a2-122">Requirements</span></span>



| <span data-ttu-id="b88a2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b88a2-123">Requirement</span></span> | <span data-ttu-id="b88a2-124">Value</span><span class="sxs-lookup"><span data-stu-id="b88a2-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b88a2-125">Versión</span><span class="sxs-lookup"><span data-stu-id="b88a2-125">Version</span></span><br/> | <span data-ttu-id="b88a2-126">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b88a2-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b88a2-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b88a2-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="b88a2-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b88a2-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b88a2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b88a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88a2-130">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="b88a2-130">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b88a2-131">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b88a2-131">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="b88a2-132">**MediaCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="b88a2-132">**MediaCollection.getByName**</span></span>](mediacollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="b88a2-133">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="b88a2-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





