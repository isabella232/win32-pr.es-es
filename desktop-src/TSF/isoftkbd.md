---
title: Interfaz ISoftKbd (Softkbdc.h)
description: Las aplicaciones y los servicios de texto usan la interfaz ISoftKbd para implementar un teclado suave.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Interfaz ISoftKbd Text Services Framework
- Interfaz ISoftKbd Text Services Framework , descrito
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a1bc49be78262e8d78f32c87dd2bc93b6c1405ec444329f908c8f41319e3d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952393"
---
# <a name="isoftkbd-interface"></a>Interfaz ISoftKbd

Las aplicaciones y los servicios de texto usan la interfaz **ISoftKbd** para implementar un teclado suave.

## <a name="members"></a>Miembros

La **interfaz ISoftKbd** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ISoftKbd** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISoftKbd** tiene estos métodos.



| Método                                                                                        | Descripción                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**AdviseSoftKeyboardEventSink**](isoftkbd-advisesoftkeyboardeventsink.md)                   | Instala un receptor de eventos de teclado soft para controlar las notificaciones OnKeySelection desde el teclado soft.<br/> |
| [**CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md) | Crea un diseño de teclado flexible a partir del recurso especificado.<br/>                                        |
| [**CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | Crea un diseño de teclado flexible a partir del archivo XML especificado.<br/>                                        |
| [**CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)                         | Crea una ventana de teclado flexible.<br/>                                                                    |
| [**DestroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)                       | Destruye una ventana de teclado suave.<br/>                                                                   |
| [**EnumSoftKeyboard**](isoftkbd-enumsoftkeyboard.md)                                         | Enumera los posibles teclados flexibles que admiten el idioma especificado.<br/>                        |
| [**GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)                               | Recupera el color del teclado suave correspondiente al tipo de color proporcionado.<br/>                        |
| [**GetSoftKeyboardPosSize**](isoftkbd-getsoftkeyboardpossize.md)                             | Recupera la posición inicial y el tamaño de un teclado suave.<br/>                                       |
| [**GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)                           | Recupera la fuente de texto utilizada por un teclado flexible.<br/>                                                   |
| [**GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)                           | Recupera el modo de tipo de un teclado flexible.<br/>                                                       |
| [**Inicialización**](isoftkbd-initialize.md)                                                     | Inicializa todos los campos necesarios para un teclado suave y genera diseños de teclado soft estándar.<br/> |
| [**SeleccioneSoftKeyboard.**](isoftkbd-selectsoftkeyboard.md)                                     | Selecciona el teclado soft especificado.<br/>                                                               |
| [**SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)                                 | Establece el texto de etiqueta del diseño de un teclado suave.<br/>                                           |
| [**SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)           | Establece una combinación de etiqueta y texto que se usa para describir un teclado suave.<br/>                             |
| [**SetSoftKeyboardColors**](isoftkbd-setsoftkeyboardcolors.md)                               | Establece el color del teclado suave correspondiente al tipo de color proporcionado.<br/>                             |
| [**SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)                             | Establece la posición inicial y el tamaño de un teclado suave.<br/>                                            |
| [**SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)                           | Establece la fuente de texto utilizada por un teclado flexible.<br/>                                                        |
| [**SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)                           | Establece el modo de tipo para un teclado suave.<br/>                                                            |
| [**ShowKeysForKeyScanMode**](isoftkbd-showkeysforkeyscanmode.md)                             | Muestra las teclas usadas para el modo de examen de teclas para un teclado suave.<br/>                                  |
| [**ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)                                         | Muestra un teclado suave.<br/>                                                                          |
| [**UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)               | Quita un receptor de eventos de teclado suave.<br/>                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



 

