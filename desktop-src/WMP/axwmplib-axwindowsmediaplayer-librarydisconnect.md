---
title: Evento LibraryDisconnect del objeto AxWindowsMediaPlayer
description: El evento LibraryDisconnect se produce cuando una biblioteca ya no está disponible.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Evento LibraryDisconnect del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700161"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="0da00-104">Evento LibraryDisconnect del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="0da00-104">LibraryDisconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="0da00-105">El evento LibraryDisconnect se produce cuando una biblioteca ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="0da00-105">The LibraryDisconnect event occurs when a library is no longer available.</span></span>

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a><span data-ttu-id="0da00-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="0da00-106">Event Data</span></span>

<span data-ttu-id="0da00-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="0da00-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEventHandler**.</span></span> <span data-ttu-id="0da00-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="0da00-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="0da00-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0da00-109">Property</span></span> | <span data-ttu-id="0da00-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0da00-110">Description</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0da00-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="0da00-111">pLibrary</span></span> | <span data-ttu-id="0da00-112">**WMPLib. IWMPLibrary** La interfaz que representa la biblioteca que se ha desconectado.</span><span class="sxs-lookup"><span data-stu-id="0da00-112">**WMPLib.IWMPLibrary** The interface that represents the library that disconnected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0da00-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0da00-113">Remarks</span></span>

<span data-ttu-id="0da00-114">Este evento no se produce para la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="0da00-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="0da00-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0da00-115">Requirements</span></span>



| <span data-ttu-id="0da00-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0da00-116">Requirement</span></span> | <span data-ttu-id="0da00-117">Value</span><span class="sxs-lookup"><span data-stu-id="0da00-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0da00-118">Versión</span><span class="sxs-lookup"><span data-stu-id="0da00-118">Version</span></span><br/>   | <span data-ttu-id="0da00-119">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="0da00-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="0da00-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0da00-120">Namespace</span></span><br/> | <span data-ttu-id="0da00-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0da00-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0da00-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="0da00-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0da00-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0da00-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da00-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0da00-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da00-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="0da00-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0da00-126">**Interfaz IWMPLibrary (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="0da00-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





