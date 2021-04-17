---
title: Evento MediaError del objeto AxWindowsMediaPlayer
description: El evento MediaError se produce cuando un objeto multimedia tiene una condición de error.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- Evento MediaError del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700147"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d9aeb-104">Evento MediaError del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d9aeb-104">MediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d9aeb-105">El evento MediaError se produce cuando un objeto multimedia tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="d9aeb-105">The MediaError event occurs when a media object has an error condition.</span></span>

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a><span data-ttu-id="d9aeb-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="d9aeb-106">Event Data</span></span>

<span data-ttu-id="d9aeb-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="d9aeb-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEventHandler**.</span></span> <span data-ttu-id="d9aeb-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="d9aeb-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d9aeb-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9aeb-109">Property</span></span>     | <span data-ttu-id="d9aeb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9aeb-110">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9aeb-111">pMediaObject</span><span class="sxs-lookup"><span data-stu-id="d9aeb-111">pMediaObject</span></span> | <span data-ttu-id="d9aeb-112">System. ObjectObject que tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="d9aeb-112">System.ObjectObject that has an error condition.</span></span> <span data-ttu-id="d9aeb-113">Puede convertirlo en una interfaz IWMPMedia para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="d9aeb-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d9aeb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9aeb-114">Requirements</span></span>



| <span data-ttu-id="d9aeb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9aeb-115">Requirement</span></span> | <span data-ttu-id="d9aeb-116">Value</span><span class="sxs-lookup"><span data-stu-id="d9aeb-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9aeb-117">Versión</span><span class="sxs-lookup"><span data-stu-id="d9aeb-117">Version</span></span><br/>   | <span data-ttu-id="d9aeb-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d9aeb-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d9aeb-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d9aeb-119">Namespace</span></span><br/> | <span data-ttu-id="d9aeb-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d9aeb-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d9aeb-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d9aeb-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d9aeb-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d9aeb-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9aeb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9aeb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9aeb-124">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d9aeb-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d9aeb-125">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d9aeb-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





