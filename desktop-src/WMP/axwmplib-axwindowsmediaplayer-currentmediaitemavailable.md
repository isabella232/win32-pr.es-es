---
title: Evento CurrentMediaItemAvailable del objeto AxWindowsMediaPlayer
description: El evento CurrentMediaItemAvailable se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible. | Evento CurrentMediaItemAvailable del objeto AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Evento CurrentMediaItemAvailable del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700168"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="5e2a0-105">Evento CurrentMediaItemAvailable del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="5e2a0-105">CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="5e2a0-106">El evento CurrentMediaItemAvailable se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible.</span><span class="sxs-lookup"><span data-stu-id="5e2a0-106">The CurrentMediaItemAvailable event occurs when a graphic metadata item in the current media item becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="5e2a0-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="5e2a0-107">Event Data</span></span>

<span data-ttu-id="5e2a0-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="5e2a0-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEventHandler**.</span></span> <span data-ttu-id="5e2a0-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="5e2a0-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="5e2a0-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5e2a0-110">Property</span></span>     | <span data-ttu-id="5e2a0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e2a0-111">Description</span></span>                                                 |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="5e2a0-112">bstrItemName</span><span class="sxs-lookup"><span data-stu-id="5e2a0-112">bstrItemName</span></span> | <span data-ttu-id="5e2a0-113">System. Stringel nombre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="5e2a0-113">System.StringThe name of the current media item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e2a0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e2a0-114">Remarks</span></span>

<span data-ttu-id="5e2a0-115">Dado que la reproducción puede comenzar antes de que un elemento multimedia se descargue por completo, es posible que los gráficos de metadatos contenidos en el elemento multimedia (por ejemplo, la portada del álbum) no estén disponibles cuando comience a reproducirse.</span><span class="sxs-lookup"><span data-stu-id="5e2a0-115">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="5e2a0-116">Este evento le avisa cuando termina la descarga de un elemento de gráfico de metadatos.</span><span class="sxs-lookup"><span data-stu-id="5e2a0-116">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="5e2a0-117">Después, puede recuperar la interfaz **IWMPMedia** pasando el valor de **bstrItemName** a *IWMPMediaCollection*. método **getByName** , después del cual se puede tener acceso al elemento gráfico de metadatos mediante *IWMPMedia3*. **getItemInfoByType** y especificando **WM/imagen** para el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="5e2a0-117">You can then retrieve the **IWMPMedia** interface by passing the value of **bstrItemName** to the *IWMPMediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *IWMPMedia3*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2a0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e2a0-118">Requirements</span></span>



| <span data-ttu-id="5e2a0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e2a0-119">Requirement</span></span> | <span data-ttu-id="5e2a0-120">Value</span><span class="sxs-lookup"><span data-stu-id="5e2a0-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2a0-121">Versión</span><span class="sxs-lookup"><span data-stu-id="5e2a0-121">Version</span></span><br/>   | <span data-ttu-id="5e2a0-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="5e2a0-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="5e2a0-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e2a0-123">Namespace</span></span><br/> | <span data-ttu-id="5e2a0-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="5e2a0-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5e2a0-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="5e2a0-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5e2a0-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5e2a0-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e2a0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e2a0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2a0-128">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5e2a0-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5e2a0-129">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5e2a0-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5e2a0-130">**IWMPMedia3. getItemInfoByType (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5e2a0-130">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5e2a0-131">**IWMPMediaCollection. getByName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5e2a0-131">**IWMPMediaCollection.getByName (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





