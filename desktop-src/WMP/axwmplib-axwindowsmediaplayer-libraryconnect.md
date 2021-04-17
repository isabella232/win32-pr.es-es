---
title: Evento LibraryConnect del objeto AxWindowsMediaPlayer
description: El evento LibraryConnect se produce cuando una biblioteca está disponible.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Evento LibraryConnect del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700163"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3cf3c-104">Evento LibraryConnect del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3cf3c-104">LibraryConnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3cf3c-105">El evento LibraryConnect se produce cuando una biblioteca está disponible.</span><span class="sxs-lookup"><span data-stu-id="3cf3c-105">The LibraryConnect event occurs when a library becomes available.</span></span>

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a><span data-ttu-id="3cf3c-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="3cf3c-106">Event Data</span></span>

<span data-ttu-id="3cf3c-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="3cf3c-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEventHandler**.</span></span> <span data-ttu-id="3cf3c-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="3cf3c-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3cf3c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3cf3c-109">Property</span></span> | <span data-ttu-id="3cf3c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cf3c-110">Description</span></span>                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf3c-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="3cf3c-111">pLibrary</span></span> | <span data-ttu-id="3cf3c-112">**WMPLib. IWMPLibrary** La interfaz que representa la biblioteca que se conectó.</span><span class="sxs-lookup"><span data-stu-id="3cf3c-112">**WMPLib.IWMPLibrary** The interface that represents the library that connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3cf3c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cf3c-113">Remarks</span></span>

<span data-ttu-id="3cf3c-114">Este evento no se produce para la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="3cf3c-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf3c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cf3c-115">Requirements</span></span>



| <span data-ttu-id="3cf3c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cf3c-116">Requirement</span></span> | <span data-ttu-id="3cf3c-117">Value</span><span class="sxs-lookup"><span data-stu-id="3cf3c-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf3c-118">Versión</span><span class="sxs-lookup"><span data-stu-id="3cf3c-118">Version</span></span><br/>   | <span data-ttu-id="3cf3c-119">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="3cf3c-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="3cf3c-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3cf3c-120">Namespace</span></span><br/> | <span data-ttu-id="3cf3c-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3cf3c-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3cf3c-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3cf3c-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3cf3c-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3cf3c-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf3c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cf3c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf3c-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3cf3c-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3cf3c-126">**Interfaz IWMPLibrary (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3cf3c-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





