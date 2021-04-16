---
title: Player. uiMode
description: La propiedad uiMode especifica o recupera un valor que indica qué controles se muestran en la interfaz de usuario.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Media Player de Windows Player. uiMode
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708762"
---
# <a name="playeruimode"></a><span data-ttu-id="54fd8-104">Player. uiMode</span><span class="sxs-lookup"><span data-stu-id="54fd8-104">Player.uiMode</span></span>

<span data-ttu-id="54fd8-105">La propiedad **uiMode** especifica o recupera un valor que indica qué controles se muestran en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="54fd8-105">The **uiMode** property specifies or retrieves a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="54fd8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54fd8-106">Syntax</span></span>

<span data-ttu-id="54fd8-107">*reproductor* . **uiMode**</span><span class="sxs-lookup"><span data-stu-id="54fd8-107">*player* .**uiMode**</span></span>

## <a name="possible-values"></a><span data-ttu-id="54fd8-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="54fd8-108">Possible Values</span></span>

<span data-ttu-id="54fd8-109">Esta propiedad es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="54fd8-109">This property is a read/write **String**.</span></span>



| <span data-ttu-id="54fd8-110">Value</span><span class="sxs-lookup"><span data-stu-id="54fd8-110">Value</span></span>     | <span data-ttu-id="54fd8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="54fd8-111">Description</span></span>                                                                                                                                                                                                           | <span data-ttu-id="54fd8-112">Ejemplo de audio</span><span class="sxs-lookup"><span data-stu-id="54fd8-112">Audio Example</span></span>                                          | <span data-ttu-id="54fd8-113">Ejemplo de vídeo</span><span class="sxs-lookup"><span data-stu-id="54fd8-113">Video Example</span></span>                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="54fd8-114">invisibles</span><span class="sxs-lookup"><span data-stu-id="54fd8-114">invisible</span></span> | <span data-ttu-id="54fd8-115">Windows Media Player está incrustado sin ninguna interfaz de usuario visible (controles, vídeo o ventana de visualización).</span><span class="sxs-lookup"><span data-stu-id="54fd8-115">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                        | <span data-ttu-id="54fd8-116">(No se muestra nada).</span><span class="sxs-lookup"><span data-stu-id="54fd8-116">(Nothing is displayed.)</span></span>                                | <span data-ttu-id="54fd8-117">(No se muestra nada).</span><span class="sxs-lookup"><span data-stu-id="54fd8-117">(Nothing is displayed.)</span></span>                                |
| <span data-ttu-id="54fd8-118">ninguno</span><span class="sxs-lookup"><span data-stu-id="54fd8-118">none</span></span>      | <span data-ttu-id="54fd8-119">Windows Media Player está incrustado sin controles y solo se muestra la ventana de vídeo o visualización.</span><span class="sxs-lookup"><span data-stu-id="54fd8-119">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                         | !["ninguno" con audio](images/uimode-none-audio-v11.png) | !["ninguno" con vídeo](images/uimode-none-video-v11.png) |
| <span data-ttu-id="54fd8-122">pequeño</span><span class="sxs-lookup"><span data-stu-id="54fd8-122">mini</span></span>      | <span data-ttu-id="54fd8-123">Windows Media Player está incrustado con los controles ventana de estado, reproducir/pausar, detener, silenciar y volumen mostrados además de la ventana de vídeo o visualización.</span><span class="sxs-lookup"><span data-stu-id="54fd8-123">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                          | !["mini" con audio](images/uimode-mini-audio-v11.png) | !["mini" con vídeo](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="54fd8-126">full</span><span class="sxs-lookup"><span data-stu-id="54fd8-126">full</span></span>      | <span data-ttu-id="54fd8-127">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="54fd8-127">Default.</span></span> <span data-ttu-id="54fd8-128">Windows Media Player está incrustado con la ventana de estado, la barra de búsqueda, los controles de reproducción/pausa, detención, silencio, siguiente, anterior, avance rápido, retroceso rápido y volumen, además de la ventana de vídeo o visualización.</span><span class="sxs-lookup"><span data-stu-id="54fd8-128">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, fast reverse, and volume controls in addition to the video or visualization window.</span></span> | !["completo" con audio](images/uimode-full-audio-v11.png) | !["completo" con vídeo](images/uimode-full-video-v11.png) |
| <span data-ttu-id="54fd8-131">custom</span><span class="sxs-lookup"><span data-stu-id="54fd8-131">custom</span></span>    | <span data-ttu-id="54fd8-132">Windows Media Player está incrustado con una interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="54fd8-132">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="54fd8-133">Solo se puede usar en programas de C++.</span><span class="sxs-lookup"><span data-stu-id="54fd8-133">Can only be used in C++ programs.</span></span>                                                                                                                      | <span data-ttu-id="54fd8-134">(Se muestra la interfaz de usuario personalizada).</span><span class="sxs-lookup"><span data-stu-id="54fd8-134">(Custom user interface is displayed.)</span></span>                  | <span data-ttu-id="54fd8-135">(Se muestra la interfaz de usuario personalizada).</span><span class="sxs-lookup"><span data-stu-id="54fd8-135">(Custom user interface is displayed.)</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="54fd8-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54fd8-136">Remarks</span></span>

<span data-ttu-id="54fd8-137">Esta propiedad especifica la apariencia del Media Player de Windows incrustado.</span><span class="sxs-lookup"><span data-stu-id="54fd8-137">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="54fd8-138">Cuando **uiMode** se establece en "none", "mini" o "Full", hay una ventana para la presentación de clips de vídeo y visualizaciones de audio.</span><span class="sxs-lookup"><span data-stu-id="54fd8-138">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="54fd8-139">Esta ventana se puede ocultar en el modo mini o completo estableciendo el atributo de **alto** de la etiqueta de **objeto** en 40, que se mide desde la parte inferior, y deja visible la parte controles de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="54fd8-139">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="54fd8-140">Si no se desea ninguna interfaz incrustada, establezca los atributos **ancho** y **alto** en cero.</span><span class="sxs-lookup"><span data-stu-id="54fd8-140">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="54fd8-141">Si **uiMode** se establece en "invisible", no se muestra ninguna interfaz de usuario, pero el espacio se reserva en la página según lo especificado en **ancho** y **alto**.</span><span class="sxs-lookup"><span data-stu-id="54fd8-141">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="54fd8-142">Esto resulta útil para conservar el diseño de página cuando **uiMode** puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="54fd8-142">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="54fd8-143">Además, el espacio reservado es transparente, por lo que todos los elementos que estén en capas detrás del control serán visibles.</span><span class="sxs-lookup"><span data-stu-id="54fd8-143">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="54fd8-144">Si **uiMode** se establece en "Full" o "mini", Windows Media Player muestra los controles de transporte en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="54fd8-144">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="54fd8-145">Si **uiMode** se establece en "none", no se muestra ningún control en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="54fd8-145">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="54fd8-146">Si la ventana está visible y el contenido de audio se está reproduciendo, la visualización que se muestra será la que se usó más recientemente en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="54fd8-146">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="54fd8-147">Si **uiMode** se establece en "Custom" en un programa de C++ que implementa **IWMPRemoteMediaServices**, se muestra el archivo de máscara indicado por **IWMPRemoteMediaServices:: GetCustomUIMode** .</span><span class="sxs-lookup"><span data-stu-id="54fd8-147">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices::GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="54fd8-148">Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".</span><span class="sxs-lookup"><span data-stu-id="54fd8-148">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="54fd8-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="54fd8-149">Examples</span></span>

<span data-ttu-id="54fd8-150">En el ejemplo siguiente se crea un elemento SELECT de HTML que permite al usuario cambiar la interfaz de usuario para un objeto **reproductor** incrustado.</span><span class="sxs-lookup"><span data-stu-id="54fd8-150">The following example creates an HTML SELECT element that allows the user to change the user interface for an embedded **Player** object.</span></span> <span data-ttu-id="54fd8-151">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="54fd8-151">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



<span data-ttu-id="54fd8-152">Windows Media Player 10 Mobile: esta propiedad solo acepta o devuelve los valores "none" o "Full".</span><span class="sxs-lookup"><span data-stu-id="54fd8-152">Windows Media Player 10 Mobile: This property only accepts or returns values of "none" or "full".</span></span> <span data-ttu-id="54fd8-153">En dispositivos Smartphone, solo se muestran el estado de reproducción y un contador cuando *uiMode* se establece en "Full".</span><span class="sxs-lookup"><span data-stu-id="54fd8-153">On Smartphone devices, only playback status and a counter are displayed when *uiMode* is set to "full".</span></span>

## <a name="requirements"></a><span data-ttu-id="54fd8-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54fd8-154">Requirements</span></span>



| <span data-ttu-id="54fd8-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="54fd8-155">Requirement</span></span> | <span data-ttu-id="54fd8-156">Value</span><span class="sxs-lookup"><span data-stu-id="54fd8-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fd8-157">Versión</span><span class="sxs-lookup"><span data-stu-id="54fd8-157">Version</span></span><br/> | <span data-ttu-id="54fd8-158">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="54fd8-158">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="54fd8-159">Windows Media Player 9 series o posterior para "invisible" o "personalizado".</span><span class="sxs-lookup"><span data-stu-id="54fd8-159">Windows Media Player 9 Series or later for "invisible" or "custom".</span></span><br/> |
| <span data-ttu-id="54fd8-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54fd8-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="54fd8-161"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54fd8-161"><dt>Wmp.dll</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="54fd8-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="54fd8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fd8-163">**Interfaz IWMPRemoteMediaServices**</span><span class="sxs-lookup"><span data-stu-id="54fd8-163">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[<span data-ttu-id="54fd8-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span><span class="sxs-lookup"><span data-stu-id="54fd8-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[<span data-ttu-id="54fd8-165">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="54fd8-165">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





