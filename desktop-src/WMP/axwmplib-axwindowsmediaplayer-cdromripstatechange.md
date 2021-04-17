---
title: Evento CdromRipStateChange del objeto AxWindowsMediaPlayer
description: El evento CdromRipStateChange se produce cuando cambia el estado de una operación de copia desde CD.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Evento CdromRipStateChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698477"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="605f1-104">Evento CdromRipStateChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="605f1-104">CdromRipStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="605f1-105">El evento CdromRipStateChange se produce cuando cambia el estado de una operación de copia desde CD.</span><span class="sxs-lookup"><span data-stu-id="605f1-105">The CdromRipStateChange event occurs when a CD ripping operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a><span data-ttu-id="605f1-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="605f1-106">Event Data</span></span>

<span data-ttu-id="605f1-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="605f1-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEventHandler**.</span></span> <span data-ttu-id="605f1-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="605f1-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="605f1-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="605f1-109">Property</span></span>  | <span data-ttu-id="605f1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="605f1-110">Description</span></span>                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605f1-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="605f1-111">pCdromRip</span></span> | <span data-ttu-id="605f1-112">Interfaz WMPLib. IWMPCdromRipThe que representa la operación de copia desde CD que provocó el error.</span><span class="sxs-lookup"><span data-stu-id="605f1-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/> |
| <span data-ttu-id="605f1-113">wmprs</span><span class="sxs-lookup"><span data-stu-id="605f1-113">wmprs</span></span>     | <span data-ttu-id="605f1-114">Valor de enumeración WMPLib. WMPRipStateThe que indica el nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="605f1-114">WMPLib.WMPRipStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="605f1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="605f1-115">Requirements</span></span>



| <span data-ttu-id="605f1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="605f1-116">Requirement</span></span> | <span data-ttu-id="605f1-117">Value</span><span class="sxs-lookup"><span data-stu-id="605f1-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605f1-118">Versión</span><span class="sxs-lookup"><span data-stu-id="605f1-118">Version</span></span><br/>   | <span data-ttu-id="605f1-119">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="605f1-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="605f1-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="605f1-120">Namespace</span></span><br/> | <span data-ttu-id="605f1-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="605f1-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="605f1-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="605f1-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="605f1-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="605f1-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605f1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="605f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605f1-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="605f1-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="605f1-126">**Interfaz IWMPCdromRip (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="605f1-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="605f1-127">**WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="605f1-127">**WMPRipState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





