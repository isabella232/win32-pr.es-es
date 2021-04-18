---
title: Estilos de control comunes (CommCtrl. h)
description: En esta sección se enumeran los estilos de control comunes. Excepto donde se indique, estos estilos se aplican a los controles Rebar, los controles de barra de herramientas y las ventanas de estado.
ms.assetid: aab0cd68-ede7-474b-8695-c75805669716
topic_type:
- apiref
api_name:
- CCS_ADJUSTABLE
- CCS_BOTTOM
- CCS_LEFT
- CCS_NODIVIDER
- CCS_NOMOVEX
- CCS_NOMOVEY
- CCS_NOPARENTALIGN
- CCS_NORESIZE
- CCS_RIGHT
- CCS_TOP
- CCS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a50b28a95d94a97da2fb6ac3522dbc568af111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653593"
---
# <a name="common-control-styles"></a>Estilos de control comunes

En esta sección se enumeran los estilos de control comunes. Excepto donde se indique, estos estilos se aplican a los controles Rebar, los controles de barra de herramientas y las ventanas de estado.



| Constante                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**CCS \_ ajustable**</dt> </dl>          | Habilita las características de personalización integradas de una barra de herramientas, que permiten al usuario arrastrar un botón a una nueva posición o quitar un botón arrastrándolo fuera de la barra de herramientas. Además, el usuario puede hacer doble clic en la barra de herramientas para mostrar el cuadro de diálogo **personalizar barra** de herramientas, que permite al usuario agregar, eliminar y reorganizar botones de la barra de herramientas.<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**CCS \_ inferior**</dt> </dl>                      | Hace que el control se coloque en la parte inferior del área de cliente de la ventana primaria y establece el ancho en el mismo que el ancho de la ventana primaria. Las ventanas de estado tienen este estilo de forma predeterminada.<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**CCS a la \_ izquierda**</dt> </dl>                            | [Versión 4,70](common-controls-intro.md). Hace que el control se muestre verticalmente en el lado izquierdo de la ventana primaria.<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**CCS \_ divisor**</dt> </dl>             | Impide que se dibuje un resaltado de dos píxeles en la parte superior del control. <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**CCS \_ NOMOVEX**</dt> </dl>                   | [Versión 4,70](common-controls-intro.md). Hace que el control cambie de tamaño y se mueva verticalmente, pero no horizontalmente, en respuesta a un mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) . Si \_ se utiliza CCS NORESIZE, este estilo no se aplica.<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ NOmovey**</dt> </dl>                   | Hace que el control cambie de tamaño y se mueva horizontalmente, pero no verticalmente, en respuesta a un mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) . Si \_ se utiliza CCS NORESIZE, este estilo no se aplica. Las ventanas de encabezado tienen este estilo de forma predeterminada.<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**CCS \_ NOPARENTALIGN**</dt> </dl> | Impide que el control se mueva automáticamente a la parte superior o inferior de la ventana primaria. En su lugar, el control mantiene su posición dentro de la ventana primaria a pesar de los cambios en el tamaño del elemento primario. Si \_ también se utiliza CCS Top o CCS \_ Bottom, el alto se ajusta al valor predeterminado, pero la posición y el ancho permanecen inalterados. <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ NORESIZE**</dt> </dl>                | Impide que el control use el ancho y el alto predeterminados al establecer su tamaño inicial o un nuevo tamaño. En su lugar, el control usa el ancho y el alto especificados en la solicitud de creación o ajuste de tamaño. <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS a la \_ derecha**</dt> </dl>                         | [Versión 4,70](common-controls-intro.md). Hace que el control se muestre verticalmente en el lado derecho de la ventana primaria.<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**CCS \_ superior**</dt> </dl>                               | Hace que el control se coloque en la parte superior del área de cliente de la ventana primaria y establece el ancho en el mismo que el ancho de la ventana primaria. De forma predeterminada, las barras de herramientas tienen este estilo. <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**CCS \_ Vert**</dt> </dl>                            | [Versión 4,70](common-controls-intro.md). Hace que el control se muestre verticalmente.<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Observaciones

En los temas siguientes se describen los estilos de control adicionales:

-   [**Estilos de control de animación**](animation-control-styles.md)
-   [**Estilos de botón**](button-styles.md)
-   [**Estilos de cuadro combinado**](combo-box-styles.md)
-   [**Estilos extendidos del control ComboBoxEx**](comboboxex-control-extended-styles.md)
-   [**Estilos de control de selector de fecha y hora**](date-and-time-picker-control-styles.md)
-   [**Editar estilos de control**](edit-control-styles.md)
-   [**Estilos de control de encabezado**](header-control-styles.md)
-   [**Estilos de cuadro de lista**](list-box-styles.md)
-   [**Estilos de ventana de vista de lista**](list-view-window-styles.md)
-   [**Estilos de control de calendario mensual**](month-calendar-control-styles.md)
-   [**Estilos de control de buscapersonas**](pager-control-styles.md)
-   [**Estilos de control de barra de progreso**](progress-bar-control-styles.md)
-   [**Estilos de control rebar**](rebar-control-styles.md)
-   [**Estilos de control Rich Edit**](rich-edit-control-styles.md)
-   [**Estilos de control de barra de desplazamiento**](scroll-bar-control-styles.md)
-   [Estilos de control estáticos](static-control-styles.md)
-   [**Estilos de barra de estado**](status-bar-styles.md)
-   [**Estilos del control SysLink**](syslink-control-styles.md)
-   [**Estilos de control de pestaña**](tab-control-styles.md)
-   [**Controles de barra de herramientas y estilos de botón**](toolbar-control-and-button-styles.md)
-   [**Estilos de información sobre herramientas**](tooltip-styles.md)
-   [**Estilos del control TrackBar**](trackbar-control-styles.md)
-   [**Estilos de ventana de control de vista de árbol**](tree-view-control-window-styles.md)
-   [**Estilos de control de flechas**](up-down-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

