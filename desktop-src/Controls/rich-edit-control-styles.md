---
title: Estilos de control Rich Edit (Winuser. h)
description: Los siguientes estilos de ventana son exclusivos de los controles Rich Edit.
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
ms.openlocfilehash: 620f73beb726eea065d8c8a63a635ff04fdeba37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660555"
---
# <a name="rich-edit-control-styles"></a>Estilos de control Rich Edit

Los siguientes estilos de ventana son exclusivos de los controles Rich Edit.



| Constante                                                                                                                                                                         | Descripción                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**s \_ DISABLENOSCROLL**</dt> </dl>     | Deshabilita las barras de desplazamiento en lugar de ocultarlas cuando no se necesitan.<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**ES \_ ex \_ NOCALLOLEINIT**</dt> </dl> | Impide que el control llame a la función [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) cuando se crea. Este estilo de ventana solo es útil en las plantillas de cuadro de diálogo porque [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) no acepta este estilo.<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**S \_ NOIME**</dt> </dl>                                | Deshabilita la operación IME. Este estilo solo está disponible para la compatibilidad con idiomas asiáticos.<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**s \_ NOOLEDRAGDROP**</dt> </dl>           | Deshabilita la compatibilidad para arrastrar y colocar objetos OLE.<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**s \_ SAVESEL**</dt> </dl>                             | Conserva la selección cuando el control pierde el foco. De forma predeterminada, se selecciona todo el contenido del control cuando vuelve a obtener el foco.<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**s \_ SELECTIONBAR**</dt> </dl>              | Agrega espacio al margen izquierdo en el que el cursor cambia a una flecha de la derecha, lo que permite al usuario seleccionar líneas de texto completas. <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**S \_ SELFIME**</dt> </dl>                          | Dirige el control Rich Edit para permitir que la aplicación controle todas las operaciones del IME. Este estilo solo está disponible para la compatibilidad con idiomas asiáticos.<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**ES \_ hundido**</dt> </dl>                                | Muestra el control con un estilo de borde hundido para que el control Rich Edit aparezca empotrado en la ventana primaria. <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**ES \_ vertical**</dt> </dl>                          | Dibuja texto y objetos en una dirección vertical. Este estilo solo está disponible para la compatibilidad con idiomas asiáticos.<br/>                                                                                                                                 |



Los controles Rich Edit también admiten los siguientes estilos de control de edición.



| Constante                                                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**s \_ AUTOHSCROLL**</dt> </dl> | Desplaza automáticamente el texto a la derecha 10 caracteres cuando el usuario escribe un carácter al final de la línea. Cuando el usuario presiona la tecla entrar, el control vuelve a desplazar todo el texto hasta la posición cero.<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**s \_ AUTOVSCROLL**</dt> </dl> | Desplaza automáticamente el texto una página cuando el usuario presiona la tecla entrar en la última línea.<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**Centro de ES \_**</dt> </dl>                | Centra el texto en un control de edición de línea única o multilínea.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**ES \_ izquierda**</dt> </dl>                      | Alinea el texto a la izquierda.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**ES \_ multilínea**</dt> </dl>       | Designa un control de edición multilínea. El valor predeterminado es el control de edición de una sola línea.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**s \_ NOHIDESEL**</dt> </dl>       | Niega el comportamiento predeterminado de un control de edición. El comportamiento predeterminado oculta la selección cuando el control pierde el foco de entrada e invierte la selección cuando el control recibe el foco de entrada. Si especifica [**es \_ NOHIDESEL**](edit-control-styles.md), se invierte el texto seleccionado, incluso si el control no tiene el foco.<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**número de ES \_**</dt> </dl>                | Permite que solo se escriban dígitos en el control de edición.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**contraseña de ES \_**</dt> </dl>          | Muestra un asterisco ( \* ) para cada carácter que se escribe en el control de edición. Este estilo solo es válido para los controles de edición de una sola línea.<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**ES de \_ solo lectura**</dt> </dl>          | Impide que el usuario escriba o modifique texto en el control de edición.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**ES \_ derecha**</dt> </dl>                   | Alinea a la derecha el texto en un control de edición de línea única o multilínea.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**s \_ WANTRETURN**</dt> </dl>    | Especifica que se inserte un retorno de carro cuando el usuario presione la tecla entrar mientras escribe texto en un control de edición multilínea en un cuadro de diálogo. Si no especifica este estilo, presionar la tecla entrar tiene el mismo efecto que presionar el botón de opción predeterminado del cuadro de diálogo. Este estilo no tiene ningún efecto en un control de edición de una sola línea.<br/>                   |



Los controles Rich Edit no admiten los siguientes estilos de control de edición.

-   [**s en \_ minúsculas**](edit-control-styles.md)
-   [**s \_ OEMCONVERT**](edit-control-styles.md)
-   [**ES en \_ mayúsculas**](edit-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

