---
title: Evento CdromBurnError del objeto AxWindowsMediaPlayer
description: El evento CdromBurnError tiene lugar cuando se produce un error genérico durante una operación de grabación de CD.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Evento CdromBurnError del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698484"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="85acd-104">Evento CdromBurnError del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="85acd-104">CdromBurnError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="85acd-105">El evento CdromBurnError tiene lugar cuando se produce un error genérico durante una operación de grabación de CD.</span><span class="sxs-lookup"><span data-stu-id="85acd-105">The CdromBurnError event occurs when a generic error happens during a CD burning operation.</span></span>

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a><span data-ttu-id="85acd-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="85acd-106">Event Data</span></span>

<span data-ttu-id="85acd-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="85acd-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEventHandler**.</span></span> <span data-ttu-id="85acd-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="85acd-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="85acd-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85acd-109">Property</span></span>   | <span data-ttu-id="85acd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="85acd-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85acd-111">hrError</span><span class="sxs-lookup"><span data-stu-id="85acd-111">hrError</span></span>    | <span data-ttu-id="85acd-112">**System. Int32** El error que provocó el evento.</span><span class="sxs-lookup"><span data-stu-id="85acd-112">**System.Int32** The error that raised the event.</span></span><br/>                                               |
| <span data-ttu-id="85acd-113">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="85acd-113">pCdromBurn</span></span> | <span data-ttu-id="85acd-114">Interfaz WMPLib. IWMPCdromBurnThe que representa la operación de grabación que provocó el error.</span><span class="sxs-lookup"><span data-stu-id="85acd-114">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="85acd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85acd-115">Remarks</span></span>

<span data-ttu-id="85acd-116">Para capturar errores específicos de medios, controle el AxWMPLib. \_ \_Evento WMPOCXEvents CdromBurnMediaError.</span><span class="sxs-lookup"><span data-stu-id="85acd-116">To capture media specific errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="85acd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85acd-117">Requirements</span></span>



| <span data-ttu-id="85acd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="85acd-118">Requirement</span></span> | <span data-ttu-id="85acd-119">Value</span><span class="sxs-lookup"><span data-stu-id="85acd-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85acd-120">Versión</span><span class="sxs-lookup"><span data-stu-id="85acd-120">Version</span></span><br/>   | <span data-ttu-id="85acd-121">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="85acd-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="85acd-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85acd-122">Namespace</span></span><br/> | <span data-ttu-id="85acd-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="85acd-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="85acd-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="85acd-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="85acd-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="85acd-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85acd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="85acd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85acd-127">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="85acd-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="85acd-128">**Evento AxWindowsMediaPlayer. CdromBurnMediaError (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="85acd-128">**AxWindowsMediaPlayer.CdromBurnMediaError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[<span data-ttu-id="85acd-129">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="85acd-129">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





