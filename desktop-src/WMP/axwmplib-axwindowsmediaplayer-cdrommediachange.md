---
title: Evento CdromMediaChange del objeto AxWindowsMediaPlayer
description: El evento CdromMediaChange se produce cuando se inserta o se expulsa un CD o DVD en una unidad de CD o DVD. | Evento CdromMediaChange del objeto AxWindowsMediaPlayer
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Evento CdromMediaChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698481"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="33874-105">Evento CdromMediaChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="33874-105">CdromMediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="33874-106">El evento **CdromMediaChange** se produce cuando se inserta o se expulsa un CD o DVD en una unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="33874-106">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a><span data-ttu-id="33874-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="33874-107">Event Data</span></span>

<span data-ttu-id="33874-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="33874-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEventHandler**.</span></span> <span data-ttu-id="33874-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="33874-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="33874-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33874-110">Property</span></span> | <span data-ttu-id="33874-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="33874-111">Description</span></span>                                                        |
|----------|--------------------------------------------------------------------|
| <span data-ttu-id="33874-112">CdromNum</span><span class="sxs-lookup"><span data-stu-id="33874-112">CdromNum</span></span> | <span data-ttu-id="33874-113">System. Int32Specifies índice de la unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="33874-113">System.Int32Specifies the index of the CD or DVD drive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33874-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33874-114">Remarks</span></span>

<span data-ttu-id="33874-115">El índice de la unidad de CD corresponde al índice de una interfaz IWMPCdrom accesible a través de la interfaz IWMPCdromCollection.</span><span class="sxs-lookup"><span data-stu-id="33874-115">The index of the CD drive corresponds to the index of an IWMPCdrom interface accessible through the IWMPCdromCollection interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="33874-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33874-116">Requirements</span></span>



| <span data-ttu-id="33874-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="33874-117">Requirement</span></span> | <span data-ttu-id="33874-118">Value</span><span class="sxs-lookup"><span data-stu-id="33874-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33874-119">Versión</span><span class="sxs-lookup"><span data-stu-id="33874-119">Version</span></span><br/>   | <span data-ttu-id="33874-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="33874-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="33874-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="33874-121">Namespace</span></span><br/> | <span data-ttu-id="33874-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="33874-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="33874-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="33874-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="33874-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="33874-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33874-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="33874-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33874-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="33874-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="33874-127">**Interfaz IWMPCdrom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="33874-127">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="33874-128">**Interfaz IWMPCdromCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="33874-128">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





