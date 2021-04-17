---
title: Evento CdromRipMediaError del objeto AxWindowsMediaPlayer
description: El evento CdromRipMediaError tiene lugar cuando se produce un error durante la copia de una pista individual desde un CD.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Evento CdromRipMediaError del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698479"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="dc3a1-104">Evento CdromRipMediaError del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="dc3a1-104">CdromRipMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="dc3a1-105">El evento CdromRipMediaError tiene lugar cuando se produce un error durante la copia de una pista individual desde un CD.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-105">The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.</span></span>

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a><span data-ttu-id="dc3a1-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="dc3a1-106">Event Data</span></span>

<span data-ttu-id="dc3a1-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEventHandler**.</span></span> <span data-ttu-id="dc3a1-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="dc3a1-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc3a1-109">Property</span></span>  | <span data-ttu-id="dc3a1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc3a1-110">Description</span></span>                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc3a1-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="dc3a1-111">pCdromRip</span></span> | <span data-ttu-id="dc3a1-112">Interfaz WMPLib. IWMPCdromRipThe que representa la operación de copia desde CD que provocó el error.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/>                |
| <span data-ttu-id="dc3a1-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="dc3a1-113">pMedia</span></span>    | <span data-ttu-id="dc3a1-114">Elemento multimedia System. ObjectThe que generó el error.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="dc3a1-115">Puede convertirlo en una interfaz IWMPMedia para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="dc3a1-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc3a1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc3a1-116">Requirements</span></span>



| <span data-ttu-id="dc3a1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc3a1-117">Requirement</span></span> | <span data-ttu-id="dc3a1-118">Value</span><span class="sxs-lookup"><span data-stu-id="dc3a1-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc3a1-119">Versión</span><span class="sxs-lookup"><span data-stu-id="dc3a1-119">Version</span></span><br/>   | <span data-ttu-id="dc3a1-120">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="dc3a1-120">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="dc3a1-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc3a1-121">Namespace</span></span><br/> | <span data-ttu-id="dc3a1-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="dc3a1-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="dc3a1-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="dc3a1-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dc3a1-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dc3a1-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc3a1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc3a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc3a1-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dc3a1-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc3a1-127">**Interfaz IWMPCdromRip (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dc3a1-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc3a1-128">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dc3a1-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





