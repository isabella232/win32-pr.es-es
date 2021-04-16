---
title: Evento StatusChange del objeto AxWindowsMediaPlayer
description: El evento StatusChange se produce cuando cambia el valor de la propiedad status. | Evento StatusChange del objeto AxWindowsMediaPlayer
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- Evento StatusChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699702"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="2e715-105">Evento StatusChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="2e715-105">StatusChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="2e715-106">El evento **StatusChange** se produce cuando cambia el valor de la propiedad **status** .</span><span class="sxs-lookup"><span data-stu-id="2e715-106">The **StatusChange** event occurs when the **status** property changes value.</span></span>

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a><span data-ttu-id="2e715-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="2e715-107">Event Data</span></span>

<span data-ttu-id="2e715-108">Este evento no contiene datos.</span><span class="sxs-lookup"><span data-stu-id="2e715-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e715-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e715-109">Requirements</span></span>



| <span data-ttu-id="2e715-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e715-110">Requirement</span></span> | <span data-ttu-id="2e715-111">Value</span><span class="sxs-lookup"><span data-stu-id="2e715-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e715-112">Versión</span><span class="sxs-lookup"><span data-stu-id="2e715-112">Version</span></span><br/>   | <span data-ttu-id="2e715-113">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="2e715-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2e715-114">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e715-114">Namespace</span></span><br/> | <span data-ttu-id="2e715-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2e715-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2e715-116">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="2e715-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2e715-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2e715-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e715-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e715-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e715-119">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e715-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2e715-120">**AxWindowsMediaPlayer. status (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e715-120">**AxWindowsMediaPlayer.status (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





