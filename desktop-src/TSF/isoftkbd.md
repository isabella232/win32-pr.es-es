---
title: Interfaz ISoftKbd (Softkbdc. h)
description: Las aplicaciones y los servicios de texto usan la interfaz ISoftKbd para implementar un teclado en pantalla.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- ISoftKbd interface Text Services Framework
- ISoftKbd interface Text Services Framework, descrito
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
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685849"
---
# <a name="isoftkbd-interface"></a>Interfaz ISoftKbd

Las aplicaciones y los servicios de texto usan la interfaz **ISoftKbd** para implementar un teclado en pantalla.

## <a name="members"></a>Miembros

La interfaz **ISoftKbd** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ISoftKbd** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISoftKbd** tiene estos métodos.



| Método                                                                                        | Descripción                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**AdviseSoftKeyboardEventSink**](isoftkbd-advisesoftkeyboardeventsink.md)                   | Instala un receptor de eventos de teclado en pantalla para controlar las notificaciones de OnKeySelection desde el teclado en pantalla.<br/> |
| [**CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md) | Crea una distribución de teclado en pantalla a partir del recurso especificado.<br/>                                        |
| [**CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | Crea una distribución de teclado en pantalla desde el archivo XML especificado.<br/>                                        |
| [**CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)                         | Crea una ventana de teclado en pantalla.<br/>                                                                    |
| [**DestroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)                       | Destruye una ventana de teclado en pantalla.<br/>                                                                   |
| [**EnumSoftKeyboard**](isoftkbd-enumsoftkeyboard.md)                                         | Enumera los posibles teclados de software que admiten el idioma especificado.<br/>                        |
| [**GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)                               | Recupera el color del teclado blando correspondiente al tipo de color proporcionado.<br/>                        |
| [**GetSoftKeyboardPosSize**](isoftkbd-getsoftkeyboardpossize.md)                             | Recupera la posición inicial y el tamaño de un teclado en pantalla.<br/>                                       |
| [**GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)                           | Recupera la fuente de texto utilizada por un teclado en pantalla.<br/>                                                   |
| [**GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)                           | Recupera el modo de tipo para un teclado en pantalla.<br/>                                                       |
| [**Inicialización**](isoftkbd-initialize.md)                                                     | Inicializa todos los campos necesarios para un teclado en pantalla y genera diseños de teclado en pantalla estándar.<br/> |
| [**SelectSoftKeyboard**](isoftkbd-selectsoftkeyboard.md)                                     | Selecciona el teclado en pantalla especificado.<br/>                                                               |
| [**SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)                                 | Establece el texto de la etiqueta del diseño de un teclado en pantalla.<br/>                                           |
| [**SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)           | Establece una combinación de etiqueta y texto que se usa para describir un teclado en pantalla.<br/>                             |
| [**SetSoftKeyboardColors**](isoftkbd-setsoftkeyboardcolors.md)                               | Establece el color del teclado blando correspondiente al tipo de color proporcionado.<br/>                             |
| [**SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)                             | Establece la posición inicial y el tamaño de un teclado en pantalla.<br/>                                            |
| [**SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)                           | Establece la fuente de texto utilizada por un teclado en pantalla.<br/>                                                        |
| [**SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)                           | Establece el modo de tipo para un teclado en pantalla.<br/>                                                            |
| [**ShowKeysForKeyScanMode**](isoftkbd-showkeysforkeyscanmode.md)                             | Muestra las claves utilizadas para el modo de exploración de teclas para un teclado en pantalla.<br/>                                  |
| [**ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)                                         | Muestra un teclado en pantalla.<br/>                                                                          |
| [**UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)               | Quita un receptor de eventos de teclado en pantalla.<br/>                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



 

