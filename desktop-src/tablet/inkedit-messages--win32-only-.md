---
description: El control InkEdit es una super class del control RichEdit.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: InkEdit Messages (solo Win32)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cb1d390bf8e37d6affbbd96c34c53ea889b268
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475041"
---
# <a name="inkedit-messages-win32-only"></a>InkEdit Messages (solo Win32)

El [control InkEdit](inkedit-control-reference.md) es una super class del control [**RichEdit.**](/windows/desktop/api/richole/nn-richole-iricheditole) Cada **mensaje RichEdit** se pasa, directamente en la mayoría de los casos, y tiene exactamente el mismo efecto que en **RichEdit**. Esto también se aplica a los mensajes de notificación de eventos.

Para enviar estos mensajes, llame a la función SendMessage con los parámetros siguientes:




| C++ | 
|-----|
| <pre data-space="preserve"><code>LRESULT SendMessage(  HWND hWnd,      // handle to destination window  UINT Msg,       // message  WPARAM wParam,  // first message parameter  LPARAM lParam   // second message parameter);</code></pre> | 




 

## <a name="message"></a>Message

La ventana primaria del control [InkEdit](inkedit-control-reference.md) recibe mensajes de notificación de eventos a través del mensaje \_ WM NOTIFY:


```C++
LRESULT CALLBACK WindowProc(
    HWND hWnd,                // handle to window
    UINT uMsg,                // WM_NOTIFY
    WPARAM wParam,        // InkEdit control identifier
    LPARAM lParam            // see documentation for notification messages
);
```





| Obtener o establecer mensaje                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EM \_ GETINKMODE<br/>           | Obtiene el modo de entrada manuscrita del control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* y *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve uno de los valores definidos en la enumeración [**InkMode,**](/windows/desktop/api/inked/ne-inked-inkmode) que especifica si la colección de lápiz está deshabilitada, si se recopila la entrada de lápiz o si se recopilan la entrada de lápiz y los gestos.<br/>                                                                                                                                                                                                                                                         |
| EM \_ SETINKMODE<br/>           | Establece el modo de entrada manuscrita del control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/>*wParam* Especifica uno de los valores de la enumeración [**InkMode,**](/windows/desktop/api/inked/ne-inked-inkmode) que especifica si la colección de entrada de lápiz está deshabilitada, si se recopila la entrada de lápiz o si se recopilan la entrada de lápiz y los gestos.<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/> Comentarios:<br/> Esto solo se debe usar si EM \_ GETSTATUS devuelve IES \_ Idle.<br/>                                                                                                               |
| EM \_ GETINKINSERTMODE<br/>     | Obtiene el modo de inserción de lápiz del control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* y *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve uno de los valores de la enumeración [**InkInsertMode,**](/windows/desktop/api/inked/ne-inked-inkinsertmode) que especifica si la entrada manuscrita se inserta en el control como texto o como entrada de lápiz.<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETINKINSERTMODE<br/>     | Establece el modo de inserción de lápiz del control [InkEdit.](inkedit-control-reference.md) El envío de este mensaje no tiene ningún efecto si se usa con cualquier sistema operativo instalado que no sea Microsoft Windows XP Tablet PC Edition.<br/> Parámetros:<br/>*wParam* Especifica uno de los valores de la enumeración [**InkInsertMode,**](/windows/desktop/api/inked/ne-inked-inkinsertmode) que especifica si la entrada de lápiz se inserta en el control como texto o como entrada de lápiz.<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                       |
| EM \_ GETDRAWATTR<br/>          | Obtiene los atributos de dibujo actuales del control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/>*wParam* Este parámetro no se utiliza; debe ser 0.<br/>*lParam* Especifica un puntero (IInkDrawingAttributes \* \* pDrawAttr) para recibir el objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) actual.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                |
| EM \_ SETDRAWATTR<br/>          | Establece los atributos de dibujo que se usarán para futuras colecciones de lápiz.<br/> Parámetros:<br/>*wParam* Este parámetro no se utiliza; debe ser 0.<br/>*lParam* Especifica un puntero (IInkDrawingAttributes \* pDrawAttr) a un [**objeto InkDrawingAttributes.**](inkdrawingattributes-class.md)<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                  |
| EM \_ GETRECOTIMEOUT<br/>       | Obtiene el tiempo de espera de reconocimiento, en milisegundos, para el control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* y *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve el tiempo de espera de reconocimiento, en milisegundos.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ SETRECOTIMEOUT<br/>       | Establece el tiempo de espera de reconocimiento, en milisegundos, para el control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/>*wParam* Especifica el tiempo de espera de reconocimiento, en milisegundos.<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                                                    |
| EM \_ GETGESTURESTATUS<br/>     | Obtiene el estado del gesto para el control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/>*wParam* Especifica el tipo de gesto, tal como se define en la [**enumeración InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve **TRUE si** el control [InkEdit](inkedit-control-reference.md) se suscribe al gesto o **FALSE** si el control InkEdit no se suscribe al gesto.<br/>                                                                                                                                                                       |
| EM \_ SETGESTURESTATUS<br/>     | Establece el estado del gesto para el control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/>*wParam* Especifica el tipo de gesto, tal como se define en la [**enumeración InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)<br/>*lParam* Especifica **TRUE si** la suscripción al gesto está habilitada o **FALSE** si no está habilitada la escucha del gesto.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/> Comentarios:<br/> Esto solo se debe usar si EM \_ GETSTATUS devuelve IES \_ Idle.<br/>                                                                                                               |
| EM \_ GETRECOGNIZER<br/>        | Obtiene el reconocedor que usa el control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/>*wParam* Este parámetro no se utiliza; debe ser 0.<br/>*lParam* Especifica un puntero a un IInkRecognizer para recibir el objeto \* [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que usa el control [InkEdit.](inkedit-control-reference.md)<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                   |
| EM \_ SETRECOGNIZER<br/>        | Establece el reconocedor que usa el control [InkEdit.](inkedit-control-reference.md) Si se [usa un factoid](factoid-constants.md) para el control InkEdit, se debe volver a aplicar después de enviar este mensaje.<br/> Parámetros:<br/>*wParam* Este parámetro no se utiliza; debe ser 0.<br/>*lParam* Especifica un puntero a un IInkRecognizer para establecer el objeto \* [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que usa el control [InkEdit](inkedit-control-reference.md) para su uso posterior.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/> Comentarios:<br/> Esto solo se debe usar si EM \_ GETSTATUS devuelve IES \_ Idle.<br/> |
| EM \_ GETFACTOID<br/>           | Obtiene el [factoid que se](factoid-constants.md) va a usar para el reconocimiento.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero a un BSTR para recibir la cadena factoid.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETFACTOID<br/>           | Establece [factoid que se](factoid-constants.md) usará para el reconocimiento.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica el BSTR que contiene la cadena factoid.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/> Comentarios:<br/> Esto solo se debe usar si EM \_ GETSTATUS devuelve IES \_ Idle.<br/>                                                                                                                                                                                                                                                                          |
| EM \_ GETSELINK<br/>            | Obtiene la entrada de lápiz dentro de la selección. Se debe reconocer la entrada de lápiz antes de que se acceda a través de este mensaje. Si no se reconoce primero, EM \_ GETSELINK siempre devuelve cero [**objetos InkDisp.**](inkdisp-class.md)<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero a variant para recibir una matriz segura para recibir objetos [**InkDisp**](inkdisp-class.md) dentro de la selección actual.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                     |
| EM \_ SETSELINK<br/>            | Establece la entrada de lápiz dentro de la selección. El envío de este mensaje no tiene ningún efecto si se usa con cualquier sistema operativo instalado que no sea Windows XP Tablet PC Edition.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero a variant con una matriz segura de objetos [**InkDisp**](inkdisp-class.md) para reemplazar la selección actual.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                     |
| EM \_ GETSELINKDISPLAYMODE<br/> | Devuelve la apariencia actual de la entrada de lápiz en el intervalo seleccionado mediante uno de los valores de la [**enumeración InkDisplayMode.**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* y *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve uno de los valores de la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (IDM Text o IDM Ink), que especifica cómo aparece una selección \_ en el \_ control.<br/>                                                                                                                                                                                                                           |
| EM \_ SETSELINKDISPLAYMODE<br/> | Establece la apariencia de la entrada de lápiz en el intervalo seleccionado mediante uno de los valores de la [**enumeración InkDisplayMode.**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica cómo aparece la entrada de lápiz en el intervalo seleccionado, tal como se define en la [**enumeración InkDisplayMode.**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error. El envío de este mensaje no tiene ningún efecto si se usa con cualquier sistema operativo instalado que no sea Windows XP Tablet PC Edition.<br/>                                                                                                   |
| EM \_ GETSTATUS<br/>            | Obtiene el estado del control [InkEdit.](inkedit-control-reference.md)<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* y *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve uno de los valores de la enumeración [**InkEditStatus,**](/windows/desktop/api/inked/ne-inked-inkeditstatus) que especifica si el control está inactivo, recopilando entrada de lápiz o reconociendo la entrada de lápiz.<br/>                                                                                                                                                                                                                                                                                                           |
| EM \_ RECOGNIZE<br/>            | Fuerza el reconocimiento.<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* y *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ GETMOUSEICON<br/>         | Obtiene el icono del mouse.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero HICON \* que se rellena con el [**HICON mouseicon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) actual. Este HICON puede ser un valor HICON o **NULL.**<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETMOUSEICON<br/>         | Establece el icono del mouse.<br/> Parámetros:<br/>*wParam* Especifica un valor BOOLEAN que se establece en **TRUE** si el control [InkEdit](inkedit-control-reference.md) debe poseer el identificador HICON o **FALSE** si el control InkEdit no debe ser el propietario del identificador HICON. Si el control InkEdit posee hicon, se encarga y destruye el HICON de forma adecuada. De lo contrario, el autor de la llamada posee el HICON y es responsable de eliminarlo.<br/>*lParam* Especifica el nuevo valor hicon. Use **NULL** para borrar el valor. El valor predeterminado es **NULL**.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                |
| EM \_ GETMOUSEPOINTER<br/>      | Obtiene el puntero del mouse.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Contiene un puntero InkMousePointer \* que se rellena con el valor actual de [**MousePointer.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) Esto se comporta igual que la **propiedad InkCollector::get \_ MousePointer.**<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                            |
| EM \_ SETMOUSEPOINTER<br/>      | Establece el puntero del mouse.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Contiene el nuevo [**valor de MousePointer,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) que se define en la [**enumeración InkMousePointer.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) Esto se comporta igual que la **propiedad InkCollector::p ut \_ MousePointer.**<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                    |
| EM \_ GETUSEMOUSEFORINPUT<br/>  | Obtiene el estado de si la entrada del mouse se trata como entrada de lápiz.<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* y *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si **es FALSE** o 1 si **es TRUE.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETUSEMOUSEFORINPUT<br/>  | Establece el estado de si la entrada del mouse se trata como entrada de lápiz.<br/> Parámetros:<br/>*wParam* Especifica un valor booleano que determina si se debe tratar la entrada del mouse como entrada de lápiz.<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si se realiza correctamente o es distinto de cero si se produce un error.<br/> Comentarios:<br/> Esto solo se debe usar si EM \_ GETSTATUS devuelve IES \_ Idle.<br/>                                                                                                                                                                                                                                             |



 



| Mensaje de notificación de eventos         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TRAZO \_ IECN<br/>            | Notifica a la ventana primaria del control [InkEdit](inkedit-control-reference.md) que se ha creado [**un IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Se envía en un mensaje WM \_ NOTIFY con los parámetros siguientes.<br/> Parámetros:<br/>*wParam* Especifica el identificador del control que envió el mensaje.<br/>*lParam* Especifica un puntero a la estructura [**\_ IEC STROKEINFO.**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)<br/> Valores devueltos:<br/> El cliente devuelve 0 para aceptar el trazo y 1 para cancelar el trazo.<br/> |
| GESTO \_ DE IECN<br/>           | Notifica a la ventana primaria del control [InkEdit](inkedit-control-reference.md) que se ha reconocido un gesto. Se envía en un mensaje WM \_ NOTIFY con los parámetros siguientes.<br/> Parámetros:<br/>*wParam* Especifica el identificador del control que envió el mensaje.<br/>*lParam* Especifica un puntero a la [**estructura \_ IEC GESTUREINFO.**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)<br/> Valores devueltos:<br/> El cliente devuelve 0 para aceptar el gesto y 1 para cancelar el gesto.<br/>                           |
| IECN \_ RECOGNITIONRESULT<br/> | Notifica a la ventana primaria del control [InkEdit](inkedit-control-reference.md) que se ha producido el reconocimiento. Se envía en un mensaje WM \_ NOTIFY con los parámetros siguientes.<br/> Parámetros:<br/>*wParam* Especifica el identificador del control que envió el mensaje.<br/>*lParam* Especifica un puntero a la [**estructura IEC \_ RECOGNITIONRESULTINFO.**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)<br/> Valores devueltos:<br/> El cliente devuelve 0 si procesa el mensaje.<br/>                                  |



 

## <a name="applies-to"></a>Se aplica a

-   [InkEdit](inkedit-control-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Iec \_ GESTUREINFO (estructura, solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**IEC \_ STROKEINFO (estructura, solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**IEC \_ RECOGNITIONRESULTINFO (estructura, solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**Propiedad MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**InkEditStatus (enumeración)**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**InkInsertMode (Enumeración)**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**InkMode (Enumeración)**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDrawingAttributes (clase)**](inkdrawingattributes-class.md)
</dt> <dt>

[**IInkRecognitionResult (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**IInkRecognizer (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkDisp (clase)**](inkdisp-class.md)
</dt> <dt>

[**IInkGesture (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

