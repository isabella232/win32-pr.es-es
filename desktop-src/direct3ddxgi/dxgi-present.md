---
description: Las constantes PRESENT de DXGI \_ especifican opciones para presentar fotogramas a la salida.
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb2d682a01ed52c827e9be9f3afd927c227afe2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476701"
---
# <a name="dxgi_present"></a>DXGI \_ PRESENT

Las **constantes PRESENT \_ de DXGI** especifican opciones para presentar fotogramas a la salida.




| Constante o valor | Descripción | 
|----------------|-------------|
| <span></span><dl><dt><strong></strong></dt><dt>0</dt></dl> | Presente un fotograma de cada búfer (empezando por el búfer actual) en la salida.<br /> | 
| <span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl><dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt><dt>0x00000002UL</dt></dl> | Presente un marco desde el búfer actual a la salida. Use esta marca para que la presentación pueda usar la sincronización vertical en blanco en lugar de secuenciar los búferes de la cadena de la manera habitual.<br /><blockquote>[!Note]<br />Si la aplicación que realiza la llamada establece la constante DXGI_PRESENT_DO_NOT_SEQUENCE en la primera operación actual (es decir, cuando no hay ningún búfer actual), el tiempo de ejecución omite esa operación actual y no llama al controlador.</blockquote><br /> | 
| <span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl><dt><strong>DXGI_PRESENT_TEST</strong></dt><dt>0x00000001UL</dt></dl> | No presente el marco en la salida. Se probará el estado de la cadena de intercambio y se devolverán los errores adecuados. DXGI_PRESENT_TEST está pensado para su uso solo al cambiar del estado de inactividad; no lo use para determinar cuándo cambiar al estado de inactividad porque puede dejar que la cadena de intercambio no pueda salir del modo de pantalla completa.<br /> | 
| <span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl><dt><strong>DXGI_PRESENT_RESTART</strong></dt><dt>0x00000004UL</dt></dl> | Especifica que el tiempo de ejecución descartará los objetos en cola pendientes.<br /> | 
| <span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl><dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt><dt>0x00000008UL</dt></dl> | Especifica que el tiempo de ejecución producirá un error en la presentación (es decir, se producirá un error en una llamada a <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::P resent1)</strong></a>con el código de error DXGI_ERROR_WAS_STILL_DRAWING si el subproceso de llamada <a href="dxgi-error.md">está</a> bloqueado; el tiempo de ejecución DXGI_ERROR_WAS_STILL_DRAWING en lugar de estar en estado de independencia hasta que se resuelva la dependencia.<br /><strong>Direct3D 11:</strong> Este valor de enumeración se admite a partir de Windows 8.<br /> | 
| <span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl><dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt><dt>0x00000010UL</dt></dl> | Indica que el contenido de la presentación solo se mostrará en la salida concreta. El contenido no será visible en otras salidas. Por ejemplo, si el usuario intenta reubicar el contenido de vídeo en otra salida, el contenido del vídeo no estará visible. <br /><strong>Direct3D 11:</strong> Este valor de enumeración se admite a partir de Windows 8. <br /><blockquote>[!Note]<br />Esta marca solo se debe usar con efecto de <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">intercambio DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> o DXGI_SWAP_EFFECT_FLIP_DISCARD. El uso de esta marca con <em>otros efectos</em> de intercambio está en desuso y es posible que no funcione en versiones futuras de Windows.</blockquote><br /> | 
| <span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl><dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt><dt>0x00000020UL</dt></dl> | Indica que si el estéreo presente debe reducirse a mono, se usa la visualización con los ojos derecho en lugar de la vista con los ojos izquierdos.<br /><strong>Direct3D 11:</strong> Este valor de enumeración se admite a partir de Windows 8.<br /> | 
| <span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl><dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt><dt>0x00000040UL</dt></dl> | Indica que la presentación debe usar el búfer izquierdo como búfer mono. Una aplicación llama al <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>método IDXGISwapChain1::IsTemporaryMonoSupported</strong></a> para determinar si una cadena de intercambio admite "mono temporal".<br /><strong>Direct3D 11:</strong> Este valor de enumeración se admite a partir de Windows 8.<br /> | 
| <span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl><dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt><dt>0x00000100UL</dt></dl> | Esta marca debe establecerse mediante aplicaciones multimedia que actualmente usan una duración presente personalizada (frecuencia de actualización personalizada). Vea <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia.</strong></a><br /><blockquote>[!Note]<br />Este valor se admite a partir de Windows 8.1.</blockquote><br /> | 
| <span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl><dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt><dt>0x00000200UL</dt></dl> | Permitir la lágrima es un requisito de las pantallas de frecuencia de actualización variable.<br /> Las condiciones para usar DXGI_PRESENT_ALLOW_TEARING durante present son las siguientes:<br /><ul><li>La cadena de intercambio debe crearse con la <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> de intercambio.</li><li>El intervalo de sincronización pasado a <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Present</strong></a> (o <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1)</strong></a>debe ser 0.</li><li>La DXGI_PRESENT_ALLOW_TEARING no se puede usar en una aplicación que se encuentra actualmente en modo exclusivo de pantalla completa (establecido mediante una llamada a <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState(TRUE)</strong></a>). Solo se puede usar en modo de ventana. Para usar esta marca en aplicaciones Win32 de pantalla completa, la aplicación debe presentarse en una ventana sin borde de pantalla completa y deshabilitar el cambio automático de pantalla completa ALT+ENTRAR mediante <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory::MakeWindowAssociation</strong></a>. Las aplicaciones para UWP que entran en modo de pantalla completa mediante una llamada a son ventanas sin borde de pantalla <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> completa y pueden usar la marca .</li></ul>Si <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>se llama</strong></a> a Present (o <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1)</strong></a>con esta marca y no se cumplen las condiciones anteriores, se devolverá DXGI_ERROR_INVALID_CALL error a la aplicación que realiza la llamada.<br /> | 




## <a name="remarks"></a>Comentarios

Las opciones de presentación se proporcionan durante la llamada [**IDXGISwapChain::P resent**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) o [**IDXGISwapChain1::P resent1.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) Los búferes se especifican en la descripción de la cadena de intercambio (vea [**DXGI \_ SWAP CHAIN \_ \_ DESC**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) o [**DXGI SWAP CHAIN \_ \_ \_ DESC1).**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)

DXGI PRESENT RESTART solo es válido para cadenas de intercambio de modelos de volteo \_ \_ y pantalla completa. Las aplicaciones pueden usar DXGI PRESENT RESTART para recuperarse de problemas en la reproducción, así como para descartar presentaciones \_ \_ previamente en cola. Descartar presentaciones previamente en cola es útil si esas presentaciones en cola son escenarios con ventanas. En concreto, la presentación anteriormente en cola podría haber asumido que la ventana es un tamaño antiguo (es decir, se produjo una operación de cambio de tamaño después del envío).

DXGI PRESENT RESTRICT TO OUTPUT solo es válido para cadenas de intercambio que especificaron una salida determinada para restringir el contenido a cuando se crearon esas cadenas de intercambio \_ \_ ( \_ \_ [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). Si no hay ninguna salida a la que restringir, la marca no es válida.

DXGI PRESENT STEREO PREFER RIGHT indica que si el presente estéreo debe reducirse a mono, se debe usar el ojo derecho en lugar del ojo izquierdo \_ \_ \_ \_ (predeterminado). Puede usar esta marca si un lado es de mayor calidad (por ejemplo, si el par estéreo se sintetiza a partir de una imagen estándar).

DXGI PRESENT STEREO TEMPORARY MONO indica que el presente debe usar el búfer \_ izquierdo \_ como búfer \_ \_ mono. Puede usar esta marca para evitar actualizar el búfer correcto cuando una aplicación no tiene contenido estéreo temporalmente. Debe usar esta marca siempre que sea posible porque permite una optimización significativa por parte del sistema operativo y, en algunas circunstancias, puede evitar artefactos de cambio de modo visible.

Debe usar la marca DXGI PRESENT STEREO TEMPORARY MONO en lugar de cambiar a una cadena de intercambio mono para la mayoría de las aplicaciones que prevé que volverán a usar \_ \_ \_ \_ estéreo. Debe equilibrar el uso de esta marca en aplicaciones de ejecución extremadamente larga o que rara vez muestran estéreo en contra de la desventaja de la memoria sin usar.

> [!Note]  
> Las aplicaciones de pantalla completa que cambian a una cadena de intercambio mono provocan un cambio de modo que generalmente tiene artefactos visibles (por ejemplo, "flashing"). Sin embargo, es posible que mono temporal no sea compatible con cadenas de intercambio de pantalla completa.

 

Las marcas DXGI PRESENT STEREO PREFER RIGHT y DXGI PRESENT STEREO TEMPORARY MONO solo se aplican \_ \_ a \_ \_ \_ \_ \_ \_ cadenas de intercambio estéreo. Si las usa al presentar cadenas de intercambio mono, se produce una operación no válida.

Si usa la marca DXGI PRESENT STEREO TEMPORARY MONO al presentar una cadena de intercambio estéreo que no admite mono temporal, se produce un error, la cadena de intercambio no se muestra y la presentación devuelve \_ \_ \_ \_ [DXGI \_ ERROR INVALID \_ \_ CALL](dxgi-error.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
