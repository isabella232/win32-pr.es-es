---
title: Evento de almacenamiento en búfer del objeto AxWindowsMediaPlayer
description: El evento de almacenamiento en búfer se produce cuando el control de Media Player de Windows comienza o finaliza la descarga o el almacenamiento en búfer. | Evento de almacenamiento en búfer del objeto AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Evento de almacenamiento en búfer del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698486"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e839a-105">Evento de almacenamiento en búfer del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="e839a-105">Buffering Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e839a-106">El evento de almacenamiento en búfer se produce cuando el control de Media Player de Windows comienza o finaliza la descarga o el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="e839a-106">The Buffering event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a><span data-ttu-id="e839a-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="e839a-107">Event Data</span></span>

<span data-ttu-id="e839a-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="e839a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_BufferingEventHandler**.</span></span> <span data-ttu-id="e839a-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="e839a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_BufferingEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="e839a-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e839a-110">Property</span></span> | <span data-ttu-id="e839a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e839a-111">Description</span></span>                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e839a-112">Start</span><span class="sxs-lookup"><span data-stu-id="e839a-112">Start</span></span>    | <span data-ttu-id="e839a-113">System. BooleanSpecifies si el almacenamiento en búfer ha empezado o ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="e839a-113">System.BooleanSpecifies whether buffering has begun or ended.</span></span> <span data-ttu-id="e839a-114">Un valor de True indica que ha empezado; un valor de False indica que ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="e839a-114">A value of true indicates that it has begun; a value of false indicates that it has ended.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e839a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e839a-115">Remarks</span></span>

<span data-ttu-id="e839a-116">Utilice este evento para determinar cuándo se inicia o se detiene el almacenamiento en búfer o la descarga.</span><span class="sxs-lookup"><span data-stu-id="e839a-116">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="e839a-117">Puede usar el mismo bloque de eventos para ambos casos y probar *IWMPNetwork*. **bufferingProgress** y *IWMPNetwork*. **downloadProgress** para determinar si Windows Media Player está almacenando en búfer o descargando contenido actualmente.</span><span class="sxs-lookup"><span data-stu-id="e839a-117">You can use the same event block for both cases and test *IWMPNetwork*.**bufferingProgress** and *IWMPNetwork*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

## <a name="requirements"></a><span data-ttu-id="e839a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e839a-118">Requirements</span></span>



| <span data-ttu-id="e839a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e839a-119">Requirement</span></span> | <span data-ttu-id="e839a-120">Value</span><span class="sxs-lookup"><span data-stu-id="e839a-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e839a-121">Versión</span><span class="sxs-lookup"><span data-stu-id="e839a-121">Version</span></span><br/>   | <span data-ttu-id="e839a-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e839a-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e839a-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e839a-123">Namespace</span></span><br/> | <span data-ttu-id="e839a-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="e839a-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e839a-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="e839a-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e839a-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e839a-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e839a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e839a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e839a-128">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e839a-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e839a-129">**IWMPNetwork. bufferingProgress (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e839a-129">**IWMPNetwork.bufferingProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e839a-130">**IWMPNetwork. downloadProgress (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e839a-130">**IWMPNetwork.downloadProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





