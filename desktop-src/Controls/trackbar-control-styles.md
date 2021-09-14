---
title: Estilos de control trackbar (CommCtrl.h)
description: Esta sección contiene información sobre los estilos usados con controles de barra de seguimiento.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165986"
---
# <a name="trackbar-control-styles"></a>Estilos de control de la barra de seguimiento

Esta sección contiene información sobre los estilos usados con controles de barra de seguimiento.



| Constante                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**TBS \_ AUTOTICKS**</dt> </dl>                      | El control trackbar tiene una marca de graduación para cada incremento de su intervalo de valores. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**TBS \_ VERT**</dt> </dl>                                     | El control trackbar está orientado verticalmente.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**TBS \_ HORZ**</dt> </dl>                                     | El control trackbar está orientado horizontalmente. Esta es la orientación predeterminada. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**TBS \_ TOP**</dt> </dl>                                        | El control trackbar muestra marcas de graduación encima del control. Este estilo solo es válido con TBS \_ HORZ. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**TBS \_ BOTTOM**</dt> </dl>                               | El control trackbar muestra marcas de graduación debajo del control. Este estilo solo es válido con TBS \_ HORZ. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**TBS \_ LEFT**</dt> </dl>                                     | El control trackbar muestra marcas de graduación a la izquierda del control. Este estilo solo es válido con TBS \_ VERT. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**DERECHO DE \_ TBS**</dt> </dl>                                  | El control trackbar muestra marcas de graduación a la derecha del control. Este estilo solo es válido con TBS \_ VERT. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_ AMBOS**</dt> </dl>                                     | El control trackbar muestra marcas de graduación en ambos lados del control. Será superior e inferior cuando se utilice con TBS HORZ o tanto a la izquierda como a la \_ derecha si se usa con \_ TBS VERT. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**TBS \_ NOTICKS**</dt> </dl>                            | El control trackbar no muestra ninguna marca de graduación. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**TBS \_ ENABLESELRANGE**</dt> </dl>       | El control trackbar muestra solo un intervalo de selección. Las marcas de graduación en las posiciones inicial y final de un intervalo de selección se muestran como triángulos (en lugar de guiones verticales) y el intervalo de selección se resalta. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**TBS \_ FIXEDLENGTH**</dt> </dl>                | El control trackbar permite cambiar el tamaño del control deslizante con el [**mensaje \_ TBM SETTHUMBLENGTH.**](tbm-setthumblength.md) <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TBS \_ NOTHUMB**</dt> </dl>                            | El control trackbar no muestra un control deslizante. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**INFORMACIÓN SOBRE \_ HERRAMIENTAS DE TBS**</dt> </dl>                         | [Versión 4.70.](common-control-versions.md) El control trackbar admite información sobre herramientas. Cuando se crea un control trackbar con este estilo, crea automáticamente un control de información sobre herramientas predeterminado que muestra la posición actual del control deslizante. Puede cambiar dónde se muestra la información sobre herramientas mediante el [**mensaje \_ SETTIPSIDE de TBM.**](tbm-settipside.md) <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**TB \_ INVERTIDOS**</dt> </dl>                         | [Versión 5.80.](common-control-versions.md) Este bit de estilo se usa para barras de seguimiento "invertida", donde un número más pequeño indica "mayor" y un número mayor indica "menor". No tiene ningún efecto en el control; es simplemente una etiqueta que se puede comprobar para determinar si una barra de seguimiento es normal o se invierte.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**TBS \_ DOWNISLEFT**</dt> </dl>                   | De forma predeterminada, el control trackbar usa los valores inferiores iguales a derecha e iguales a izquierda. Use el estilo DOWNISLEFT de TBS para invertir el valor predeterminado, lo que hace que sea igual a la izquierda \_ y hacia arriba igual a la derecha. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**TBS \_ NOTIFYBEFOREMOVE**</dt> </dl> | [Versión 6.00](common-control-versions.md) **y Windows Vista.** La barra de seguimiento debe notificar al elemento primario antes de cambiar la posición del control deslizante debido a la acción del usuario (habilita el ajuste). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**TBS \_ TRANSPARENTBNDAND**</dt> </dl> | [Versión 6.00](common-control-versions.md) **y Windows Vista.** El elemento primario pinta el fondo a través del \_ mensaje PRINTCLIENT de WM. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





