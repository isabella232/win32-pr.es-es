---
title: Estilos de botón (Winuser.h)
description: Especifica una combinación de estilos de botón. Si crea un botón con la clase BUTTON con las funciones CreateWindow o CreateWindowEx, puede especificar cualquiera de los estilos de botón que se enumeran a continuación.
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
ms.openlocfilehash: 60419d947036516e093d481f3fc0d8caa097671c13bd4fe3fc8e95d21cc3cb83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832485"
---
# <a name="button-styles"></a>Estilos de botón

Especifica una combinación de estilos de botón. Si crea un botón mediante la clase BUTTON con las funciones [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) puede especificar cualquiera de los estilos de botón que se enumeran a continuación.

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
Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) en GitHub.


## <a name="constants"></a>Constantes
| Constante                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**BS \_ 3STATE**</dt> </dl>                            | Crea un botón que es el mismo que una casilla, salvo que la casilla puede estar atenuada, así como activada o desactivada. Use el estado atenuado para mostrar que el estado de la casilla no está determinado.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**BS \_ AUTO3STATE**</dt> </dl>                | Crea un botón que es el mismo que una casilla de tres estados, salvo que la casilla cambia de estado cuando el usuario lo selecciona. El estado se pasa por comprobado, indeterminado y borrado.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**BS \_ AUTOCHECKBOX**</dt> </dl>          | Crea un botón que es el mismo que una casilla, salvo que el estado de comprobación alterna automáticamente entre activado y desactivado cada vez que el usuario activa la casilla.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**BS \_ AUTORADIOBUTTON**</dt> </dl> | Crea un botón que es el mismo que un botón de radio, salvo que cuando el usuario lo selecciona, el sistema establece automáticamente el estado de comprobación del botón en activado y establece automáticamente el estado de comprobación de todos los demás botones del mismo grupo que se borrarán.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**MAPA DE BITS DE BS \_**</dt> </dl>                            | Especifica que el botón muestra un mapa de bits. Consulte la sección Comentarios para ver su interacción con BS \_ ICON.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**BS \_ BOTTOM**</dt> </dl>                            | Coloca el texto en la parte inferior del rectángulo del botón.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**CENTRO DE \_ BS**</dt> </dl>                            | Centra el texto horizontalmente en el rectángulo del botón.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**CASILLA \_ BS**</dt> </dl>                      | Crea una casilla pequeña y vacía con texto. De forma predeterminada, el texto se muestra a la derecha de la casilla. Para mostrar el texto a la izquierda de la casilla, combine esta marca con el estilo LEFTTEXT de BS (o con el estilo RIGHTBUTTON de \_ BS \_ equivalente).<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**BS \_ COMMANDLINK**</dt> </dl>             | Crea un botón de vínculo de comando que se comporta como un botón de estilo PUSHBUTTON de BS, pero el botón de vínculo de comando tiene una flecha verde a la izquierda que apunta al \_ texto del botón. Se puede establecer un título para el texto del botón mediante el envío del mensaje SETNOTE de BCM \_ al botón.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**BS \_ DEFCOMMANDLINK**</dt> </dl>    | Crea un botón de vínculo de comando que se comporta como un botón de estilo \_ PUSHBUTTON de BS. Si el botón está en un cuadro de diálogo, el usuario puede seleccionar el botón de vínculo de comando presionando la tecla ENTRAR, incluso cuando el botón de vínculo de comando no tenga el foco de entrada. Este estilo es útil para permitir que el usuario seleccione rápidamente la opción más probable (predeterminada).<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**BS \_ DEFPUSHBUTTON**</dt> </dl>       | Crea un botón de inserción que se comporta como un botón de estilo PUSHBUTTON de \_ BS, pero tiene una apariencia distinta. Si el botón está en un cuadro de diálogo, el usuario puede seleccionarlo presionando la tecla ENTRAR, incluso cuando el botón no tenga el foco de entrada. Este estilo es útil para permitir que el usuario seleccione rápidamente la opción más probable (predeterminada).<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**BS \_ DEFSPLITBUTTON**</dt> </dl>    | Crea un botón de división que se comporta como un botón de estilo PUSHBUTTON de BS, pero \_ también tiene un aspecto distintivo. Si el botón de división está en un cuadro de diálogo, el usuario puede seleccionar el botón de división presionando la tecla ENTRAR, incluso cuando el botón de división no tenga el foco de entrada. Este estilo es útil para permitir que el usuario seleccione rápidamente la opción más probable (predeterminada).<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**BS \_ GROUPBOX**</dt> </dl>                      | Crea un rectángulo en el que se pueden agrupar otros controles. Cualquier texto asociado a este estilo se muestra en la esquina superior izquierda del rectángulo.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**ICONO \_ DE BS**</dt> </dl>                                  | Especifica que el botón muestra un icono. Vea la sección Comentarios para ver su interacción con BS \_ BITMAP.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ FLAT**</dt> </dl>                                  | Especifica que el botón es bidimensional; no usa el sombreado predeterminado para crear una imagen 3D. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**BS \_ LEFT**</dt> </dl>                                  | Justifica a la izquierda el texto en el rectángulo del botón. Sin embargo, si el botón es una casilla o un botón de radio que no tiene el estilo RIGHTBUTTON de BS, el texto se justifica a la izquierda en el lado derecho de la casilla o el botón \_ de radio.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**BS \_ LEFTTEXT**</dt> </dl>                      | Coloca texto en el lado izquierdo del botón de radio o la casilla cuando se combina con un botón de radio o un estilo de casilla. Igual que el estilo \_ RIGHTBUTTON de BS.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**BS \_ MULTILINE**</dt> </dl>                   | Ajusta el texto del botón a varias líneas si la cadena de texto es demasiado larga para caber en una sola línea del rectángulo del botón.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**NOTIFICACIÓN \_ DE BS**</dt> </dl>                            | Habilita un botón para enviar códigos [de notificación \_ KILLFOCUS](bn-killfocus.md) y [ \_ BN SETFOCUS](bn-setfocus.md) de BN a su ventana primaria. <br/> Tenga en cuenta que los botones envían [el código de notificación \_ CLICKED](bn-clicked.md) de BN independientemente de si tiene este estilo. Para obtener [los códigos de notificación \_ DBLCLK de BN,](bn-dblclk.md) el botón debe tener el estilo BS RADIOBUTTON o \_ BS \_ OWNERDRAW.<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**BS \_ OWNERDRAW**</dt> </dl>                   | Crea un botón dibujado por el propietario. La ventana de propietario recibe [**un mensaje \_ DRAWITEM de WM**](wm-drawitem.md) cuando ha cambiado un aspecto visual del botón. No combine el estilo BS \_ OWNERDRAW con ningún otro estilo de botón.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**BOTÓN \_ PUSHBUTTON DE BS**</dt> </dl>                | Crea un botón de inserción que envía un [**mensaje \_ WM COMMAND**](/windows/desktop/menurc/wm-command) a la ventana de propietario cuando el usuario selecciona el botón.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**BS \_ PUSHLIKE**</dt> </dl>                      | Hace que un botón (como una casilla, una casilla de tres estados o un botón de radio) tenga un aspecto y actúe como un botón de inserción. El botón se genera cuando no se inserta ni se comprueba, y se desconsolla cuando se inserta o se comprueba.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**BS \_ RADIOBUTTON**</dt> </dl>             | Crea un círculo pequeño con texto. De forma predeterminada, el texto se muestra a la derecha del círculo. Para mostrar el texto a la izquierda del círculo, combine esta marca con el estilo LEFTTEXT de BS (o con el estilo RIGHTBUTTON de \_ BS \_ equivalente). Use botones de radio para grupos de opciones relacionadas, pero mutuamente excluyentes.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**BS \_ RIGHT**</dt> </dl>                               | Justifica el texto a la derecha en el rectángulo del botón. Sin embargo, si el botón es una casilla o un botón de radio que no tiene el estilo RIGHTBUTTON de BS, el texto se justifica a la derecha en el lado derecho de la casilla o el botón \_ de radio.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**BS \_ RIGHTBUTTON**</dt> </dl>             | Coloca el círculo de un botón de radio o el cuadrado de una casilla en el lado derecho del rectángulo del botón. Igual que el estilo \_ LEFTTEXT de BS.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**BS \_ SPLITBUTTON**</dt> </dl>             | Crea un botón de división. Un botón de división tiene una flecha desplegable.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**TEXTO DE \_ BS**</dt> </dl>                                  | Especifica que el botón muestra texto.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**BS \_ TOP**</dt> </dl>                                     | Coloca el texto en la parte superior del rectángulo del botón.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**MÁSCARA DE TIPOS DE BS \_**</dt> </dl>                      | No use este estilo. Bit de estilo compuesto que resulta del uso del operador OR en bits de \_ \* estilo BS. Se puede usar para enmascarar bits BS \_ \* válidos de una máscara de bits determinada. Tenga en cuenta que esto no está actualizado y no incluye correctamente todos los estilos válidos. Por lo tanto, no debe usar este estilo.<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**BS \_ USERBUTTON**</dt> </dl>                | Obsoleto, pero proporcionado por compatibilidad con versiones de 16 bits de Windows. Las aplicaciones deben usar BS \_ OWNERDRAW en su lugar.<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**BS \_ VCENTER**</dt> </dl>                         | Coloca el texto en el centro (verticalmente) del rectángulo del botón.<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>Comentarios

Para obtener ilustraciones de los estilos de botón principal, como BS \_ CHECKBOX y BS \_ GROUPBOX, vea [Tipos de botón](button-types-and-styles.md).

La apariencia del texto o de un icono o ambos en un control de botón depende de los estilos BS ICON y BS BITMAP, y de si se envía el mensaje \_ \_ BM [**\_ SETIMAGE.**](bm-setimage.md) Los resultados posibles son los siguientes.



| ¿Icono de BS \_ o conjunto de mapas de bits de BS? \_ | ¿Se ha llamado a BM \_ SETIMAGE? | Resultado              |
|-----------------------------|----------------------|---------------------|
| Sí                         | Sí                  | Mostrar solo icono.     |
| No                          | Sí                  | Mostrar icono y texto. |
| Sí                         | No                   | Mostrar solo texto.     |
| No                          | No                   | Mostrar solo texto      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser.h</dt> </dl> |



 

