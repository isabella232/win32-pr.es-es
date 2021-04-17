---
title: Evento FolderScanStateChange del objeto AxWindowsMediaPlayer
description: El evento FolderScanStateChange se produce cuando cambia el estado de una operación de supervisión de carpetas.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Evento FolderScanStateChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698544"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a042a-104">Evento FolderScanStateChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a042a-104">FolderScanStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a042a-105">El evento FolderScanStateChange se produce cuando cambia el estado de una operación de supervisión de carpetas.</span><span class="sxs-lookup"><span data-stu-id="a042a-105">The FolderScanStateChange event occurs when a folder monitoring operation changes state.</span></span>

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a><span data-ttu-id="a042a-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="a042a-106">Event Data</span></span>

<span data-ttu-id="a042a-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="a042a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEventHandler**.</span></span> <span data-ttu-id="a042a-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="a042a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a042a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a042a-109">Property</span></span> | <span data-ttu-id="a042a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a042a-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a042a-111">wmpfss</span><span class="sxs-lookup"><span data-stu-id="a042a-111">wmpfss</span></span>   | <span data-ttu-id="a042a-112">Valor de enumeración WMPLib. WMPFolderScanStateThe que indica el nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="a042a-112">WMPLib.WMPFolderScanStateThe enumeration value that indicates the new state.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a042a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a042a-113">Requirements</span></span>



| <span data-ttu-id="a042a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a042a-114">Requirement</span></span> | <span data-ttu-id="a042a-115">Value</span><span class="sxs-lookup"><span data-stu-id="a042a-115">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a042a-116">Versión</span><span class="sxs-lookup"><span data-stu-id="a042a-116">Version</span></span><br/>   | <span data-ttu-id="a042a-117">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="a042a-117">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="a042a-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a042a-118">Namespace</span></span><br/> | <span data-ttu-id="a042a-119">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a042a-119">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a042a-120">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a042a-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a042a-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a042a-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a042a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a042a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a042a-123">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a042a-123">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a042a-124">**WMPFolderScanState**</span><span class="sxs-lookup"><span data-stu-id="a042a-124">**WMPFolderScanState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





