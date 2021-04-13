---
description: El control InkEdit es una superclase del control RichEdit.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: Mensajes InkEdit (solo Win32)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b403e950ca67523620baab6f90a8fef9a47bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360823"
---
# <a name="inkedit-messages-win32-only"></a>Mensajes InkEdit (solo Win32)

El control [InkEdit](inkedit-control-reference.md) es una superclase del control [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . Todos los mensajes **RichEdit** se pasan, directamente en la mayoría de los casos, y tienen exactamente el mismo efecto que en **RichEdit**. Esto también se aplica a los mensajes de notificación de eventos.

Para enviar estos mensajes, llame a la función SendMessage con los parámetros siguientes:



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>LRESULT SendMessage(
  HWND hWnd,      // handle to destination window
  UINT Msg,       // message
  WPARAM wParam,  // first message parameter
  LPARAM lParam   // second message parameter
);</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="message"></a>Message

La ventana primaria del control [InkEdit](inkedit-control-reference.md) recibe mensajes de notificación de eventos a través del mensaje de notificación de WM \_ :


```C++
LRESULT CALLBACK WindowProc(
    HWND hWnd,                // handle to window
    UINT uMsg,                // WM_NOTIFY
    WPARAM wParam,        // InkEdit control identifier
    LPARAM lParam            // see documentation for notification messages
);
```





| Obtener/establecer mensaje                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_GETINKMODE em<br/>           | Obtiene el modo de entrada de lápiz del control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* e *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve uno de los valores que se definen en la enumeración [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) , que especifica si la colección de tintas está deshabilitada, si se recopila la tinta o si se recopilan entradas de lápiz y movimientos.<br/>                                                                                                                                                                                                                                                         |
| \_SETINKMODE em<br/>           | Establece el modo de entrada de lápiz del control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/>*wParam* Especifica uno de los valores de la enumeración [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) , que especifica si la colección de tintas está deshabilitada, si se recopila la tinta o si se recopilan entradas de lápiz y movimientos.<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/> Comentarios:<br/> Solo se debe usar si el GETSTATUS EM \_ devuelve s \_ idle.<br/>                                                                                                               |
| \_GETINKINSERTMODE em<br/>     | Obtiene el modo de inserción de entrada de lápiz del control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* e *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve uno de los valores de la enumeración [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) , que especifica si la entrada de lápiz se inserta en el control como texto o como entrada de lápiz.<br/>                                                                                                                                                                                                                                                                                                    |
| \_SETINKINSERTMODE em<br/>     | Establece el modo de inserción de entrada de lápiz del control [InkEdit](inkedit-control-reference.md) . El envío de este mensaje no tiene ningún efecto si se usa con cualquier sistema operativo instalado que no sea Microsoft Windows XP Tablet PC Edition.<br/> Parámetros:<br/>*wParam* Especifica uno de los valores de la enumeración [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) , que especifica si la entrada de lápiz se inserta en el control como texto o como entrada de lápiz.<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                       |
| \_GETDRAWATTR em<br/>          | Obtiene los atributos de dibujo actuales del control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero (IInkDrawingAttributes \* \* pDrawAttr) para recibir el objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) actual.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                |
| \_SETDRAWATTR em<br/>          | Establece los atributos de dibujo que se van a usar para la recopilación futura de entradas de lápiz.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero (IInkDrawingAttributes \* pDrawAttr) a un objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) .<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                  |
| \_GETRECOTIMEOUT em<br/>       | Obtiene el tiempo de espera de reconocimiento, en milisegundos, para el control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* e *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve el tiempo de espera de reconocimiento, en milisegundos.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_SETRECOTIMEOUT em<br/>       | Establece el tiempo de espera de reconocimiento, en milisegundos, para el control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/>*wParam* Especifica el tiempo de espera de reconocimiento, en milisegundos.<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                                                    |
| \_GETGESTURESTATUS em<br/>     | Obtiene el estado del gesto para el control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/>*wParam* Especifica el tipo de gesto, tal y como se define en la enumeración [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve **true** si el control [InkEdit](inkedit-control-reference.md) se suscribe al gesto o **false** si el control InkEdit no se suscribe al gesto.<br/>                                                                                                                                                                       |
| \_SETGESTURESTATUS em<br/>     | Establece el estado del gesto para el control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/>*wParam* Especifica el tipo de gesto, tal y como se define en la enumeración [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .<br/>*lParam* Especifica **true** si la suscripción al gesto está habilitada o **false** si la escucha del gesto no está habilitada.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/> Comentarios:<br/> Solo se debe usar si el GETSTATUS EM \_ devuelve s \_ idle.<br/>                                                                                                               |
| \_GETRECOGNIZER em<br/>        | Obtiene el reconocedor que el control [InkEdit](inkedit-control-reference.md) usa.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero a un IInkRecognizer \* para recibir el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que usa el control [InkEdit](inkedit-control-reference.md) .<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                   |
| \_SETRECOGNIZER em<br/>        | Establece el reconocedor que el control [InkEdit](inkedit-control-reference.md) usa. Si se usa un [Factoid](factoid-constants.md) para el control InkEdit, se debe volver a aplicar después de enviar este mensaje.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero a un IInkRecognizer \* para establecer el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que el control [InkEdit](inkedit-control-reference.md) utiliza para su uso posterior.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/> Comentarios:<br/> Solo se debe usar si el GETSTATUS EM \_ devuelve s \_ idle.<br/> |
| \_GETFACTOID em<br/>           | Obtiene el [Factoid](factoid-constants.md) que se va a usar para el reconocimiento.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero a un BSTR para recibir la cadena Factoid.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| \_SETFACTOID em<br/>           | Establece el [Factoid](factoid-constants.md) que se va a usar para el reconocimiento.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica el BSTR que contiene la cadena Factoid.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/> Comentarios:<br/> Solo se debe usar si el GETSTATUS EM \_ devuelve s \_ idle.<br/>                                                                                                                                                                                                                                                                          |
| \_GETSELINK em<br/>            | Obtiene la entrada de lápiz dentro de la selección. Se debe reconocer la tinta antes de tener acceso a ella a través de este mensaje. Si no se reconoce primero, EM \_ GETSELINK siempre devuelve cero objetos [**InkDisp**](inkdisp-class.md) .<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero a una variante para recibir una matriz segura para recibir objetos [**InkDisp**](inkdisp-class.md) dentro de la selección actual.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                     |
| \_SETSELINK em<br/>            | Establece la entrada de lápiz dentro de la selección. El envío de este mensaje no tiene ningún efecto si se usa con cualquier sistema operativo instalado que no sea Windows XP Tablet PC Edition.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un puntero a una variante con una matriz segura de objetos [**InkDisp**](inkdisp-class.md) para reemplazar la selección actual.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                     |
| \_GETSELINKDISPLAYMODE em<br/> | Devuelve la apariencia actual de la entrada de lápiz en el intervalo seleccionado utilizando uno de los valores de la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* e *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve uno de los valores de la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) ( \_ texto IDM o \_ tinta IDM), que especifica cómo aparece una selección en el control.<br/>                                                                                                                                                                                                                           |
| \_SETSELINKDISPLAYMODE em<br/> | Establece la apariencia de la entrada de lápiz en el intervalo seleccionado utilizando uno de los valores de la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica cómo aparece la tinta en el intervalo seleccionado, tal como se define en la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error. El envío de este mensaje no tiene ningún efecto si se usa con cualquier sistema operativo instalado que no sea Windows XP Tablet PC Edition.<br/>                                                                                                   |
| \_GETSTATUS em<br/>            | Obtiene el estado del control [InkEdit](inkedit-control-reference.md) .<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* e *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve uno de los valores de la enumeración [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus) , que especifica si el control está inactivo, recopilando entradas de lápiz o reconociendo la tinta.<br/>                                                                                                                                                                                                                                                                                                           |
| \_reconocer em<br/>            | Fuerza el reconocimiento.<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* e *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_GETMOUSEICON em<br/>         | Obtiene el icono del mouse.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Especifica un \* puntero HICON que se rellena con el HICON de [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) actual. Este HICON puede ser un valor de HICON o **null** .<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                                                                    |
| \_SETMOUSEICON em<br/>         | Establece el icono del mouse.<br/> Parámetros:<br/>*wParam* Especifica un valor BOOLEANO que se establece en **true** si el control [InkEdit](inkedit-control-reference.md) debe poseer el identificador HICON o **false** si el control INKEDIT no debe poseer el identificador HICON. Si el control InkEdit posee el HICON, se encarga de y destruye el HICON de forma adecuada. De lo contrario, el autor de la llamada posee el HICON y es responsable de eliminarlo.<br/>*lParam* Especifica el nuevo valor de HICON. Use **null** para borrar el valor. El valor predeterminado es **NULL**.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                |
| \_GETMOUSEPOINTER em<br/>      | Obtiene el puntero del mouse.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Contiene un \* puntero InkMousePointer que se rellena con el valor actual de [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) . Esto se comporta igual que la propiedad **InkCollector:: get \_ MousePointer** .<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                                            |
| \_SETMOUSEPOINTER em<br/>      | Establece el puntero del mouse.<br/> Parámetros:<br/>*wParam* Este parámetro no se usa; debe ser 0.<br/>*lParam* Contiene el nuevo valor de [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) , que se define en la enumeración [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) . Esto se comporta igual que la propiedad **InkCollector::p UT \_ MousePointer** .<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/>                                                                                                                                                                                                                                    |
| \_GETUSEMOUSEFORINPUT em<br/>  | Obtiene el estado que indica si la entrada del mouse se trata como entrada manuscrita.<br/> Parámetros:<br/> Este mensaje no tiene parámetros; *wParam* e *lParam* deben ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si **es false** o 1 si **es true**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \_SETUSEMOUSEFORINPUT em<br/>  | Establece el estado de si la entrada del mouse se trata como entrada manuscrita.<br/> Parámetros:<br/>*wParam* Especifica un valor booleano que determina si se debe tratar la entrada del mouse como entrada manuscrita.<br/>*lParam* Este parámetro no se usa; debe ser 0.<br/> Valores devueltos:<br/> Este mensaje devuelve 0 si es correcto o es distinto de cero si se produce un error.<br/> Comentarios:<br/> Solo se debe usar si el GETSTATUS EM \_ devuelve s \_ idle.<br/>                                                                                                                                                                                                                                             |



 



| Mensaje de notificación de eventos         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_trazo IECN<br/>            | Notifica a la ventana primaria del control [InkEdit](inkedit-control-reference.md) que se ha creado un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . Se envía en un mensaje de \_ notificación de WM con los parámetros siguientes.<br/> Parámetros:<br/>*wParam* Especifica el identificador del control que envió el mensaje.<br/>*lParam* Especifica un puntero a la estructura [**IEC \_ STROKEINFO**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo) .<br/> Valores devueltos:<br/> El cliente devuelve 0 para aceptar el trazo y 1 para cancelar el trazo.<br/> |
| \_gesto IECN<br/>           | Notifica a la ventana primaria del control [InkEdit](inkedit-control-reference.md) que se ha reconocido un gesto. Se envía en un mensaje de \_ notificación de WM con los parámetros siguientes.<br/> Parámetros:<br/>*wParam* Especifica el identificador del control que envió el mensaje.<br/>*lParam* Especifica un puntero a la estructura [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo) .<br/> Valores devueltos:<br/> El cliente devuelve 0 para aceptar el gesto y 1 para cancelar el gesto.<br/>                           |
| IECN \_ RECOGNITIONRESULT<br/> | Notifica a la ventana primaria del control [InkEdit](inkedit-control-reference.md) que se ha producido el reconocimiento. Se envía en un mensaje de \_ notificación de WM con los parámetros siguientes.<br/> Parámetros:<br/>*wParam* Especifica el identificador del control que envió el mensaje.<br/>*lParam* Especifica un puntero a la estructura [**IEC \_ RECOGNITIONRESULTINFO**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) .<br/> Valores devueltos:<br/> El cliente devuelve 0 si procesa el mensaje.<br/>                                  |



 

## <a name="applies-to"></a>Se aplica a

-   [InkEdit](inkedit-control-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_Estructura IEC GESTUREINFO (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**\_Estructura IEC STROKEINFO (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**\_Estructura IEC RECOGNITIONRESULTINFO (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**MousePointer (propiedad)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**Enumeración InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**Enumeración InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**Enumeración InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**Interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Clase InkDrawingAttributes**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interfaz IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**Interfaz IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Clase InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Interfaz IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

