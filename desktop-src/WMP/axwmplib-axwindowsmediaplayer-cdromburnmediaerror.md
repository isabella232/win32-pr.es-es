---
title: Evento CdromBurnMediaError del objeto AxWindowsMediaPlayer
description: El evento CdromBurnMediaError tiene lugar cuando se produce un error mientras se graba un elemento multimedia individual en un CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Evento CdromBurnMediaError del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698482"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="01552-104">Evento CdromBurnMediaError del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="01552-104">CdromBurnMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="01552-105">El evento CdromBurnMediaError tiene lugar cuando se produce un error mientras se graba un elemento multimedia individual en un CD.</span><span class="sxs-lookup"><span data-stu-id="01552-105">The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.</span></span>

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a><span data-ttu-id="01552-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="01552-106">Event Data</span></span>

<span data-ttu-id="01552-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="01552-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEventHandler**.</span></span> <span data-ttu-id="01552-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="01552-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="01552-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01552-109">Property</span></span>   | <span data-ttu-id="01552-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="01552-110">Description</span></span>                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01552-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="01552-111">pCdromBurn</span></span> | <span data-ttu-id="01552-112">Interfaz WMPLib. IWMPCdromBurnThe que representa la operación de grabación que provocó el error.</span><span class="sxs-lookup"><span data-stu-id="01552-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/>               |
| <span data-ttu-id="01552-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="01552-113">pMedia</span></span>     | <span data-ttu-id="01552-114">Elemento multimedia System. ObjectThe que generó el error.</span><span class="sxs-lookup"><span data-stu-id="01552-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="01552-115">Puede convertirlo en una interfaz IWMPMedia para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="01552-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="01552-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01552-116">Remarks</span></span>

<span data-ttu-id="01552-117">Para capturar errores genéricos, controle el AxWMPLib. \_ \_Evento WMPOCXEvents CdromBurnError.</span><span class="sxs-lookup"><span data-stu-id="01552-117">To capture generic errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="01552-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01552-118">Requirements</span></span>



| <span data-ttu-id="01552-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="01552-119">Requirement</span></span> | <span data-ttu-id="01552-120">Value</span><span class="sxs-lookup"><span data-stu-id="01552-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01552-121">Versión</span><span class="sxs-lookup"><span data-stu-id="01552-121">Version</span></span><br/>   | <span data-ttu-id="01552-122">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="01552-122">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="01552-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01552-123">Namespace</span></span><br/> | <span data-ttu-id="01552-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="01552-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="01552-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="01552-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="01552-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="01552-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01552-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="01552-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01552-128">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="01552-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="01552-129">**Evento AxWindowsMediaPlayer. CdromBurnError (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="01552-129">**AxWindowsMediaPlayer.CdromBurnError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[<span data-ttu-id="01552-130">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="01552-130">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="01552-131">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="01552-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





