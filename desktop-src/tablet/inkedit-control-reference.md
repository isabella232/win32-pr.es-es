---
description: El control InkEdit permite recopilar entrada de lápiz, reconocer la entrada de lápiz y mostrar la entrada de lápiz como texto.
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: Referencia del control InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbbe2aad6b7d8b536f2ede35fd93bd19840e69fc
ms.sourcegitcommit: f8f06d7ad2ff6599e90b0493b355e0c1811d898f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113369317"
---
# <a name="inkedit-control-reference"></a>Referencia del control InkEdit

El control InkEdit permite recopilar entrada de lápiz, reconocer la entrada de lápiz y mostrar la entrada de lápiz como texto. Este control permite habilitar formularios inteligentes, lo que mejora la precisión de la entrada de texto.

Este control es un superconjunto del control [**RichEdit.**](/windows/desktop/api/richole/nn-richole-iricheditole) Amplía el control **RichEdit** con la capacidad de capturar, reconocer y mostrar la entrada de lápiz.

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

La creación del control InkEdit detrás de un control transparente (como GroupBox con el conjunto de propiedades TRANSPARENT de WS EX) impedirá que \_ \_ InkEdit recopile la entrada de lápiz.

## <a name="members"></a>Miembros



| Enumeración                                            | Descripción                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppearanceConstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | Define valores que especifican si el control aparece plano o 3D.<br/>                                                                                            |
| [**BorderStyleConstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | Define valores que especifican si el control tiene un borde.<br/>                                                                                                   |
| [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | Define valores que establecen el interés en un conjunto de gestos específicos de la aplicación.<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | Define valores que especifican si una selección aparece como entrada de lápiz o texto.<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | Define valores que especifican si el control InkEdit está inactivo, recopilando entrada de lápiz o reconociendo la entrada de lápiz.<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | Define valores que especifican cómo se inserta la entrada de lápiz en el control InkEdit.<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | Define valores que especifican la configuración del modo de recopilación para la entrada de lápiz dibujada: si la colección de lápiz está deshabilitada, si se recopila la entrada de lápiz o si se recopilan los gestos y la entrada de lápiz.<br/> |
| [**InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | Define valores que especifican qué botón del mouse se presionó.<br/>                                                                                                     |
| [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | Define valores que especifican el tipo de puntero del mouse que aparece.<br/>                                                                                             |
| [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | Define valores que especifican qué botón del mouse se presionó.<br/>                                                                                                     |
| [**ScrollBarsConstants**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | Define valores que especifican cómo aparecen en la pantalla las barras de desplazamiento de un control InkEdit.<br/>                                                                     |
| [**SelAlignmentConstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | Define valores que especifican la alineación del párrafo con respecto a los márgenes del control InkEdit.<br/>                                                      |



 



| Mensaje de notificación de eventos                                   | Description                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [TRAZO \_ IECN](inkedit-messages--win32-only-.md)            | Este mensaje se envía a través de un mensaje \_ WM NOTIFY cuando se completa un trazo (solo Win32).<br/>  |
| [GESTO \_ DE IECN](inkedit-messages--win32-only-.md)           | Este mensaje se envía a través de un mensaje WM NOTIFY cuando se completa un gesto \_ (solo Win32).<br/> |
| [IECN \_ RECOGNITIONRESULT](inkedit-messages--win32-only-.md) | Este mensaje se envía a través de un mensaje \_ WM NOTIFY cuando se produce el reconocimiento (solo Win32).<br/>     |



 



| Evento                                                  | Descripción                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cambio**](inkedit-change.md)                       | Se produce cuando cambia el contenido del control o un valor de propiedad.<br/>                                                                                                              |
| [**Haga clic**](inkedit-click.md)                         | Se produce cuando se hace clic en el control.<br/>                                                                                                                                              |
| [**Dblclick**](inkedit-dblclick.md)                   | Se produce cuando se hace doble clic en el control.<br/>                                                                                                                                       |
| [**Gesto**](inkedit-gesture.md)                     | Se produce cuando se reconoce un gesto de aplicación.<br/>                                                                                                                                |
| [**Keydown**](inkedit-keydown.md)                     | Se produce cuando el usuario presiona una tecla mientras el control InkEdit tiene el foco.<br/>                                                                                                          |
| [**Keypress**](inkedit-keypress.md)                   | Se produce cuando se presiona una tecla mientras el control InkEdit tiene el foco.<br/>                                                                                                                |
| [**Keyup**](inkedit-keyup.md)                         | Se produce cuando se libera una clave mientras el control InkEdit tiene el foco.<br/>                                                                                                               |
| [**Mousedown**](inkedit-mousedown.md)                 | Se produce cuando el puntero del mouse está sobre el control InkEdit y se presiona un botón del mouse.<br/>                                                                                         |
| [**Mousemove**](inkedit-mousemove.md)                 | Se produce cuando el puntero del mouse se mueve sobre el control InkEdit.<br/>                                                                                                                 |
| [**MouseUp**](inkedit-mouseup.md)                     | Se produce cuando el puntero del mouse está sobre el control InkEdit y se libera un botón del mouse.<br/>                                                                                        |
| [**RecognitionResult**](inkedit-recognitionresult.md) | Se produce cuando el control InkEdit obtiene los resultados manualmente de una llamada al [**método Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automáticamente después de que se haya desencadenado el tiempo de espera de reconocimiento.<br/> |
| [**SelChange**](inkedit-selchange.md)                 | Se produce cuando cambia la selección de lápiz dentro del control InkEdit.<br/>                                                                                                             |
| [**Golpe**](inkedit-stroke.md)                       | Se produce cuando el usuario dibuja un nuevo [**objeto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en cualquier [**objeto IInkTablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)<br/>                                                 |



 



| Get/Set message                                               | Description                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EM \_ GETINKMODE](inkedit-messages--win32-only-.md)           | Obtiene el modo de entrada de lápiz del control (solo Win32).<br/>                                                                                                                       |
| [EM \_ SETINKMODE](inkedit-messages--win32-only-.md)           | Establece el modo de entrada de lápiz del control (solo Win32).<br/>                                                                                                                       |
| [EM \_ GETINKINSERTMODE](inkedit-messages--win32-only-.md)     | Obtiene el modo de inserción de lápiz del control (solo Win32).<br/>                                                                                                             |
| [EM \_ SETINKINSERTMODE](inkedit-messages--win32-only-.md)     | Establece el modo de inserción de lápiz del control (solo Win32).<br/>                                                                                                             |
| [EM \_ GETDRAWATTR](inkedit-messages--win32-only-.md)          | Obtiene los atributos de dibujo actuales del control (solo Win32).<br/>                                                                                                     |
| [EM \_ SETDRAWATTR](inkedit-messages--win32-only-.md)          | Establece los atributos de dibujo que se usarán para futuras colecciones de lápiz (solo Win32).<br/>                                                                                           |
| [EM \_ GETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | Obtiene el tiempo de espera de reconocimiento para el control (solo Win32).<br/>                                                                                                           |
| [EM \_ SETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | Establece el tiempo de espera de reconocimiento para el control (solo Win32).<br/>                                                                                                           |
| [EM \_ GETGESTURESTATUS](inkedit-messages--win32-only-.md)     | Obtiene el estado del gesto para el control (solo Win32).<br/>                                                                                                                |
| [EM \_ SETGESTURESTATUS](inkedit-messages--win32-only-.md)     | Establece el estado del gesto para el control (solo Win32).<br/>                                                                                                                |
| [EM \_ GETRECOGNIZER](inkedit-messages--win32-only-.md)        | Obtiene el reconocedor que usa el control (solo Win32).<br/>                                                                                                              |
| [EM \_ SETRECOGNIZER](inkedit-messages--win32-only-.md)        | Establece el reconocedor que usa el control (solo Win32).<br/>                                                                                                              |
| [EM \_ GETFACTOID](inkedit-messages--win32-only-.md)           | Obtiene el factoid que se va a usar para el reconocimiento (solo Win32).<br/>                                                                                                                |
| [EM \_ SETFACTIOD](inkedit-messages--win32-only-.md)           | Establece el factoid que se usará para el reconocimiento (solo Win32).<br/>                                                                                                                |
| [EM \_ GETSELINK](inkedit-messages--win32-only-.md)            | Obtiene la entrada de lápiz de la selección (solo Win32).<br/>                                                                                                                          |
| [EM \_ SETSELINK](inkedit-messages--win32-only-.md)            | Establece la entrada de lápiz en la selección (solo Win32).<br/>                                                                                                                          |
| [EM \_ GETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | Devuelve la apariencia actual de la entrada de lápiz en el intervalo seleccionado mediante uno de los valores de la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (solo Win32).<br/> |
| [EM \_ SETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | Establece la apariencia de la entrada de lápiz en el intervalo seleccionado mediante uno de los valores de la enumeración [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (solo Win32).<br/>            |
| [EM \_ GETSTATUS](inkedit-messages--win32-only-.md)            | Obtiene el estado del control (solo Win32).<br/>                                                                                                                         |
| [EM \_ RECOGNIZE](inkedit-messages--win32-only-.md)            | Fuerza el reconocimiento (solo Win32).<br/>                                                                                                                                     |
| [EM \_ GETMOUSEICON](inkedit-messages--win32-only-.md)         | Obtiene el icono del mouse (solo Win32).<br/>                                                                                                                                    |
| [EM \_ SETMOUSEICON](inkedit-messages--win32-only-.md)         | Establece el icono del mouse (solo Win32).<br/>                                                                                                                                    |
| [EM \_ GETMOUSEPOINTER](inkedit-messages--win32-only-.md)      | Obtiene el puntero del mouse (solo Win32).<br/>                                                                                                                                 |
| [EM \_ SETMOUSEPOINTER](inkedit-messages--win32-only-.md)      | Establece solo el puntero del mouse Win32).<br/>                                                                                                                                  |
| [EM \_ GETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | Obtiene el estado de si la entrada del mouse se trata como entrada de lápiz (solo Win32).<br/>                                                                                        |
| [EM \_ SETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | Establece el estado de si la entrada del mouse se trata como entrada de lápiz (solo Win32).<br/>                                                                                        |



 



| Método                                               | Descripción                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | Obtiene el interés del control InkEdit en un conjunto conocido de gestos.<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | Especifica que debe producirse el reconocimiento.<br/>                             |
| [**Actualizar**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | Hace que el control se vuelva a dibujar.<br/>                                        |
| [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | Establece el interés del control InkEdit en un conjunto conocido de gestos.<br/> |



 



| Propiedad                                                 | Description                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspecto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Obtiene o establece un valor que determina si el control InkEdit aparece plano o 3D.<br/>                                                                                      |
| [**Backcolor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Obtiene o establece el color de fondo del control InkEdit.<br/>                                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Obtiene o establece un valor que determina si el control InkEdit tiene un borde.<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Obtiene o establece un valor que determina si las barras de desplazamiento del control InkEdit están deshabilitadas.<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Obtiene o establece los atributos de dibujo para la entrada de lápiz que aún no se han dibujado en el control InkEdit.<br/>                                                                                |
| [**habilitado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Obtiene o establece un valor que determina si el control InkEdit puede responder a eventos generados por el usuario.<br/>                                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Obtiene o establece la [constante Factoid](factoid-constants.md) que usa un [**objeto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para restringir su búsqueda para el resultado del reconocimiento.<br/> |
| [**Fuente**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Obtiene o establece la fuente del texto que muestra el control InkEdit.<br/>                                                                                                       |
| [**Hwnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Obtiene el identificador de ventana al que está enlazado el control [**InkDisp.**](inkdisp-class.md)<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Obtiene o establece un valor que especifica cómo se inserta la entrada de lápiz en el control InkEdit, ya sea como texto o como entrada de lápiz.<br/>                                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Obtiene o establece un valor que especifica si la colección de entrada de lápiz está deshabilitada, si se recopila la entrada de lápiz o si se recopilan los gestos y la entrada de lápiz.<br/>                                               |
| [**Bloqueado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Obtiene o establece un valor que especifica si el control InkEdit es de solo lectura o no.<br/>                                                                                       |
| [**Maxlength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Obtiene o establece un valor que indica si un control InkEdit puede contener un número máximo de caracteres y, si es así, especifica el número máximo de caracteres.<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Obtiene o establece el icono del mouse personalizado actual.<br/>                                                                                                                                |
| [**Mousepointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está sobre una parte determinada del control InkEdit.<br/>                                |
| [**Multilínea**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Obtiene o establece un valor que indica si se trata de un control InkEdit multilínea.<br/>                                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Obtiene o establece el tiempo, en milisegundos, entre el último objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado y el principio del reconocimiento de texto.<br/>        |
| [**Reconocedor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Obtiene o establece el [**objeto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que se va a usar para el reconocimiento.<br/>                                                                                   |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Obtiene o establece el tipo de barras de desplazamiento que aparecen en el control InkEdit.<br/>                                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Obtiene o establece la alineación que se va a aplicar al punto de inserción o selección actual (solo en tiempo de ejecución).<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control InkEdit está en negrita (solo en tiempo de ejecución).<br/>                                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Obtiene o establece si el texto del control InkEdit aparece en la línea base, como un superíndice o como un subíndice (solo en tiempo de ejecución).<br/>                                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Obtiene o establece el color del texto del punto de inserción o selección de texto actual (solo en tiempo de ejecución).<br/>                                                                              |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Obtiene o establece el nombre de fuente del texto seleccionado dentro del control InkEdit (solo en tiempo de ejecución).<br/>                                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Obtiene o establece el tamaño de fuente del texto seleccionado en el control InkEdit (solo en tiempo de ejecución).<br/>                                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Obtiene o establece la matriz de objetos [**InkDisp**](inkdisp-class.md) incrustados (si se muestran como entrada de lápiz) que contiene la selección actual.<br/>                                     |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Obtiene o establece un valor que permite alternar la apariencia de la selección entre la entrada de lápiz y el texto.<br/>                                                                            |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control InkEdit está en cursiva (solo en tiempo de ejecución).<br/>                                |
| [**Sellength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Obtiene o establece el número de caracteres seleccionados en el control InkEdit (solo en tiempo de ejecución).<br/>                                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Obtiene o establece el texto con formato Formato de texto enriquecido (RTF) seleccionado actualmente en el control InkEdit (solo en tiempo de ejecución).<br/>                                                          |
| [**Selstart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Obtiene o establece el punto inicial del texto seleccionado en el cuadro de texto (solo en tiempo de ejecución).<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Obtiene o establece el texto seleccionado en el control InkEdit (solo en tiempo de ejecución).<br/>                                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control InkEdit está subrayado (solo en tiempo de ejecución).<br/>                            |
| [**Estado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Obtiene un valor que especifica si el control InkEdit está inactivo, recopilando entrada de lápiz o reconociendo la entrada de lápiz (solo en tiempo de ejecución).<br/>                                                       |
| [**Texto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Obtiene o establece el texto actual del cuadro de texto.<br/>                                                                                                                             |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Obtiene o establece el texto del control InkEdit, incluidos todos los códigos RTF.<br/>                                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Obtiene o establece un valor que indica si el mouse se puede usar como un dispositivo de entrada.<br/>                                                                                      |

| Estructura                                                                    | Description                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IEC \_ STROKEINFO**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | Contiene información sobre un [**evento stroke**](inkedit-stroke.md) (solo Win32).<br/> |
| [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | Contiene información sobre un gesto específico (solo Win32).<br/>                       |
| [**IEC \_ RECOGNITIONRESULTINFO**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | Contiene información sobre un resultado de reconocimiento (solo Win32).<br/>                     |

## <a name="com-implementation"></a>Implementación com

Este objeto implementa la [interfaz COM IInkEdit.](/windows/win32/api/inked/nn-inked-iinkedit)

## <a name="related-topics"></a>Temas relacionados

- [**InkOverlay (clase )**](inkoverlay-class.md) 
- [Referencia del control InkPicture](inkpicture-control-reference.md)
- [**InkRecognizerContext (clase)**](inkrecognizercontext-class.md)
