---
description: Las \_ constantes de DXGI presentes especifican las opciones para presentar fotogramas a la salida.
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a21d53159572a52b372774e4988e775744ede5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707846"
---
# <a name="dxgi_present"></a>DXGI \_ presente

Las constantes de **DXGI \_ presentes** especifican las opciones para presentar fotogramas a la salida.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span></span><dl> <dt><strong></strong></dt><dt>0</dt> </dl></td>
<td style="text-align: left;">Presente un fotograma desde cada búfer (empezando por el búfer actual) hasta la salida.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </dl></td>
<td style="text-align: left;">Presenta un fotograma del búfer actual a la salida. Use esta marca para que la presentación pueda usar la sincronización vertical en blanco en lugar de los búferes de secuenciación de la cadena de la manera habitual.<br/>
<blockquote>
[!Note]<br />
Si la aplicación que realiza la llamada establece la constante DXGI_PRESENT_DO_NOT_SEQUENCE en la primera operación Present (es decir, cuando no hay ningún búfer actual), el tiempo de ejecución omite esa operación Present y no llama al controlador.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </dl></td>
<td style="text-align: left;">No presente el marco en la salida. Se probará el estado de la cadena de intercambio y se devolverán los errores correspondientes. DXGI_PRESENT_TEST está diseñado para usarse solo cuando se cambia del estado de inactividad; no lo utilice para determinar cuándo cambiar al estado de inactividad, ya que, si lo hace, puede dejar que la cadena de intercambio no pueda salir del modo de pantalla completa.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </dl></td>
<td style="text-align: left;">Especifica que el tiempo de ejecución descartará los planteamientos pendientes en cola.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </dl></td>
<td style="text-align: left;">Especifica que el tiempo de ejecución producirá un error en la presentación (es decir, no se realizará una llamada a <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::P resent1</strong></a>) con el código de error <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> si el subproceso que realiza la llamada está bloqueado; el tiempo de ejecución devuelve DXGI_ERROR_WAS_STILL_DRAWING en lugar de suspender hasta que se resuelva la dependencia.<br/> <strong>Direct3D 11:</strong> Este valor de enumeración se admite a partir de Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </dl></td>
<td style="text-align: left;">Indica que el contenido de la presentación se mostrará solo en la salida determinada. El contenido no será visible en otras salidas. Por ejemplo, si el usuario intenta reubicar el contenido de vídeo en otra salida, el contenido del vídeo no será visible. <br/> <strong>Direct3D 11:</strong> Este valor de enumeración se admite a partir de Windows 8. <br/>
<blockquote>
[!Note]<br />
Esta marca solo se debe usar con el efecto de intercambio <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> o DXGI_SWAP_EFFECT_FLIP_DISCARD. El uso de esta marca con <em>otros</em> efectos de intercambio está en desuso y es posible que no funcione en versiones futuras de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </dl></td>
<td style="text-align: left;">Indica que, si el estéreo presente debe reducirse a mono, se usa la visualización a la derecha en lugar de la vista de ojos a la izquierda.<br/> <strong>Direct3D 11:</strong> Este valor de enumeración se admite a partir de Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </dl></td>
<td style="text-align: left;">Indica que la presentación debe utilizar el búfer izquierdo como búfer mono. Una aplicación llama al método <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1:: IsTemporaryMonoSupported</strong></a> para determinar si una cadena de intercambio admite &quot; mono temporal &quot; .<br/> <strong>Direct3D 11:</strong> Este valor de enumeración se admite a partir de Windows 8.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </dl></td>
<td style="text-align: left;">Esta marca se debe establecer mediante aplicaciones multimedia que usan actualmente una duración actual personalizada (frecuencia de actualización personalizada). Vea <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>.<br/>
<blockquote>
[!Note]<br />
Este valor se admite a partir de Windows 8.1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </dl></td>
<td style="text-align: left;">Permitir el recorte es un requisito de la frecuencia de actualización de variables.<br/> Las condiciones para usar DXGI_PRESENT_ALLOW_TEARING durante el presente son las siguientes:<br/>
<ul>
<li>La cadena de intercambio se debe crear con la marca <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> .</li>
<li>El intervalo de sincronización que se pasa a <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>present</strong></a> (o <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) debe ser 0.</li>
<li>La marca de DXGI_PRESENT_ALLOW_TEARING no se puede usar en una aplicación que se encuentre actualmente en modo exclusivo de pantalla completa (se establece mediante una llamada a <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState (true)</strong></a>). Solo se puede usar en modo de ventana. Para usar esta marca en las aplicaciones Win32 de pantalla completa, la aplicación debe encontrarse en una ventana sin borde de pantalla completa y deshabilitar el cambio automático de ALT + entrar en pantalla completa mediante <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory:: MakeWindowAssociation</strong></a>. Las aplicaciones UWP que entran en el modo de pantalla completa mediante una llamada a <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> son ventanas sin borde de pantalla completa y pueden usar la marca.</li>
</ul>
Si se llama a <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>present</strong></a> (o <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) con esta marca y no se cumplen las condiciones anteriores, se producirá un error de DXGI_ERROR_INVALID_CALL que se devolverá a la aplicación que realiza la llamada.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Las opciones de presentación se proporcionan durante la llamada a [**IDXGISwapChain::P reenviar**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) o [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Los búferes se especifican en la descripción de la cadena de intercambio (vea [**dxgi \_ swap \_ Chain \_ DESC**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) o [**dxgi \_ swap \_ Chain \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)).

El \_ \_ reinicio de la presentación de DXGI solo es válido para las cadenas de intercambio de modelo flip y la pantalla completa. Las aplicaciones pueden usar el reinicio de la presentación de DXGI \_ \_ para recuperarse de los problemas de reproducción, así como para descartar las presentaciones en cola previamente. Descartar las presentaciones en cola anteriores resulta útil si esas presentaciones en cola son escenarios de ventanas. En concreto, la presentación en cola anterior podría haber supuesto que la ventana tiene un tamaño anterior (es decir, que se ha producido una operación de cambiar el tamaño después del envío).

DXGI \_ present \_ Restrict \_ to \_ Output solo es válido para las cadenas de intercambio que especificaron una salida determinada a fin de restringir el contenido a cuando se crearon esas cadenas de intercambio ([**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). Si no hay ninguna salida para restringir a, la marca no es válida.

El \_ valor \_ de la opción preferente de estéreo de DXGI \_ \_ indica que si el estéreo presente debe reducirse a mono, se debe usar el ojo adecuado en lugar del ojo izquierdo (predeterminado). Puede usar esta marca si un lado tiene una calidad mayor (por ejemplo, si el par estéreo se sintetiza a partir de una imagen estándar).

\_ \_ El mono temporal estéreo presente de DXGI \_ \_ indica que el presente debe usar el búfer izquierdo como búfer mono. Puede usar esta marca para evitar actualizar el búfer derecho cuando una aplicación no tiene contenido estéreo de forma temporal. Debe utilizar esta marca siempre que sea posible, ya que permite una optimización significativa por parte del sistema operativo y, en algunas circunstancias, puede evitar los artefactos de cambio del modo visible.

Debe usar la \_ \_ \_ \_ marca de mono temporal estéreo presente de DXGI en preferencia para cambiar a una cadena de intercambio mono para la mayoría de las aplicaciones que prevé que usarán de nuevo el estéreo. Debe equilibrar el uso de esta marca en aplicaciones que tienen una ejecución extremadamente larga o que raramente muestran estéreo contra la desventaja de la memoria no utilizada.

> [!Note]  
> Las aplicaciones de pantalla completa que cambian a una cadena de intercambio mono provocan un cambio de modo que generalmente tiene artefactos visibles (por ejemplo, "parpadeo"). Sin embargo, es posible que mono temporal no sea compatible con las cadenas de intercambio de pantalla completa.

 

Las \_ marcas de estéreo presentes de dxgi \_ \_ preferentes \_ right y de la presentación de dxgi de estéreo \_ presente \_ \_ \_ solo se aplican a las cadenas de intercambio estéreo. Si se usan cuando se presentan cadenas de intercambio mono, se produce una operación no válida.

Si usa la marca de \_ \_ mono temporal estéreo presente de DXGI \_ \_ cuando presenta una cadena de intercambio estéreo que no admite mono temporal, se produce un error, la cadena de intercambio no se muestra y la presentación devuelve un [error de DXGI \_ \_ \_ llamada no válida](dxgi-error.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
