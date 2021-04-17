---
title: IWMPControls playItem, método
description: El método playItem reproduce el elemento multimedia especificado. | IWMPControls playItem, método
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- método playItem de Windows Media Player
- método playItem Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método playItem
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690874"
---
# <a name="iwmpcontrolsplayitem-method"></a><span data-ttu-id="06ae5-107">IWMPControls::p método layItem</span><span class="sxs-lookup"><span data-stu-id="06ae5-107">IWMPControls::playItem method</span></span>

<span data-ttu-id="06ae5-108">El método **playItem** reproduce el elemento multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="06ae5-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ae5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06ae5-109">Syntax</span></span>


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a><span data-ttu-id="06ae5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06ae5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06ae5-111">*pIWMPMedia* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06ae5-111">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06ae5-112">Una interfaz **WMPLib. IWMPMedia** para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="06ae5-112">A **WMPLib.IWMPMedia** interface to the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06ae5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06ae5-113">Return value</span></span>

<span data-ttu-id="06ae5-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="06ae5-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06ae5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06ae5-115">Remarks</span></span>

<span data-ttu-id="06ae5-116">El elemento multimedia se cargará y reproducirá automáticamente, independientemente del valor de la propiedad **IWMPSettings. autoStart** .</span><span class="sxs-lookup"><span data-stu-id="06ae5-116">The media item will load and play automatically, regardless of the value of the **IWMPSettings.autoStart** property.</span></span> <span data-ttu-id="06ae5-117">Para cargar un elemento sin reproducirlo automáticamente, establezca **IWMPSettings. autoStart** en **false** y asigne un valor a **AxWindowsMediaPlayer. URL**, después del cual se puede llamar a **IWMPControls. Play** para empezar a reproducir el elemento.</span><span class="sxs-lookup"><span data-stu-id="06ae5-117">To load an item without playing it automatically, set **IWMPSettings.autoStart** to **false** and assign a value to **AxWindowsMediaPlayer.URL**, after which **IWMPControls.play** can be called to start playing the item.</span></span>

<span data-ttu-id="06ae5-118">Nota</span><span class="sxs-lookup"><span data-stu-id="06ae5-118">Note</span></span>

<span data-ttu-id="06ae5-119">**playItem** solo funciona con elementos de **AxWindowsMediaPlayer. currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="06ae5-119">**playItem** works only with items in **AxWindowsMediaPlayer.currentPlaylist**.</span></span> <span data-ttu-id="06ae5-120">No se admite la llamada a **playItem** con una referencia a un elemento multimedia guardado.</span><span class="sxs-lookup"><span data-stu-id="06ae5-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="06ae5-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06ae5-121">Examples</span></span>

<span data-ttu-id="06ae5-122">En el ejemplo siguiente se usa **playItem** para reproducir un elemento multimedia de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="06ae5-122">The following example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="06ae5-123">El elemento que se va a reproducir se elige en función de su posición en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="06ae5-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="06ae5-124">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="06ae5-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a><span data-ttu-id="06ae5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06ae5-125">Requirements</span></span>



| <span data-ttu-id="06ae5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="06ae5-126">Requirement</span></span> | <span data-ttu-id="06ae5-127">Value</span><span class="sxs-lookup"><span data-stu-id="06ae5-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06ae5-128">Versión</span><span class="sxs-lookup"><span data-stu-id="06ae5-128">Version</span></span><br/>   | <span data-ttu-id="06ae5-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="06ae5-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="06ae5-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="06ae5-130">Namespace</span></span><br/> | <span data-ttu-id="06ae5-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="06ae5-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="06ae5-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="06ae5-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="06ae5-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="06ae5-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06ae5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="06ae5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ae5-135">**AxWindowsMediaPlayer. currentPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="06ae5-135">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06ae5-136">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="06ae5-136">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06ae5-137">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="06ae5-137">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06ae5-138">**IWMPControls. Play (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="06ae5-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06ae5-139">**IWMPPlaylist. Item (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="06ae5-139">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06ae5-140">**IWMPSettings. autoStart (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="06ae5-140">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





