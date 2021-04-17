---
title: Estilos del control TrackBar (CommCtrl. h)
description: Esta sección contiene información sobre los estilos usados con los controles TrackBar.
ms.assetid: ac2f59c6-85a2-4f41-aace-4132971d3559
topic_type:
- apiref
api_name:
- TBS_AUTOTICKS
- TBS_VERT
- TBS_HORZ
- TBS_TOP
- TBS_BOTTOM
- TBS_LEFT
- TBS_RIGHT
- TBS_BOTH
- TBS_NOTICKS
- TBS_ENABLESELRANGE
- TBS_FIXEDLENGTH
- TBS_NOTHUMB
- TBS_TOOLTIPS
- TBS_REVERSED
- TBS_DOWNISLEFT
- TBS_NOTIFYBEFOREMOVE
- TBS_TRANSPARENTBKGND
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42966f98db18257c9a6a9ca463d5bd88028a02f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660428"
---
# <a name="trackbar-control-styles"></a>Estilos del control TrackBar

Esta sección contiene información sobre los estilos usados con los controles TrackBar.



| Constante                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**ciclos de paso de TBS \_**</dt> </dl>                      | El control TrackBar tiene una marca de graduación para cada incremento en su intervalo de valores. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**vertical de TBS \_**</dt> </dl>                                     | El control TrackBar está orientado verticalmente.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**\_horizontal TBS**</dt> </dl>                                     | El control TrackBar está orientado horizontalmente. Esta es la orientación predeterminada. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**TBS \_ superior**</dt> </dl>                                        | El control TrackBar muestra las marcas de graduación sobre el control. Este estilo solo es válido con TBS \_ horizontal. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**inferior de TBS \_**</dt> </dl>                               | El control TrackBar muestra las marcas de graduación debajo del control. Este estilo solo es válido con TBS \_ horizontal. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**TBS a la \_ izquierda**</dt> </dl>                                     | El control TrackBar muestra las marcas de graduación a la izquierda del control. Este estilo solo es válido con TBS \_ Vert. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**TBS a la \_ derecha**</dt> </dl>                                  | El control TrackBar muestra las marcas de graduación a la derecha del control. Este estilo solo es válido con TBS \_ Vert. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_ ambos**</dt> </dl>                                     | El control TrackBar muestra las marcas de graduación en ambos lados del control. Esta será la parte superior e inferior cuando se use con TBS \_ horizontal o tanto a la izquierda como a la derecha si se usa con TBS \_ Vert. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**notics de TBS \_**</dt> </dl>                            | El control TrackBar no muestra ninguna marca de graduación. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**\_ENABLESELRANGE TBS**</dt> </dl>       | El control TrackBar solo muestra un intervalo de selección. Las marcas de graduación de las posiciones inicial y final de un intervalo de selección se muestran como triángulos (en lugar de guiones verticales) y se resalta el intervalo de selección. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**FIXEDLENGTH de TBS \_**</dt> </dl>                | El control TrackBar permite cambiar el tamaño del control deslizante con el mensaje [**\_ SETTHUMBLENGTH de TBM**](tbm-setthumblength.md) . <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**no está en el control de TBS \_**</dt> </dl>                            | El control TrackBar no muestra un control deslizante. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**\_información sobre herramientas de TBS**</dt> </dl>                         | [Versión 4,70](common-control-versions.md). El control TrackBar admite información sobre herramientas. Cuando se crea un control TrackBar con este estilo, se crea automáticamente un control ToolTip predeterminado que muestra la posición actual del control deslizante. Puede cambiar el lugar en el que se muestra la información sobre herramientas mediante el mensaje [**TBM \_ SETTIPSIDE**](tbm-settipside.md) . <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**TBS \_ invertido**</dt> </dl>                         | [Versión 5,80.](common-control-versions.md) Este bit de estilo se usa para el trackbars "invertido", donde un número menor indica "mayor" y un número mayor indica "inferior". No tiene ningún efecto en el control; es simplemente una etiqueta que se puede comprobar para determinar si una barra de estado es normal o inversa.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**\_DOWNISLEFT TBS**</dt> </dl>                   | De forma predeterminada, el control de barra de seguimiento usa un valor inferior a derecha y de igual a izquierda. Use el \_ estilo DOWNISLEFT de TBS para invertir el valor predeterminado, desactivando igual a izquierda y hacia arriba a la derecha. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**\_NOTIFYBEFOREMOVE TBS**</dt> </dl> | [Versión 6,00](common-control-versions.md) y **Windows Vista.** TrackBar debe notificar a Parent antes de cambiar la posición del control deslizante debido a la acción del usuario (permite el ajuste). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**\_TRANSPARENTBKGND TBS**</dt> </dl> | [Versión 6,00](common-control-versions.md) y **Windows Vista.** El elemento primario pinta el fondo a través del \_ mensaje de PRINTCLIENT de WM. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





