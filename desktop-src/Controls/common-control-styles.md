---
title: Estilos de control comunes (CommCtrl.h)
description: En esta sección se enumeran los estilos de control comunes. Excepto donde se indica, estos estilos se aplican a controles rebar, controles de barra de herramientas y ventanas de estado.
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
ms.openlocfilehash: bd9ec00cd7cedc4bb105543f932cd5fdcfc76d7c038fb930abb7f0b5d1aeb13d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698825"
---
# <a name="common-control-styles"></a>Estilos de control comunes

En esta sección se enumeran los estilos de control comunes. Excepto donde se indica, estos estilos se aplican a controles rebar, controles de barra de herramientas y ventanas de estado.



| Constante                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CCS_ADJUSTABLE"></span><span id="ccs_adjustable"></span><dl> <dt>**CCS \_ ADJUSTABLE**</dt> </dl>          | Habilita las características de personalización integradas de una barra de herramientas, que permiten al usuario arrastrar un botón a una nueva posición o quitar un botón arrastrándolo fuera de la barra de herramientas. Además, el usuario puede hacer doble clic  en la barra de herramientas para mostrar el cuadro de diálogo Personalizar barra de herramientas, que permite al usuario agregar, eliminar y reorganizar los botones de la barra de herramientas.<br/> |
| <span id="CCS_BOTTOM"></span><span id="ccs_bottom"></span><dl> <dt>**CCS \_ BOTTOM**</dt> </dl>                      | Hace que el control se coloque en la parte inferior del área cliente de la ventana primaria y establece que el ancho sea el mismo que el ancho de la ventana primaria. Las ventanas de estado tienen este estilo de forma predeterminada.<br/>                                                                                                                                          |
| <span id="CCS_LEFT"></span><span id="ccs_left"></span><dl> <dt>**CCS \_ LEFT**</dt> </dl>                            | [Versión 4.70.](common-controls-intro.md) Hace que el control se muestre verticalmente en el lado izquierdo de la ventana primaria.<br/>                                                                                                                                                                                                            |
| <span id="CCS_NODIVIDER"></span><span id="ccs_nodivider"></span><dl> <dt>**CCS \_ NODIVIDER**</dt> </dl>             | Impide que se dibuja un resaltado de dos píxeles en la parte superior del control. <br/>                                                                                                                                                                                                                                                                |
| <span id="CCS_NOMOVEX"></span><span id="ccs_nomovex"></span><dl> <dt>**CCS \_ NOMOVEX**</dt> </dl>                   | [Versión 4.70.](common-controls-intro.md) Hace que el control cambie de tamaño y se mueva verticalmente, pero no horizontalmente, en respuesta a un [**mensaje \_ WM SIZE.**](/windows/desktop/winmsg/wm-size) Si se usa \_ CCS NORESIZE, este estilo no se aplica.<br/>                                                                                                    |
| <span id="CCS_NOMOVEY"></span><span id="ccs_nomovey"></span><dl> <dt>**CCS \_ NOMOVEY**</dt> </dl>                   | Hace que el control cambie de tamaño y se mueva horizontalmente, pero no verticalmente, en respuesta a un [**mensaje \_ WM SIZE.**](/windows/desktop/winmsg/wm-size) Si se usa \_ CCS NORESIZE, este estilo no se aplica. Las ventanas de encabezado tienen este estilo de forma predeterminada.<br/>                                                                                                    |
| <span id="CCS_NOPARENTALIGN"></span><span id="ccs_noparentalign"></span><dl> <dt>**CCS \_ NOPARENTALIGN**</dt> </dl> | Impide que el control se mueva automáticamente a la parte superior o inferior de la ventana primaria. En su lugar, el control mantiene su posición dentro de la ventana primaria a pesar de los cambios en el tamaño del elemento primario. Si también se usa CCS TOP o CCS BOTTOM, el alto se ajusta al valor predeterminado, pero la posición y el ancho \_ \_ permanecen sin cambios. <br/>        |
| <span id="CCS_NORESIZE"></span><span id="ccs_noresize"></span><dl> <dt>**CCS \_ NORESIZE**</dt> </dl>                | Impide que el control use el ancho y alto predeterminados al establecer su tamaño inicial o un nuevo tamaño. En su lugar, el control usa el ancho y el alto especificados en la solicitud de creación o ajuste de tamaño. <br/>                                                                                                                                 |
| <span id="CCS_RIGHT"></span><span id="ccs_right"></span><dl> <dt>**CCS \_ RIGHT**</dt> </dl>                         | [Versión 4.70.](common-controls-intro.md) Hace que el control se muestre verticalmente en el lado derecho de la ventana primaria.<br/>                                                                                                                                                                                                           |
| <span id="CCS_TOP"></span><span id="ccs_top"></span><dl> <dt>**CCS \_ TOP**</dt> </dl>                               | Hace que el control se coloque en la parte superior del área de cliente de la ventana primaria y establece que el ancho sea el mismo que el ancho de la ventana primaria. Las barras de herramientas tienen este estilo de forma predeterminada. <br/>                                                                                                                                                  |
| <span id="CCS_VERT"></span><span id="ccs_vert"></span><dl> <dt>**CCS \_ VERT**</dt> </dl>                            | [Versión 4.70.](common-controls-intro.md) Hace que el control se muestre verticalmente.<br/>                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Comentarios

En los temas siguientes se describen estilos de control adicionales:

-   [**Estilos de control de animación**](animation-control-styles.md)
-   [**Estilos de botón**](button-styles.md)
-   [**Estilos de cuadro combinado**](combo-box-styles.md)
-   [**Estilos extendidos del control ComboBoxEx**](comboboxex-control-extended-styles.md)
-   [**Estilos de control selector de fecha y hora**](date-and-time-picker-control-styles.md)
-   [**Editar estilos de control**](edit-control-styles.md)
-   [**Estilos de control de encabezado**](header-control-styles.md)
-   [**Estilos de cuadro de lista**](list-box-styles.md)
-   [**Estilos de ventana De vista de lista**](list-view-window-styles.md)
-   [**Estilos de control de calendario mensual**](month-calendar-control-styles.md)
-   [**Estilos de control de paginación**](pager-control-styles.md)
-   [**Estilos de control de barra de progreso**](progress-bar-control-styles.md)
-   [**Estilos de control Rebar**](rebar-control-styles.md)
-   [**Estilos de control Rich Edit**](rich-edit-control-styles.md)
-   [**Estilos de control de barra de desplazamiento**](scroll-bar-control-styles.md)
-   [Estilos de control estáticos](static-control-styles.md)
-   [**Estilos de barra de estado**](status-bar-styles.md)
-   [**Estilos de control SysLink**](syslink-control-styles.md)
-   [**Estilos de control de pestaña**](tab-control-styles.md)
-   [**Estilos de botón y control de barra de herramientas**](toolbar-control-and-button-styles.md)
-   [**Estilos de información sobre herramientas**](tooltip-styles.md)
-   [**Estilos de control de la barra de seguimiento**](trackbar-control-styles.md)
-   [**Estilos de ventana de control Vista de árbol**](tree-view-control-window-styles.md)
-   [**Estilos de control hacia abajo**](up-down-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

