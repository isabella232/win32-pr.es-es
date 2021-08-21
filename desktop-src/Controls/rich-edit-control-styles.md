---
title: Estilos de control Rich Edit (Winuser.h)
description: Los siguientes estilos de ventana son únicos para los controles de edición enriquecidos.
ms.assetid: 0f1b3e01-01cb-4b3e-b959-6f32498f0394
topic_type:
- apiref
api_name:
- ES_DISABLENOSCROLL
- ES_EX_NOCALLOLEINIT
- ES_NOIME
- ES_NOOLEDRAGDROP
- ES_SAVESEL
- ES_SELECTIONBAR
- ES_SELFIME
- ES_SUNKEN
- ES_VERTICAL
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc88ea2c3c5d32dff9920b2699474a810f29b14dcf50d9b4c2401863c875778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169095"
---
# <a name="rich-edit-control-styles"></a>Estilos de control Rich Edit

Los siguientes estilos de ventana son únicos para los controles de edición enriquecidos.



| Constante                                                                                                                                                                         | Descripción                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**ES \_ DISABLENOSCROLL**</dt> </dl>     | Deshabilita las barras de desplazamiento en lugar de ocultarlas cuando no son necesarias.<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**ES \_ EX \_ NOCALLOLEINIT**</dt> </dl> | Impide que el control llame a [**la función OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) cuando se crea. Este estilo de ventana solo es útil en las plantillas de diálogo porque [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) no acepta este estilo.<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**ES \_ NOIME**</dt> </dl>                                | Deshabilita la operación IME. Este estilo solo está disponible para la compatibilidad con idiomas asiáticos.<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**ES \_ NOOLEDRAGDROP**</dt> </dl>           | Deshabilita la compatibilidad con arrastrar y colocar objetos OLE.<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**ES \_ SAVESEL**</dt> </dl>                             | Conserva la selección cuando el control pierde el foco. De forma predeterminada, todo el contenido del control se selecciona cuando recupera el foco.<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**ES \_ SELECTIONBAR**</dt> </dl>              | Agrega espacio al margen izquierdo donde el cursor cambia a una flecha hacia la derecha, lo que permite al usuario seleccionar líneas de texto completa. <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**ES \_ SELFIME**</dt> </dl>                          | Dirige el control de edición enriquecido para permitir que la aplicación controle todas las operaciones de IME. Este estilo solo está disponible para la compatibilidad con idiomas asiáticos.<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**ES \_ SUNKEN**</dt> </dl>                                | Muestra el control con un estilo de borde bloqueado para que el control de edición enriquecido aparezca en su ventana primaria. <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**ES \_ VERTICAL**</dt> </dl>                          | Dibuja texto y objetos en una dirección vertical. Este estilo solo está disponible para la compatibilidad en idioma asiático.<br/>                                                                                                                                 |



Los controles de edición enriquecciones también admiten los siguientes estilos de control de edición.



| Constante                                                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**ES \_ AUTOHSCROLL**</dt> </dl> | Desplaza automáticamente el texto a la derecha en 10 caracteres cuando el usuario tipos un carácter al final de la línea. Cuando el usuario presiona la tecla ENTRAR, el control vuelve a desplazar todo el texto a la posición cero.<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**ES \_ AUTOVSCROLL**</dt> </dl> | Desplaza automáticamente el texto hacia arriba una página cuando el usuario presiona la tecla ENTRAR en la última línea.<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**CENTRO DE ES \_**</dt> </dl>                | Centra el texto en un control de edición de una o varias líneas.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**ES \_ LEFT**</dt> </dl>                      | A la izquierda se alinea el texto.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**ES \_ MULTILINE**</dt> </dl>       | Designa un control de edición multilínea. El valor predeterminado es el control de edición de una sola línea.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**ES \_ NOHIDESEL**</dt> </dl>       | Nega el comportamiento predeterminado de un control de edición. El comportamiento predeterminado oculta la selección cuando el control pierde el foco de entrada e invierte la selección cuando el control recibe el foco de entrada. Si especifica [**ES \_ NOHIDESEL**](edit-control-styles.md), el texto seleccionado se invierte, incluso si el control no tiene el foco.<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**NÚMERO DE ES \_**</dt> </dl>                | Permite especificar solo dígitos en el control de edición.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**CONTRASEÑA DE \_ ES**</dt> </dl>          | Muestra un asterisco ( \* ) para cada carácter que se escribe en el control de edición. Este estilo solo es válido para controles de edición de una sola línea.<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**ES \_ READONLY**</dt> </dl>          | Impide que el usuario escriba o edite texto en el control de edición.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**ES \_ RIGHT**</dt> </dl>                   | A la derecha alinea el texto en un control de edición de una o varias líneas.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**ES \_ WANTRETURN**</dt> </dl>    | Especifica que se inserte un retorno de carro cuando el usuario presione la tecla ENTRAR mientras escribe texto en un control de edición multilínea en un cuadro de diálogo. Si no especifica este estilo, presionar la tecla ENTRAR tiene el mismo efecto que presionar el botón de inserción predeterminado del cuadro de diálogo. Este estilo no tiene ningún efecto en un control de edición de una sola línea.<br/>                   |



Los controles rich edit no admiten los siguientes estilos de control de edición.

-   [**ES \_ MINÚSCULAS**](edit-control-styles.md)
-   [**ES \_ OEMCONVERT**](edit-control-styles.md)
-   [**ES \_ MAYÚSCULA**](edit-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser.h</dt> </dl> |



 

