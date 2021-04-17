---
title: Evento StringCollectionChange del objeto AxWindowsMediaPlayer
description: El evento StringCollectionChange se produce cuando cambia una colección de cadenas. | Evento StringCollectionChange del objeto AxWindowsMediaPlayer
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Evento StringCollectionChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698502"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7b99f-105">Evento StringCollectionChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7b99f-105">StringCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7b99f-106">El evento StringCollectionChange se produce cuando cambia una colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="7b99f-106">The StringCollectionChange event occurs when a string collection changes.</span></span>

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="7b99f-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="7b99f-107">Event Data</span></span>

<span data-ttu-id="7b99f-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="7b99f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEventHandler**.</span></span> <span data-ttu-id="7b99f-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="7b99f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="7b99f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b99f-110">Property</span></span>              | <span data-ttu-id="7b99f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b99f-111">Description</span></span>                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b99f-112">pdispStringCollection</span><span class="sxs-lookup"><span data-stu-id="7b99f-112">pdispStringCollection</span></span> | <span data-ttu-id="7b99f-113">Elemento de colección de cadenas System. ObjectThe que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b99f-113">System.ObjectThe string collection item that changed.</span></span> <span data-ttu-id="7b99f-114">Puede convertirlo en una interfaz IWMPStringCollection para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="7b99f-114">You can cast this to an IWMPStringCollection interface to access it.</span></span><br/> |
| <span data-ttu-id="7b99f-115">lCollectionIndex</span><span class="sxs-lookup"><span data-stu-id="7b99f-115">lCollectionIndex</span></span>      | <span data-ttu-id="7b99f-116">Índice System. Int32el del elemento de colección de cadenas que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b99f-116">System.Int32The index of the string collection item that changed.</span></span><br/>                                                          |
| <span data-ttu-id="7b99f-117">cambiar</span><span class="sxs-lookup"><span data-stu-id="7b99f-117">change</span></span>                | <span data-ttu-id="7b99f-118">Valor de enumeración WMPLib. WMPStringCollectionChangeEventTypeAn que indica el tipo de cambio que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="7b99f-118">WMPLib.WMPStringCollectionChangeEventTypeAn enumeration value indicating the type of change that occurred.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="7b99f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b99f-119">Requirements</span></span>



| <span data-ttu-id="7b99f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b99f-120">Requirement</span></span> | <span data-ttu-id="7b99f-121">Value</span><span class="sxs-lookup"><span data-stu-id="7b99f-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b99f-122">Versión</span><span class="sxs-lookup"><span data-stu-id="7b99f-122">Version</span></span><br/>   | <span data-ttu-id="7b99f-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="7b99f-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7b99f-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7b99f-124">Namespace</span></span><br/> | <span data-ttu-id="7b99f-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7b99f-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7b99f-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="7b99f-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7b99f-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7b99f-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b99f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b99f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b99f-129">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7b99f-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7b99f-130">**Interfaz IWMPStringCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7b99f-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7b99f-131">**WMPStringCollectionChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="7b99f-131">**WMPStringCollectionChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





