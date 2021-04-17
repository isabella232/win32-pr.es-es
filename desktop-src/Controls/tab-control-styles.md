---
title: Estilos de control de pestaña (CommCtrl. h)
description: En esta sección se enumeran los estilos de control de pestaña admitidos.
ms.assetid: a01a6609-b02e-4ada-afa0-ed5ad8dde0d6
topic_type:
- apiref
api_name:
- TCS_BOTTOM
- TCS_BUTTONS
- TCS_FIXEDWIDTH
- TCS_FLATBUTTONS
- TCS_FOCUSNEVER
- TCS_FOCUSONBUTTONDOWN
- TCS_FORCEICONLEFT
- TCS_FORCELABELLEFT
- TCS_HOTTRACK
- TCS_MULTILINE
- TCS_MULTISELECT
- TCS_OWNERDRAWFIXED
- TCS_RAGGEDRIGHT
- TCS_RIGHT
- TCS_RIGHTJUSTIFY
- TCS_SCROLLOPPOSITE
- TCS_SINGLELINE
- TCS_TABS
- TCS_TOOLTIPS
- TCS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 352864fe71b5efc39529109bafb3bdc49cee68e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660470"
---
# <a name="tab-control-styles"></a>Estilos de control de pestaña

En esta sección se enumeran los estilos de control de pestaña admitidos.



| Constante                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**los ect \_ inferiores**</dt> </dl>                                  | [Versión 4,70](common-control-versions.md). Las pestañas aparecen en la parte inferior del control. Este valor es igual a TCS a la \_ derecha. Este estilo no se admite si usa ComCtl32.dll versión 6.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**botones de TCS \_**</dt> </dl>                               | Las pestañas aparecen como botones y no se dibuja ningún borde alrededor del área de presentación.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**TCS \_ FIXEDWIDTH**</dt> </dl>                      | Todas las pestañas tienen el mismo ancho. Este estilo no se puede combinar con el \_ estilo de RIGHTJUSTIFY de TCS.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**FLATBUTTONS de TCS \_**</dt> </dl>                   | [Versión 4,71](common-control-versions.md). Las pestañas seleccionadas aparecen como sangrías en segundo plano mientras que otras pestañas aparecen en el mismo plano que el fondo. Este estilo solo afecta a los controles de ficha con el \_ estilo botones de TCS.<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**FOCUSNEVER de TCS \_**</dt> </dl>                      | El control de pestaña no recibe el foco de entrada cuando se hace clic en él.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**FOCUSONBUTTONDOWN de TCS \_**</dt> </dl> | El control de pestaña recibe el foco de entrada cuando se hace clic en él.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**FORCEICONLEFT de TCS \_**</dt> </dl>             | Los iconos están alineados con el borde izquierdo de cada pestaña de ancho fijo. Este estilo solo se puede usar con el \_ estilo TCS FIXEDWIDTH.<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**FORCELABELLEFT de TCS \_**</dt> </dl>          | Las etiquetas se alinean con el borde izquierdo de cada pestaña de ancho fijo; es decir, la etiqueta se muestra inmediatamente a la derecha del icono en lugar de centrarse. Este estilo solo se puede usar con el \_ estilo TCS FIXEDWIDTH e implica el \_ estilo FORCEICONLEFT de TCS.<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**HOTTRACK de TCS \_**</dt> </dl>                            | [Versión 4,70](common-control-versions.md). Los elementos que se encuentran bajo el puntero se resaltan automáticamente. Puede comprobar si el seguimiento activo está habilitado mediante una llamada a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**\_varias líneas de ect**</dt> </dl>                         | Se muestran varias filas de pestañas, si es necesario, por lo que todas las pestañas están visibles a la vez.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**SELECCIÓN de ect \_**</dt> </dl>                   | [Versión 4,70](common-control-versions.md). Se pueden seleccionar varias pestañas si se mantiene presionada la tecla CTRL al hacer clic. Este estilo se debe usar con el \_ estilo botones de TCS.<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**los ect \_ OWNERDRAWFIXED**</dt> </dl>          | La ventana primaria es responsable de las pestañas de dibujo.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**RAGGEDRIGHT de TCS \_**</dt> </dl>                   | Las filas de pestañas no se ajustarán para rellenar todo el ancho del control. Este estilo es el valor predeterminado.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS a la \_ derecha**</dt> </dl>                                     | [Versión 4,70](common-control-versions.md). Las pestañas aparecen verticalmente en el lado derecho de los controles que usan el \_ estilo vertical de TCS. Este valor es igual a TCS en la \_ parte inferior. Este estilo no se admite si se usan estilos visuales.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**RIGHTJUSTIFY de TCS \_**</dt> </dl>                | El ancho de cada pestaña aumenta, si es necesario, para que cada fila de pestañas ocupe todo el ancho del control de ficha. Este estilo de ventana se omite a menos que \_ también se especifique el estilo de varias líneas de TCS.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**SCROLLOPPOSITE de TCS \_**</dt> </dl>          | [Versión 4,70](common-control-versions.md). Las pestañas innecesarias se desplazan al lado opuesto del control cuando se selecciona una pestaña.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**SINGLELINE de TCS \_**</dt> </dl>                      | Solo se muestra una fila de pestañas. El usuario puede desplazarse para ver más pestañas, si es necesario. Este estilo es el valor predeterminado.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**\_pestañas de ect**</dt> </dl>                                        | Las pestañas aparecen como pestañas y se dibuja un borde alrededor del área de presentación. Este estilo es el valor predeterminado.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**\_información sobre herramientas de ect**</dt> </dl>                            | El control de ficha tiene un control de información sobre herramientas asociado a él. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**TCS \_ vertical**</dt> </dl>                            | [Versión 4,70](common-control-versions.md). Las pestañas aparecen en el lado izquierdo del control y el texto de la pestaña se muestra verticalmente. Este estilo solo es válido cuando se usa con el \_ estilo de varias líneas de TCS. Para que aparezcan las pestañas en el lado derecho del control, use también el \_ estilo derecho de TCS. Este estilo no se admite si usa ComCtl32.dll versión 6.<br/> |



## <a name="remarks"></a>Observaciones

Los siguientes estilos se pueden modificar una vez creado el control.

-   los ect \_ inferiores
-   botones de TCS \_
-   TCS \_ FIXEDWIDTH
-   FLATBUTTONS de TCS \_
-   FORCEICONLEFT de TCS \_
-   FORCELABELLEFT de TCS \_
-   \_varias líneas de ect
-   los ect \_ OWNERDRAWFIXED
-   RAGGEDRIGHT de TCS \_
-   TCS a la \_ derecha
-   TCS \_ vertical

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

