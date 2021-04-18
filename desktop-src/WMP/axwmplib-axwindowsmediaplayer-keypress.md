---
title: Evento KeyPress del objeto AxWindowsMediaPlayer
description: El evento KeyPress tiene lugar cuando se presiona y se suelta una tecla. | Evento KeyPress del objeto AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Evento KeyPress del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700165"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4b0d2-105">Evento KeyPress del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4b0d2-105">KeyPress Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4b0d2-106">El evento KeyPress tiene lugar cuando se presiona y se suelta una tecla.</span><span class="sxs-lookup"><span data-stu-id="4b0d2-106">The KeyPress event occurs when a key is pressed and released.</span></span>

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a><span data-ttu-id="4b0d2-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="4b0d2-107">Event Data</span></span>

<span data-ttu-id="4b0d2-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4b0d2-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEventHandler**.</span></span> <span data-ttu-id="4b0d2-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="4b0d2-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="4b0d2-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b0d2-110">Property</span></span>      | <span data-ttu-id="4b0d2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b0d2-111">Description</span></span>                                                                        |
|---------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0d2-112">**nKeyAscii**</span><span class="sxs-lookup"><span data-stu-id="4b0d2-112">**nKeyAscii**</span></span> | <span data-ttu-id="4b0d2-113">System. Int16Specifies el código ANSI numérico estándar para el carácter.</span><span class="sxs-lookup"><span data-stu-id="4b0d2-113">System.Int16Specifies the standard numeric ANSI code for the character.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b0d2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b0d2-114">Remarks</span></span>

<span data-ttu-id="4b0d2-115">Este evento se produce cuando el resultado de la pulsación de tecla es cualquier carácter imprimible, la tecla CTRL combinada con un carácter del alfabeto estándar o uno de unos pocos caracteres especiales, y la tecla entrar o retroceso.</span><span class="sxs-lookup"><span data-stu-id="4b0d2-115">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b0d2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b0d2-116">Requirements</span></span>



| <span data-ttu-id="4b0d2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b0d2-117">Requirement</span></span> | <span data-ttu-id="4b0d2-118">Value</span><span class="sxs-lookup"><span data-stu-id="4b0d2-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0d2-119">Versión</span><span class="sxs-lookup"><span data-stu-id="4b0d2-119">Version</span></span><br/>   | <span data-ttu-id="4b0d2-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4b0d2-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4b0d2-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4b0d2-121">Namespace</span></span><br/> | <span data-ttu-id="4b0d2-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4b0d2-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4b0d2-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="4b0d2-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4b0d2-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4b0d2-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b0d2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b0d2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b0d2-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4b0d2-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





