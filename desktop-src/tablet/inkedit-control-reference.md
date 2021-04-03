---
description: El control InkEdit permite recopilar la tinta, reconocer la tinta y mostrar la entrada de lápiz como texto.
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: Referencia de control InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53edfdc6a72a7792c60a6c7c7bf0e38ffc5e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083317"
---
# <a name="inkedit-control-reference"></a>Referencia de control InkEdit

El control InkEdit permite recopilar la tinta, reconocer la tinta y mostrar la entrada de lápiz como texto. Este control permite habilitar formularios inteligentes, lo que mejora la precisión de la entrada de texto.

Este control es un superconjunto del control [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . Extiende el control **RichEdit** con la capacidad de capturar, reconocer y mostrar la entrada de lápiz.

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

La creación del control InkEdit detrás de un control transparente (como GroupBox con el \_ conjunto de \_ propiedades transparentes WS ex) impedirá que InkEdit recopile la tinta.

## <a name="members"></a>Miembros



| Enumeración                                            | Descripción                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppearanceConstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | Define valores que especifican si el control aparece plano o 3D.<br/>                                                                                            |
| [**BorderStyleConstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | Define valores que especifican si el control tiene un borde.<br/>                                                                                                   |
| [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | Define valores que establecen el interés en un conjunto de gestos específicos de la aplicación.<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | Define valores que especifican si una selección aparece como entrada de lápiz o texto.<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | Define valores que especifican si el control InkEdit está inactivo, recopilando entradas manuscritas o reconociendo entradas de lápiz.<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | Define valores que especifican cómo se inserta la entrada de lápiz en el control InkEdit.<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | Define valores que especifican la configuración del modo de recopilación para la tinta dibujada, independientemente de si la colección de tintas está deshabilitada, se recopila la tinta o se recopilan los movimientos y las entradas de lápiz.<br/> |
| [**InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | Define valores que especifican qué botón del mouse se presionó.<br/>                                                                                                     |
| [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | Define valores que especifican el tipo de puntero del mouse que aparece.<br/>                                                                                             |
| [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | Define valores que especifican qué botón del mouse se presionó.<br/>                                                                                                     |
| [**ScrollBarsConstants**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | Define valores que especifican el modo en que las barras de desplazamiento de un control InkEdit aparecen en la pantalla.<br/>                                                                     |
| [**SelAlignmentConstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | Define valores que especifican la alineación del párrafo con respecto a los márgenes del control InkEdit.<br/>                                                      |



 



| Mensaje de notificación de eventos                                   | Descripción                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [\_trazo IECN](inkedit-messages--win32-only-.md)            | Este mensaje se envía a través de un mensaje de notificación de WM \_ cuando se completa un trazo (solo Win32).<br/>  |
| [\_gesto IECN](inkedit-messages--win32-only-.md)           | Este mensaje se envía a través de un mensaje de notificación de WM \_ cuando se completa un gesto (solo Win32).<br/> |
| [IECN \_ RECOGNITIONRESULT](inkedit-messages--win32-only-.md) | Este mensaje se envía a través de un mensaje de notificación de WM \_ cuando se produce el reconocimiento (solo Win32).<br/>     |



 



| Evento                                                  | Descripción                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cambio**](inkedit-change.md)                       | Se produce cuando cambia el contenido del control o de un valor de propiedad.<br/>                                                                                                              |
| [**Hizo**](inkedit-click.md)                         | Se produce cuando se hace clic en el control.<br/>                                                                                                                                              |
| [**DblClick**](inkedit-dblclick.md)                   | Se produce cuando se hace doble clic en el control.<br/>                                                                                                                                       |
| [**Gesto**](inkedit-gesture.md)                     | Se produce cuando se reconoce un gesto de aplicación.<br/>                                                                                                                                |
| [**KeyUp**](inkedit-keydown.md)                     | Se produce cuando el usuario presiona una tecla mientras el control InkEdit tiene el foco.<br/>                                                                                                          |
| [**KeyPress**](inkedit-keypress.md)                   | Se produce cuando se presiona una tecla mientras el control InkEdit tiene el foco.<br/>                                                                                                                |
| [**KeyUp**](inkedit-keyup.md)                         | Se produce cuando se suelta una tecla mientras el control InkEdit tiene el foco.<br/>                                                                                                               |
| [**Eventos**](inkedit-mousedown.md)                 | Se produce cuando el puntero del mouse se encuentra sobre el control InkEdit y se presiona un botón del mouse.<br/>                                                                                         |
| [**MouseMove**](inkedit-mousemove.md)                 | Se produce cuando el puntero del mouse se mueve sobre el control InkEdit.<br/>                                                                                                                 |
| [**MouseUp**](inkedit-mouseup.md)                     | Se produce cuando el puntero del mouse se encuentra sobre el control InkEdit y se suelta un botón del mouse.<br/>                                                                                        |
| [**RecognitionResult**](inkedit-recognitionresult.md) | Se produce cuando el control InkEdit obtiene los resultados manualmente desde una llamada al método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automáticamente después de que se haya desactivado el tiempo de espera de reconocimiento.<br/> |
| [**SelChange**](inkedit-selchange.md)                 | Se produce cuando cambia la selección de tinta dentro del control InkEdit.<br/>                                                                                                             |
| [**Stroke**](inkedit-stroke.md)                       | Se produce cuando el usuario dibuja un nuevo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en cualquier objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .<br/>                                                 |



 



| Obtener/establecer mensaje                                               | Descripción                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_GETINKMODE em](inkedit-messages--win32-only-.md)           | Obtiene el modo de entrada de lápiz del control (solo Win32).<br/>                                                                                                                       |
| [\_SETINKMODE em](inkedit-messages--win32-only-.md)           | Establece el modo de entrada de lápiz del control (solo Win32).<br/>                                                                                                                       |
| [\_GETINKINSERTMODE em](inkedit-messages--win32-only-.md)     | Obtiene el modo de inserción de entrada de lápiz del control (solo Win32).<br/>                                                                                                             |
| [\_SETINKINSERTMODE em](inkedit-messages--win32-only-.md)     | Establece el modo de inserción de entrada de lápiz del control (solo Win32).<br/>                                                                                                             |
| [\_GETDRAWATTR em](inkedit-messages--win32-only-.md)          | Obtiene los atributos de dibujo actuales del control (solo Win32).<br/>                                                                                                     |
| [\_SETDRAWATTR em](inkedit-messages--win32-only-.md)          | Establece los atributos de dibujo que se van a usar para la colección de entradas de lápiz futura (solo Win32).<br/>                                                                                           |
| [\_GETRECOTIMEOUT em](inkedit-messages--win32-only-.md)       | Obtiene el tiempo de espera de reconocimiento para el control (solo Win32).<br/>                                                                                                           |
| [\_SETRECOTIMEOUT em](inkedit-messages--win32-only-.md)       | Establece el tiempo de espera de reconocimiento para el control (solo Win32).<br/>                                                                                                           |
| [\_GETGESTURESTATUS em](inkedit-messages--win32-only-.md)     | Obtiene el estado del gesto del control (solo Win32).<br/>                                                                                                                |
| [\_SETGESTURESTATUS em](inkedit-messages--win32-only-.md)     | Establece el estado del gesto para el control (solo Win32).<br/>                                                                                                                |
| [\_GETRECOGNIZER em](inkedit-messages--win32-only-.md)        | Obtiene el reconocedor que usa el control (solo Win32).<br/>                                                                                                              |
| [\_SETRECOGNIZER em](inkedit-messages--win32-only-.md)        | Establece el reconocedor que usa el control (solo Win32).<br/>                                                                                                              |
| [\_GETFACTOID em](inkedit-messages--win32-only-.md)           | Obtiene el Factoid que se va a usar para el reconocimiento (solo Win32).<br/>                                                                                                                |
| [\_SETFACTIOD em](inkedit-messages--win32-only-.md)           | Establece el Factoid que se va a usar para el reconocimiento (solo Win32).<br/>                                                                                                                |
| [\_GETSELINK em](inkedit-messages--win32-only-.md)            | Obtiene la entrada manuscrita en la selección (solo Win32).<br/>                                                                                                                          |
| [\_SETSELINK em](inkedit-messages--win32-only-.md)            | Establece la entrada de lápiz en la selección (solo Win32).<br/>                                                                                                                          |
| [\_GETSELINKDISPLAYMODE em](inkedit-messages--win32-only-.md) | Devuelve la apariencia actual de la entrada de lápiz en el intervalo seleccionado utilizando uno de los valores de la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (solo Win32).<br/> |
| [\_SETSELINKDISPLAYMODE em](inkedit-messages--win32-only-.md) | Establece la apariencia de la entrada de lápiz en el intervalo seleccionado utilizando uno de los valores de la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (solo Win32).<br/>            |
| [\_GETSTATUS em](inkedit-messages--win32-only-.md)            | Obtiene el estado del control (solo Win32).<br/>                                                                                                                         |
| [\_reconocer em](inkedit-messages--win32-only-.md)            | Fuerza el reconocimiento (solo Win32).<br/>                                                                                                                                     |
| [\_GETMOUSEICON em](inkedit-messages--win32-only-.md)         | Obtiene el icono del mouse (solo Win32).<br/>                                                                                                                                    |
| [\_SETMOUSEICON em](inkedit-messages--win32-only-.md)         | Establece el icono del mouse (solo Win32).<br/>                                                                                                                                    |
| [\_GETMOUSEPOINTER em](inkedit-messages--win32-only-.md)      | Obtiene el puntero del mouse (solo Win32).<br/>                                                                                                                                 |
| [\_SETMOUSEPOINTER em](inkedit-messages--win32-only-.md)      | Establece el puntero del mouse solo en Win32).<br/>                                                                                                                                  |
| [\_GETUSEMOUSEFORINPUT em](inkedit-messages--win32-only-.md)  | Obtiene el estado que indica si la entrada del mouse se trata como entrada manuscrita (solo Win32).<br/>                                                                                        |
| [\_SETUSEMOUSEFORINPUT em](inkedit-messages--win32-only-.md)  | Establece el estado de si la entrada del mouse se trata como entrada manuscrita (solo Win32).<br/>                                                                                        |



 



| Método                                               | Descripción                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | Obtiene el interés del control InkEdit en un conjunto conocido de gestos.<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | Especifica que debe producirse el reconocimiento.<br/>                             |
| [**Actualizaciones**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | Hace que se vuelva a dibujar el control.<br/>                                        |
| [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | Establece el interés del control InkEdit en un conjunto conocido de gestos.<br/> |



 



| Propiedad                                                 | Descripción                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspecto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Obtiene o establece un valor que determina si el control InkEdit aparece plano o 3D.<br/>                                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Obtiene o establece el color de fondo del control InkEdit.<br/>                                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Obtiene o establece un valor que determina si el control InkEdit tiene un borde.<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Obtiene o establece un valor que determina si las barras de desplazamiento del control InkEdit están deshabilitadas.<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Obtiene o establece los atributos de dibujo de la tinta que todavía se va a dibujar en el control InkEdit.<br/>                                                                                |
| [**habilitado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Obtiene o establece un valor que determina si el control InkEdit puede responder a los eventos generados por el usuario.<br/>                                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Obtiene o establece la constante [Factoid](factoid-constants.md) que usa un objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para restringir su búsqueda para el resultado del reconocimiento.<br/> |
| [**Tipo**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Obtiene o establece la fuente del texto que muestra el control InkEdit.<br/>                                                                                                       |
| [**Identificador**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Obtiene el identificador de ventana al que está enlazado el control [**InkDisp**](inkdisp-class.md) .<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Obtiene o establece un valor que especifica cómo se inserta la entrada de lápiz en el control InkEdit, ya sea como texto o como entrada de lápiz.<br/>                                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Obtiene o establece un valor que especifica si la colección de tintas está deshabilitada, se recopila la tinta o se recopilan los movimientos y las entradas de lápiz.<br/>                                               |
| [**Bloqueado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Obtiene o establece un valor que especifica si el control InkEdit es de solo lectura o no.<br/>                                                                                       |
| [**Longitud**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Obtiene o establece un valor que indica si un control InkEdit puede contener un número máximo de caracteres y, si es así, especifica el número máximo de caracteres.<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Obtiene o establece el icono actual del mouse.<br/>                                                                                                                                |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está sobre una parte determinada del control InkEdit.<br/>                                |
| [**Ocupa**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Obtiene o establece un valor que indica si se trata de un control InkEdit multilínea.<br/>                                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Obtiene o establece el período de tiempo, en milisegundos, entre el último objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado y el principio del reconocimiento de texto.<br/>        |
| [**Reconocedor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Obtiene o establece el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que se va a usar para el reconocimiento.<br/>                                                                                   |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Obtiene o establece el tipo de barras de desplazamiento que aparecen en el control InkEdit.<br/>                                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Obtiene o establece la alineación que se va a aplicar a la selección o al punto de inserción actual (solo en tiempo de ejecución).<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control InkEdit está en negrita (solo en tiempo de ejecución).<br/>                                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Obtiene o establece si el texto del control InkEdit aparece en la línea base, como superíndice o como subíndice (solo en tiempo de ejecución).<br/>                                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Obtiene o establece el color del texto de la selección de texto o punto de inserción actual (solo en tiempo de ejecución).<br/>                                                                              |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Obtiene o establece el nombre de fuente del texto seleccionado en el control InkEdit (solo en tiempo de ejecución).<br/>                                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Obtiene o establece el tamaño de fuente del texto seleccionado en el control InkEdit (solo en tiempo de ejecución).<br/>                                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Obtiene o establece la matriz de objetos [**InkDisp**](inkdisp-class.md) insertados (si se muestra como entrada de lápiz) que contiene la selección actual.<br/>                                     |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Obtiene o establece un valor que permite alternar la apariencia de la selección entre la tinta y el texto.<br/>                                                                            |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control InkEdit está en cursiva (solo en tiempo de ejecución).<br/>                                |
| [**LongitudDeSel**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Obtiene o establece el número de caracteres seleccionados en el control InkEdit (solo en tiempo de ejecución).<br/>                                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Obtiene o establece el texto con formato RTF (formato de texto enriquecido) seleccionado actualmente en el control InkEdit (solo en tiempo de ejecución).<br/>                                                          |
| [**ComienzoDeSel**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Obtiene o establece el punto inicial del texto que se selecciona en el cuadro de texto (solo en tiempo de ejecución).<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Obtiene o establece el texto seleccionado en el control InkEdit (solo en tiempo de ejecución).<br/>                                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control InkEdit está subrayado (solo en tiempo de ejecución).<br/>                            |
| [**Status**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Obtiene un valor que especifica si el control InkEdit está inactivo, recopilando entradas de lápiz o reconocimiento de tinta (solo en tiempo de ejecución).<br/>                                                       |
| [**Texto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Obtiene o establece el texto actual del cuadro de texto.<br/>                                                                                                                             |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Obtiene o establece el texto del control InkEdit, incluidos todos los códigos RTF.<br/>                                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Obtiene o establece un valor que indica si se puede usar el mouse como dispositivo de entrada.<br/>                                                                                      |



 



| Estructura                                                                    | Descripción                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_STROKEINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | Contiene información sobre un evento de [**trazo**](inkedit-stroke.md) (solo Win32).<br/> |
| [**\_GESTUREINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | Contiene información sobre un gesto específico (solo Win32).<br/>                       |
| [**\_RECOGNITIONRESULTINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | Contiene información sobre un resultado de reconocimiento (solo Win32).<br/>                     |



 

## <a name="com-implementation"></a>Implementación COM

Este objeto implementa la interfaz com **IInkEdit** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[Referencia del control InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Clase InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

