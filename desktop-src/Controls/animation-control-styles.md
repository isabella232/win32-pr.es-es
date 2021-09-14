---
title: Estilos de control de animación (CommCtrl.h)
description: En esta sección se enumeran los estilos de ventana utilizados con controles de animación.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aff6116433533bdc79535be0e282cb81baa9368f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170154"
---
# <a name="animation-control-styles"></a>Estilos de control de animación

En esta sección se enumeran los estilos de ventana utilizados con controles de animación.




| Constante | Descripción | 
|----------|-------------|
| <span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl><dt><strong>ACS_AUTOPLAY</strong></dt></dl> | Comienza a reproducir la animación en cuanto se abre el clip AVI. <br /> | 
| <span id="ACS_CENTER"></span><span id="acs_center"></span><dl><dt><strong>ACS_CENTER</strong></dt></dl> | Centra la animación en la ventana del control de animación. <br /> | 
| <span id="ACS_TIMER"></span><span id="acs_timer"></span><dl><dt><strong>ACS_TIMER</strong></dt></dl> | De forma predeterminada, el control crea un subproceso para reproducir el clip AVI. Si establece esta marca, el control reproduce el clip sin crear un subproceso; internamente, el control usa un temporizador Win32 para sincronizar la reproducción. <br /><strong>Comctl32.dll versión 6 y posteriores:</strong> No se admite este estilo. De forma predeterminada, el control reproduce el clip AVI sin crear un subproceso.<br /><blockquote>[!Note]<br />Comctl32.dll versión 6 no es redistribuible. Para usar Comctl32.dll versión 6, es especificarlo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">Habilitar estilos visuales.</a></blockquote><br /> | 
| <span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl><dt><strong>ACS_TRANSPARENT</strong></dt></dl> | Permite hacer coincidir el color de fondo de una animación con el de la ventana subyacente, creando un fondo "transparente". El elemento primario del control de animación no debe tener el WS_CLIPCHILDREN (vea <a href="/windows/desktop/winmsg/window-styles">Estilos de ventana).</a> El control envía un <a href="wm-ctlcolorstatic.md"><strong>mensaje WM_CTLCOLORSTATIC</strong></a> a su elemento primario. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor para</strong></a> establecer el color de fondo del contexto del dispositivo en un valor adecuado. El control interpreta el píxel superior izquierdo del primer fotograma como el color de fondo predeterminado de la animación. Volverá a asignar todos los píxeles con ese color al valor que proporcionó en respuesta a WM_CTLCOLORSTATIC. <br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



