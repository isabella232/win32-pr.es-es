---
title: Propiedad AxWindowsMediaPlayer. playState
description: La propiedad playState obtiene un valor de enumeración que indica el estado de la operación de Media Player de Windows.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- propiedades de playState Media Player de Windows
- propiedad playState Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad playState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700214"
---
# <a name="axwindowsmediaplayerplaystate-property"></a><span data-ttu-id="0ddaa-106">Propiedad AxWindowsMediaPlayer. playState</span><span class="sxs-lookup"><span data-stu-id="0ddaa-106">AxWindowsMediaPlayer.playState property</span></span>

<span data-ttu-id="0ddaa-107">La propiedad playState obtiene un valor de enumeración que indica el estado de la operación de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-107">The playState property gets an enumeration value indicating the state of the Windows Media Player operation.</span></span>

<span data-ttu-id="0ddaa-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddaa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ddaa-109">Syntax</span></span>


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a><span data-ttu-id="0ddaa-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0ddaa-110">Property value</span></span>

<span data-ttu-id="0ddaa-111">El valor de enumeración WMPLib. WMPPlayState.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-111">The WMPLib.WMPPlayState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ddaa-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ddaa-112">Remarks</span></span>

<span data-ttu-id="0ddaa-113">No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="0ddaa-114">Además, no todos los Estados se producen necesariamente durante una secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="0ddaa-115">No debe escribir código que se base en el orden de los Estados.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-115">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="0ddaa-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0ddaa-116">Examples</span></span>

<span data-ttu-id="0ddaa-117">En el ejemplo siguiente se usa la propiedad playState para mostrar el estado actual de reproducción del reproductor en una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-117">The following example uses the playState property to display the current playing status of the player in a label.</span></span> <span data-ttu-id="0ddaa-118">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a><span data-ttu-id="0ddaa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ddaa-119">Requirements</span></span>



| <span data-ttu-id="0ddaa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ddaa-120">Requirement</span></span> | <span data-ttu-id="0ddaa-121">Value</span><span class="sxs-lookup"><span data-stu-id="0ddaa-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddaa-122">Versión</span><span class="sxs-lookup"><span data-stu-id="0ddaa-122">Version</span></span><br/>   | <span data-ttu-id="0ddaa-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="0ddaa-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="0ddaa-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0ddaa-124">Namespace</span></span><br/> | <span data-ttu-id="0ddaa-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ddaa-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0ddaa-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="0ddaa-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ddaa-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0ddaa-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ddaa-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ddaa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddaa-129">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="0ddaa-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ddaa-130">**Evento AxWindowsMediaPlayer. PlayStateChange (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="0ddaa-130">**AxWindowsMediaPlayer.PlayStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="0ddaa-131">**WMPPlayState**</span><span class="sxs-lookup"><span data-stu-id="0ddaa-131">**WMPPlayState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





