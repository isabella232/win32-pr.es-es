---
title: Propiedad IWMPSettings de autoStart
description: La propiedad autoStart obtiene o establece un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- propiedades de inicio automático de Windows Media Player
- propiedad autoStart Media Player Windows, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad autoStart
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718880"
---
# <a name="iwmpsettingsautostart-property"></a><span data-ttu-id="61b70-106">IWMPSettings:: autoStart (propiedad)</span><span class="sxs-lookup"><span data-stu-id="61b70-106">IWMPSettings::autoStart property</span></span>

<span data-ttu-id="61b70-107">La propiedad **autoStart** obtiene o establece un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="61b70-107">The **autoStart** property gets or sets a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b70-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61b70-108">Syntax</span></span>


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="61b70-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="61b70-109">Property value</span></span>

<span data-ttu-id="61b70-110">Valor **System. Boolean** que indica si el elemento multimedia actual comienza a reproducirse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="61b70-110">A **System.Boolean** value that indicates whether the current media item begins playing automatically.</span></span> <span data-ttu-id="61b70-111">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="61b70-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="61b70-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61b70-112">Remarks</span></span>

<span data-ttu-id="61b70-113">Si **autoStart** se establece en **true**, el elemento multimedia comenzará a reproducirse cuando se establezca **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentPlaylist** o **AxWindowsMediaPlayer. currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="61b70-113">If **autoStart** is set to **true**, the media item will begin playing when **AxWindowsMediaPlayer.URL**, **AxWindowsMediaPlayer.currentPlaylist**, or **AxWindowsMediaPlayer.currentMedia** is set.</span></span> <span data-ttu-id="61b70-114">De lo contrario, el elemento multimedia no comenzará a reproducirse hasta que se llame al método **IWMPControls. Play** .</span><span class="sxs-lookup"><span data-stu-id="61b70-114">Otherwise, the media item will not start playing until the **IWMPControls.play** method is called.</span></span>

<span data-ttu-id="61b70-115">A menos que establezca **autoStart** en **true** inmediatamente antes de especificar un elemento multimedia, no debe confiar en este valor como sustituto para usar el método **IWMPControls. Play** .</span><span class="sxs-lookup"><span data-stu-id="61b70-115">Unless you set **autoStart** to **true** immediately before specifying a media item, you should not rely on this setting as a substitute for using the **IWMPControls.play** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b70-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b70-116">Requirements</span></span>



| <span data-ttu-id="61b70-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b70-117">Requirement</span></span> | <span data-ttu-id="61b70-118">Value</span><span class="sxs-lookup"><span data-stu-id="61b70-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b70-119">Versión</span><span class="sxs-lookup"><span data-stu-id="61b70-119">Version</span></span><br/>   | <span data-ttu-id="61b70-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="61b70-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="61b70-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61b70-121">Namespace</span></span><br/> | <span data-ttu-id="61b70-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="61b70-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="61b70-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="61b70-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="61b70-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="61b70-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b70-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="61b70-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b70-126">**AxWindowsMediaPlayer. currentMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="61b70-126">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="61b70-127">**AxWindowsMediaPlayer. currentPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="61b70-127">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="61b70-128">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="61b70-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="61b70-129">**IWMPControls. Play (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="61b70-129">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="61b70-130">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="61b70-130">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





