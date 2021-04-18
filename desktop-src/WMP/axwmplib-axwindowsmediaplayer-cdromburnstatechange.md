---
title: Evento CdromBurnStateChange del objeto AxWindowsMediaPlayer
description: El evento CdromBurnStateChange se produce cuando cambia el estado de una operación de grabación de CD.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Evento CdromBurnStateChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698483"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f94ea-104">Evento CdromBurnStateChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="f94ea-104">CdromBurnStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f94ea-105">El evento CdromBurnStateChange se produce cuando cambia el estado de una operación de grabación de CD.</span><span class="sxs-lookup"><span data-stu-id="f94ea-105">The CdromBurnStateChange event occurs when a CD burning operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a><span data-ttu-id="f94ea-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="f94ea-106">Event Data</span></span>

<span data-ttu-id="f94ea-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="f94ea-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEventHandler**.</span></span> <span data-ttu-id="f94ea-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="f94ea-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="f94ea-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f94ea-109">Property</span></span>   | <span data-ttu-id="f94ea-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f94ea-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f94ea-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="f94ea-111">pCdromBurn</span></span> | <span data-ttu-id="f94ea-112">Interfaz WMPLib. IWMPCdromBurnThe que representa la operación de grabación que provocó el error.</span><span class="sxs-lookup"><span data-stu-id="f94ea-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |
| <span data-ttu-id="f94ea-113">wmpbs</span><span class="sxs-lookup"><span data-stu-id="f94ea-113">wmpbs</span></span>      | <span data-ttu-id="f94ea-114">Valor de enumeración WMPLib. WMPBurnStateThe que indica el nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="f94ea-114">WMPLib.WMPBurnStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="f94ea-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f94ea-115">Requirements</span></span>



| <span data-ttu-id="f94ea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f94ea-116">Requirement</span></span> | <span data-ttu-id="f94ea-117">Value</span><span class="sxs-lookup"><span data-stu-id="f94ea-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f94ea-118">Versión</span><span class="sxs-lookup"><span data-stu-id="f94ea-118">Version</span></span><br/>   | <span data-ttu-id="f94ea-119">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="f94ea-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="f94ea-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f94ea-120">Namespace</span></span><br/> | <span data-ttu-id="f94ea-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f94ea-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f94ea-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="f94ea-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f94ea-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f94ea-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94ea-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f94ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94ea-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f94ea-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f94ea-126">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f94ea-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f94ea-127">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="f94ea-127">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





