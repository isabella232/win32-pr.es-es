---
title: Evento AudioLanguageChange del objeto AxWindowsMediaPlayer
description: El evento AudioLanguageChange se produce cuando cambia el idioma de audio actual. | Evento AudioLanguageChange del objeto AxWindowsMediaPlayer
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Evento AudioLanguageChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698487"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="688ce-105">Evento AudioLanguageChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="688ce-105">AudioLanguageChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="688ce-106">El evento AudioLanguageChange se produce cuando cambia el idioma de audio actual.</span><span class="sxs-lookup"><span data-stu-id="688ce-106">The AudioLanguageChange event occurs when the current audio language changes.</span></span>

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a><span data-ttu-id="688ce-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="688ce-107">Event Data</span></span>

<span data-ttu-id="688ce-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="688ce-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEventHandler**.</span></span> <span data-ttu-id="688ce-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="688ce-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="688ce-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="688ce-110">Property</span></span>   | <span data-ttu-id="688ce-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="688ce-111">Description</span></span>                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="688ce-112">**ididioma**</span><span class="sxs-lookup"><span data-stu-id="688ce-112">**langID**</span></span> | <span data-ttu-id="688ce-113">**System. Int32** Identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="688ce-113">**System.Int32** Uniquely identifies a particular language dialect, called a locale.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="688ce-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="688ce-114">Remarks</span></span>

<span data-ttu-id="688ce-115">Un identificador de configuración regional (LCID) identifica de forma única un dialecto de idioma determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="688ce-115">A locale identifier (LCID) uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="688ce-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="688ce-116">Requirements</span></span>



| <span data-ttu-id="688ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="688ce-117">Requirement</span></span> | <span data-ttu-id="688ce-118">Value</span><span class="sxs-lookup"><span data-stu-id="688ce-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="688ce-119">Versión</span><span class="sxs-lookup"><span data-stu-id="688ce-119">Version</span></span><br/>   | <span data-ttu-id="688ce-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="688ce-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="688ce-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="688ce-121">Namespace</span></span><br/> | <span data-ttu-id="688ce-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="688ce-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="688ce-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="688ce-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="688ce-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="688ce-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="688ce-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="688ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="688ce-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="688ce-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="688ce-127">**IWMPControls3. currentAudioLanguage (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="688ce-127">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





