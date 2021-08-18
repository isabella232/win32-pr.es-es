---
title: Estilos de control tab (CommCtrl.h)
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
ms.openlocfilehash: ec4dfdcfb17b2f4a8ffebd4a7cfba5042e19ba2b566d4b03635032438a2f7fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078419"
---
# <a name="tab-control-styles"></a>Estilos de control de pestaña

En esta sección se enumeran los estilos de control de pestaña admitidos.



| Constante                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**TCS \_ BOTTOM**</dt> </dl>                                  | [Versión 4.70.](common-control-versions.md) Las pestañas aparecen en la parte inferior del control. Este valor es igual a TCS \_ RIGHT. Este estilo no se admite si usa ComCtl32.dll versión 6.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**BOTONES DE TCS \_**</dt> </dl>                               | Las pestañas aparecen como botones y no se dibuja ningún borde alrededor del área de presentación.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**TCS \_ FIXEDWIDTH**</dt> </dl>                      | Todas las pestañas tienen el mismo ancho. Este estilo no se puede combinar con el estilo \_ RIGHTJUSTIFY de TCS.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**TCS \_ FLATBUTTONS**</dt> </dl>                   | [Versión 4.71.](common-control-versions.md) Las pestañas seleccionadas aparecen como con sangría en segundo plano, mientras que otras pestañas aparecen en el mismo plano que el fondo. Este estilo solo afecta a los controles de tabulación con el estilo TCS \_ BUTTONS.<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**TCS \_ FOCUSNEVER**</dt> </dl>                      | El control de pestaña no recibe el foco de entrada cuando se hace clic en él.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**TCS \_ FOCUSONBUTTONDOWN**</dt> </dl> | El control de pestaña recibe el foco de entrada cuando se hace clic en él.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**TCS \_ FORCEICONLEFT**</dt> </dl>             | Los iconos se alinean con el borde izquierdo de cada pestaña de ancho fijo. Este estilo solo se puede usar con el \_ estilo FIXEDWIDTH de TCS.<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**TCS \_ FORCELABELLEFT**</dt> </dl>          | Las etiquetas se alinean con el borde izquierdo de cada pestaña de ancho fijo; es decir, la etiqueta se muestra inmediatamente a la derecha del icono en lugar de estar centrada. Este estilo solo se puede usar con el estilo \_ FIXEDWIDTH de TCS e implica el estilo \_ FORCEICONLEFT de TCS.<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**TCS \_ HOTTRACK**</dt> </dl>                            | [Versión 4.70.](common-control-versions.md) Los elementos situados bajo el puntero se resaltan automáticamente. Puede comprobar si el seguimiento en caliente está habilitado llamando [**a SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**TCS \_ MULTILINE**</dt> </dl>                         | Si es necesario, se muestran varias filas de pestañas, por lo que todas las pestañas están visibles a la vez.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**TCS \_ MULTISELECT**</dt> </dl>                   | [Versión 4.70.](common-control-versions.md) Se pueden seleccionar varias pestañas manteniendo presionada la tecla CTRL al hacer clic. Este estilo debe usarse con el estilo TCS \_ BUTTONS.<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**PROPIETARIO DE \_ TCSDRAWFIXED**</dt> </dl>          | La ventana primaria es responsable de dibujar pestañas.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**TCS \_ RAGGEDRIGHT**</dt> </dl>                   | Las filas de pestañas no se ajustarán para rellenar todo el ancho del control. Este estilo es el predeterminado.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS \_ RIGHT**</dt> </dl>                                     | [Versión 4.70.](common-control-versions.md) Las pestañas aparecen verticalmente en el lado derecho de los controles que usan el estilo \_ VERTICAL de TCS. Este valor es igual a TCS \_ BOTTOM. Este estilo no se admite si se usan estilos visuales.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**TCS \_ RIGHTJUSTIFY**</dt> </dl>                | El ancho de cada pestaña aumenta, si es necesario, para que cada fila de pestañas rellene todo el ancho del control de ficha. Este estilo de ventana se omite a menos que también se especifique el \_ estilo MULTILINE de TCS.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**TCS \_ SCROLLOSITE**</dt> </dl>          | [Versión 4.70.](common-control-versions.md) Las pestañas innecesarios se desplazan al lado opuesto del control cuando se selecciona una pestaña.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**TCS \_ SINGLELINE**</dt> </dl>                      | Solo se muestra una fila de pestañas. El usuario puede desplazarse para ver más pestañas, si es necesario. Este estilo es el predeterminado.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**PESTAÑAS \_ DE TCS**</dt> </dl>                                        | Las pestañas aparecen como pestañas y se dibuja un borde alrededor del área de presentación. Este estilo es el predeterminado.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**INFORMACIÓN SOBRE \_ HERRAMIENTAS DE TCS**</dt> </dl>                            | El control de pestaña tiene asociado un control de información sobre herramientas. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**TCS \_ VERTICAL**</dt> </dl>                            | [Versión 4.70.](common-control-versions.md) Las pestañas aparecen en el lado izquierdo del control, con texto de tabulación mostrado verticalmente. Este estilo solo es válido cuando se usa con el estilo \_ MULTILINE de TCS. Para que las pestañas aparezcan en el lado derecho del control, use también el estilo TCS \_ RIGHT. Este estilo no se admite si usa ComCtl32.dll versión 6.<br/> |



## <a name="remarks"></a>Comentarios

Los estilos siguientes se pueden modificar después de crear el control.

-   TCS \_ BOTTOM
-   BOTONES DE TCS \_
-   TCS \_ FIXEDWIDTH
-   TCS \_ FLATBUTTONS
-   TCS \_ FORCEICONLEFT
-   TCS \_ FORCELABELLEFT
-   TCS \_ MULTILINE
-   PROPIETARIO DE \_ TCSDRAWFIXED
-   TCS \_ RAGGEDRIGHT
-   TCS \_ RIGHT
-   TCS \_ VERTICAL

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

