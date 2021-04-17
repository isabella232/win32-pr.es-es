---
title: Propiedad AxWindowsMediaPlayer. fullScreen
description: La propiedad fullScreen obtiene o establece un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- propiedad fullScreen Media Player Windows
- propiedad fullScreen Media Player Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad fullScreen
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698543"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a><span data-ttu-id="ea0fa-106">Propiedad AxWindowsMediaPlayer. fullScreen</span><span class="sxs-lookup"><span data-stu-id="ea0fa-106">AxWindowsMediaPlayer.fullScreen property</span></span>

<span data-ttu-id="ea0fa-107">La propiedad fullScreen obtiene o establece un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-107">The fullScreen property gets or sets a value indicating whether video content is played in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea0fa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea0fa-108">Syntax</span></span>


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="ea0fa-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ea0fa-109">Property value</span></span>

<span data-ttu-id="ea0fa-110">Valor System. Boolean que indica si el contenido se reproduce en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-110">A System.Boolean value that indicates whether content is played in full-screen mode.</span></span> <span data-ttu-id="ea0fa-111">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea0fa-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea0fa-112">Remarks</span></span>

<span data-ttu-id="ea0fa-113">Para que el modo de pantalla completa funcione correctamente al insertar el control Media Player de Windows, el área de presentación del vídeo debe tener un alto y un ancho de al menos un píxel.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-113">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="ea0fa-114">Si **uiMode** se establece en "mini" o "Full", el alto del propio control debe ser 65 o superior para dar cabida al área de presentación de vídeo además de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-114">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="ea0fa-115">Si **uiMode** se establece en "invisible", al establecer esta propiedad en true se genera un error y no se ve afectado el comportamiento del control.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-115">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="ea0fa-116">Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) es igual a false y **uiMode** es igual a "none".</span><span class="sxs-lookup"><span data-stu-id="ea0fa-116">During full-screen playback, Windows Media Player hides the mouse cursor when [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="ea0fa-117">Si **uiMode** se establece en "Full" o "mini", Windows Media Player muestra los controles de transporte en modo de pantalla completa cuando se mueve el cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-117">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="ea0fa-118">Después de un breve intervalo de ausencia de movimiento del mouse, se ocultan los controles de transporte.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-118">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="ea0fa-119">Si **uiMode** se establece en "none", no se muestra ningún control en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-119">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="ea0fa-120">Para mostrar los controles de transporte en modo de pantalla completa, se requiere el sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-120">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

 

<span data-ttu-id="ea0fa-121">Si los controles de transporte no se muestran en el modo de pantalla completa, Windows Media Player sale automáticamente del modo de pantalla completa cuando se detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-121">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

## <a name="examples"></a><span data-ttu-id="ea0fa-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ea0fa-122">Examples</span></span>

<span data-ttu-id="ea0fa-123">En el ejemplo siguiente se crea un botón que utiliza la propiedad fullScreen para cambiar un objeto reproductor incrustado al modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-123">The following example creates a button that uses the fullScreen property to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="ea0fa-124">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="ea0fa-124">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ea0fa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea0fa-125">Requirements</span></span>



| <span data-ttu-id="ea0fa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea0fa-126">Requirement</span></span> | <span data-ttu-id="ea0fa-127">Value</span><span class="sxs-lookup"><span data-stu-id="ea0fa-127">Value</span></span> |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea0fa-128">Versión</span><span class="sxs-lookup"><span data-stu-id="ea0fa-128">Version</span></span><br/>   | <span data-ttu-id="ea0fa-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ea0fa-129">Windows Media Player 9 Series or later</span></span><br/>                                                                  |
| <span data-ttu-id="ea0fa-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ea0fa-130">Namespace</span></span><br/> | <span data-ttu-id="ea0fa-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ea0fa-131">**AxWMPLib**</span></span><br/>                                                                                            |
| <span data-ttu-id="ea0fa-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ea0fa-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ea0fa-133"><dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ea0fa-133"><dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea0fa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea0fa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea0fa-135">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ea0fa-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ea0fa-136">**AxWindowsMediaPlayer. uiMode (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ea0fa-136">**AxWindowsMediaPlayer.uiMode (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





