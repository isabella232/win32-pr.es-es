---
title: Estilos de control de barra de progreso (CommCtrl.h)
description: Los controles de barra de progreso admiten los siguientes estilos de control.
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1216171b116bffb962b3ebfe1a76497473cf2db2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167614"
---
# <a name="progress-bar-control-styles"></a>Estilos de control de barra de progreso

Los controles de barra de progreso admiten los siguientes estilos [de](progress-bar-control.md) control:




| Constante | Descripción | 
|----------|-------------|
| <span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl><dt><strong>PBS_MARQUEE</strong></dt></dl> | <a href="common-control-versions.md">Versión 6.0</a> o posterior. El indicador de progreso no aumenta de tamaño, sino que se mueve repetidamente a lo largo de la longitud de la barra, lo que indica la actividad sin especificar qué proporción del progreso se ha completado. <br /><blockquote>[!Note]<br />Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows o posterior. Para usar Comctl32.dll versión 6, es especificarlo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">Habilitar estilos visuales.</a></blockquote><br /> | 
| <span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl><dt><strong>PBS_SMOOTH</strong></dt></dl> | <a href="common-control-versions.md">Versión 4.70</a> o posterior. La barra de progreso muestra el estado de progreso en una barra de desplazamiento suave en lugar de la barra segmentada predeterminada. <br /><blockquote>[!Note]<br />Este estilo solo se admite en el tema Windows clásico. Todos los demás temas invalidan este estilo.</blockquote><br /> | 
| <span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl><dt><strong>PBS_SMOOTHREVERSE</strong></dt></dl> | <a href="common-control-versions.md">Versión 6.0</a> o posterior y <strong>Windows Vista.</strong> Determina el comportamiento de animación que debe usar la barra de progreso al retroceder (de un valor superior a un valor inferior). Si se establece, se producirá una transición "suave"; de lo contrario, el control "saltará" al valor inferior.<br /> | 
| <span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl><dt><strong>PBS_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Versión 4.70</a> o posterior. La barra de progreso muestra el estado de progreso verticalmente, de abajo a arriba.<br /> | 




## <a name="remarks"></a>Observaciones

Puede establecer estilos de barra de progreso, de la misma manera que otros controles comunes, con [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)o [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

