---
title: Estilos de botón (Winuser. h)
description: Especifica una combinación de estilos de botón. Si crea un botón mediante la clase BUTTON con la función CreateWindow o CreateWindowEx, puede especificar cualquiera de los estilos de botón que se enumeran a continuación.
ms.assetid: 30254cb5-43cd-407f-8ad6-bd7f9ec3edc7
topic_type:
- apiref
api_name:
- BS_3STATE
- BS_AUTO3STATE
- BS_AUTOCHECKBOX
- BS_AUTORADIOBUTTON
- BS_BITMAP
- BS_BOTTOM
- BS_CENTER
- BS_CHECKBOX
- BS_COMMANDLINK
- BS_DEFCOMMANDLINK
- BS_DEFPUSHBUTTON
- BS_DEFSPLITBUTTON
- BS_GROUPBOX
- BS_ICON
- BS_FLAT
- BS_LEFT
- BS_LEFTTEXT
- BS_MULTILINE
- BS_NOTIFY
- BS_OWNERDRAW
- BS_PUSHBUTTON
- BS_PUSHLIKE
- BS_RADIOBUTTON
- BS_RIGHT
- BS_RIGHTBUTTON
- BS_SPLITBUTTON
- BS_TEXT
- BS_TOP
- BS_TYPEMASK
- BS_USERBUTTON
- BS_VCENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 2b0054920f3cb2ae323a9655b1b028da473e119f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653560"
---
# <a name="button-styles"></a>Estilos de botón

Especifica una combinación de estilos de botón. Si crea un botón mediante la clase BUTTON con la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , puede especificar cualquiera de los estilos de botón que se enumeran a continuación.

## <a name="example"></a>Ejemplo

```cpp
HRESULT Button::CreateText(HWND hParent, const TCHAR *szCaption, int nID, 
                               const Rect& rcBound)
{
    CREATESTRUCT create;
    ZeroMemory(&create, sizeof(CREATESTRUCT));

    create.x = rcBound.left;
    create.y = rcBound.top;
    create.cx = rcBound.right - create.x;
    create.cy = rcBound.bottom - create.y;

    create.hwndParent = hParent;
    create.lpszName = szCaption;
    create.hMenu = (HMENU)(INT_PTR)nID;
    create.lpszClass = TEXT("BUTTON");
    create.style = BS_PUSHBUTTON | BS_FLAT;
    return Control::Create(create);
}
```
Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) en github.


## <a name="constants"></a>Constantes
| Constante                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**\_3STATE BS**</dt> </dl>                            | Crea un botón que es igual que una casilla, con la excepción de que el cuadro puede estar atenuado, así como estar activado o desactivado. Use el estado atenuado para mostrar que no se determina el estado de la casilla.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**\_AUTO3STATE BS**</dt> </dl>                | Crea un botón que es igual que una casilla de tres Estados, salvo que el cuadro cambia su estado cuando el usuario lo selecciona. El estado se recorre como activado, indeterminado y desactivado.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**CASILLA BS automarca \_**</dt> </dl>          | Crea un botón que es igual que una casilla, con la excepción de que el estado de activación alterna automáticamente entre activado y desactivado cada vez que el usuario activa la casilla.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**autoradiobutton de BS \_**</dt> </dl> | Crea un botón que es igual que un botón de radio, salvo que cuando el usuario lo selecciona, el sistema establece automáticamente el estado de activación del botón en activado y establece automáticamente el estado de activación de los demás botones del mismo grupo en desactivado.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**\_mapa de bits BS**</dt> </dl>                            | Especifica que el botón muestra un mapa de bits. Vea la sección Comentarios para su interacción con el \_ icono de BS.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**inferior a BS \_**</dt> </dl>                            | Coloca el texto en la parte inferior del rectángulo del botón.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**Centro de BS \_**</dt> </dl>                            | Centra el texto horizontalmente en el rectángulo del botón.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**\_casilla BS**</dt> </dl>                      | Crea una pequeña casilla vacía con texto. De forma predeterminada, el texto se muestra a la derecha de la casilla. Para mostrar el texto a la izquierda de la casilla, combine esta marca con el estilo BS \_ LEFTTEXT (o con el estilo de BS \_ RIGHTBUTTON equivalente).<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**\_COMMANDLINK BS**</dt> </dl>             | Crea un botón de vínculo de comando que se comporta como un \_ botón de estilo de pulsador de BS, pero el botón de vínculo de comando tiene una flecha verde a la izquierda que apunta al texto del botón. Se puede establecer un título para el texto del botón enviando el \_ mensaje SETNOTE de BCM al botón.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**\_DEFCOMMANDLINK BS**</dt> </dl>    | Crea un botón de vínculo de comando que se comporta como un \_ botón de estilo de pulsador de BS. Si el botón está en un cuadro de diálogo, el usuario puede seleccionar el botón de vínculo de comando presionando la tecla entrar, aunque el botón de vínculo de comando no tenga el foco de entrada. Este estilo es útil para permitir al usuario seleccionar rápidamente la opción más probable (valor predeterminado).<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**\_DEFPUSHBUTTON BS**</dt> </dl>       | Crea un botón de reenvío que se comporta como un \_ botón de estilo de pulsación de BS, pero tiene una apariencia distinta. Si el botón está en un cuadro de diálogo, el usuario puede seleccionar el botón presionando la tecla entrar, incluso cuando el botón no tiene el foco de entrada. Este estilo es útil para permitir al usuario seleccionar rápidamente la opción más probable (valor predeterminado).<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**\_DEFSPLITBUTTON BS**</dt> </dl>    | Crea un botón de expansión que se comporta como un \_ botón de estilo de pulsación de BS, pero también tiene un aspecto distintivo. Si el botón de expansión está en un cuadro de diálogo, el usuario puede seleccionar el botón de expansión presionando la tecla entrar, incluso cuando el botón de expansión no tenga el foco de entrada. Este estilo es útil para permitir al usuario seleccionar rápidamente la opción más probable (valor predeterminado).<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**\_GROUPBOX (GROUPBOX)**</dt> </dl>                      | Crea un rectángulo en el que se pueden agrupar otros controles. Cualquier texto asociado a este estilo se muestra en la esquina superior izquierda del rectángulo.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**icono de BS \_**</dt> </dl>                                  | Especifica que el botón muestra un icono. Vea la sección Comentarios para su interacción con el \_ mapa de bits BS.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ plano**</dt> </dl>                                  | Especifica que el botón es bidimensional; no utiliza el sombreado predeterminado para crear una imagen 3D. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**BS a la \_ izquierda**</dt> </dl>                                  | Justifica a la izquierda el texto del rectángulo del botón. Sin embargo, si el botón es una casilla o un botón de radio que no tiene el \_ estilo BS RIGHTBUTTON, el texto se alinea a la derecha en el lado derecho de la casilla o botón de radio.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**\_LEFTTEXT BS**</dt> </dl>                      | Coloca el texto en el lado izquierdo del botón de radio o la casilla cuando se combina con un botón de radio o un estilo de casilla. Igual que el \_ estilo BS RIGHTBUTTON.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**BS \_ multilínea**</dt> </dl>                   | Ajusta el texto del botón en varias líneas si la cadena de texto es demasiado larga para caber en una sola línea del rectángulo del botón.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**notificación de BS \_**</dt> </dl>                            | Habilita un botón para enviar los códigos de notificación [BN \_ KILLFOCUS](bn-killfocus.md) y [BN \_ SETFOCUS](bn-setfocus.md) a su ventana primaria. <br/> Tenga en cuenta que los botones envían el código de notificación en el que se ha [ \_ hecho clic BN](bn-clicked.md) independientemente de si tiene este estilo. Para obtener los códigos de notificación de [BN \_ DBLCLK](bn-dblclk.md) , el botón debe tener el estilo de estilo de la opción BS \_ o de \_ tipo OWNERDRAW.<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**OWNERDRAW de BS \_**</dt> </dl>                   | Crea un botón dibujado por el propietario. La ventana propietaria recibe un mensaje de Windows de [**WM \_**](wm-drawitem.md) cuando ha cambiado un aspecto visual del botón. No combine el estilo de \_ OWNERDRAW BS con ningún otro estilo de botón.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**\_pulsador de BS**</dt> </dl>                | Crea un botón de comando que envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) a la ventana propietaria cuando el usuario selecciona el botón.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**\_PUSHLIKE BS**</dt> </dl>                      | Hace que un botón (por ejemplo, una casilla de verificación, una casilla de tres Estados o un botón de radio) tenga el aspecto y actúe como un botón de inserción. Se produce el botón cuando no se inserta o se activa y se hundi cuando se inserta o se activa.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**RADIOBUTTON de BS \_**</dt> </dl>             | Crea un círculo pequeño con texto. De forma predeterminada, el texto se muestra a la derecha del círculo. Para mostrar el texto a la izquierda del círculo, combine esta marca con el estilo BS \_ LEFTTEXT (o con el \_ estilo BS RIGHTBUTTON equivalente). Use los botones de radio para los grupos de opciones relacionadas, pero mutuamente excluyentes.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**\_derecho BS**</dt> </dl>                               | Alinea a la derecha el texto en el rectángulo del botón. Sin embargo, si el botón es una casilla o un botón de radio que no tiene el \_ estilo BS RIGHTBUTTON, el texto se justifica a la derecha en el lado derecho de la casilla o botón de radio.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**\_RIGHTBUTTON BS**</dt> </dl>             | Coloca el círculo o la casilla de un botón de radio en el lado derecho del rectángulo del botón. Igual que el \_ estilo BS LEFTTEXT.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**División de BS \_**</dt> </dl>             | Crea un botón de expansión. Un botón de expansión tiene una flecha desplegable.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**\_texto BS**</dt> </dl>                                  | Especifica que el botón muestra texto.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**superior a BS \_**</dt> </dl>                                     | Coloca el texto en la parte superior del rectángulo del botón.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**\_TYPEMASK BS**</dt> </dl>                      | No utilice este estilo. Bit de estilo compuesto que es el resultado de utilizar el operador OR en \_ \* bits de estilo BS. Se puede usar para enmascarar los bits BS válidos a \_ \* partir de una máscara de bits determinada. Tenga en cuenta que esto no está actualizado y no incluye correctamente todos los estilos válidos. Por lo tanto, no debe usar este estilo.<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**\_USERBUTTON BS**</dt> </dl>                | Obsoleto, pero se proporciona por compatibilidad con las versiones de 16 bits de Windows. En su lugar, las aplicaciones deben usar el \_ OWNERDRAW BS.<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**BS \_ vCenter**</dt> </dl>                         | Coloca el texto en el centro (verticalmente) del rectángulo del botón.<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>Observaciones

Para ver las ilustraciones de los estilos de botón principal, como BS \_ CheckBox y BS \_ GROUPBOX, consulte [tipos de botón](button-types-and-styles.md).

La apariencia del texto o de un icono o de ambos en un control de botón depende del icono de BS y de los \_ \_ estilos de mapa de bits BS, y de si se envía el mensaje de el [**\_ SETIMAGE de BM**](bm-setimage.md) . Los resultados posibles son los siguientes.



| \_¿Icono de BS \_ o conjunto de mapas de bits BS? | Se \_ llamó a la BM SETIMAGE? | Resultado              |
|-----------------------------|----------------------|---------------------|
| Sí                         | Sí                  | Mostrar solo el icono.     |
| No                          | Sí                  | Mostrar el icono y el texto. |
| Sí                         | No                   | Mostrar solo texto.     |
| No                          | No                   | Mostrar solo texto      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

