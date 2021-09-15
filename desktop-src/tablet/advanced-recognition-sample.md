---
description: El ejemplo de reconocimiento avanzado muestra las características avanzadas de la interfaz de programación de aplicaciones (API) de Microsoft Tablet PC Automation que se usa para el reconocimiento de escritura a mano.
ms.assetid: 4c9b9f31-c317-43fd-8404-35295b41d093
title: Ejemplo de reconocimiento avanzado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e23a078ded9c6967f8e45780f8cb3a739b246f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247880"
---
# <a name="advanced-recognition-sample"></a>Ejemplo de reconocimiento avanzado

El ejemplo de reconocimiento avanzado muestra las características avanzadas de la interfaz de programación de aplicaciones (API) de Microsoft Tablet PC Automation que se usa para el reconocimiento de escritura a mano.

Contiene las características siguientes:

-   Enumeración del reconocedor instalado
-   Creación de un contexto de reconocedor con un lenguaje específico
-   Uso del objeto de reconocedor
-   Establecimiento de listas de palabras y factoid de reconocimiento
-   Uso de guías para mejorar la calidad del reconocimiento
-   Reconocimiento dinámico en segundo plano
-   Reconocimiento de gestos

Las interfaces usadas son: [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer), **IInkRecoContext**, [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult), **IInkRecognitionGuide**, **IInkWordList**, [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture), **IInkCollector**, **IInkDisp**, **IInkRenderer**, **IInkDrawingAttributes,** **IInkStrokes** e **IInkStroke**.

## <a name="ink-and-project-headers"></a>Encabezados ink y Project

En primer lugar, incluya los encabezados de las interfaces de Automatización de Tablet PC. Estos se instalan con el SDK de la plataforma de Tablet PC. El archivo TpcError.h contiene las definiciones de código de error de la API de Tablet PC.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
#include <TpcError.h>
```



El archivo EventSinks.h define las **interfaces IInkEventsImpl** **e IInkRecognitionEventsImpl** y configura los eventos [**RecognitionWithAlternates,**](inkrecognizercontext-recognitionwithalternates.md) [**Stroke**](inkcollector-stroke.md)y [**Gesture.**](inkcollector-gesture.md)


```C++
#include "EventSinks.h"
```



El archivo ChildWnds.h contiene las definiciones de las clases **CInkInputWnd** y **CRecoOutputWnd**, que se derivan de CWindowImpl del ATL y se usan para crear las ventanas secundarias del ejemplo.


```C++
#include "ChildWnds.h"
```



El archivo AdvReco.h declara la clase **CAdvRecoApp,** que es la clase de ventana de aplicación para este ejemplo.


```C++
#include "AdvReco.h"
```



## <a name="initializing-the-application-window"></a>Inicialización de la ventana de la aplicación

El método de la ventana configura el objeto `Run` **CAdvRecoApp,** carga el menú y el icono de la ventana, crea un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) para el reconocedor predeterminado e inicia el bucle de mensajes de la ventana.

El método **OnCreate** de la ventana controla el **evento WM \_ CREATE** y crea las ventanas secundarias. Un [**objeto InkCollector**](inkcollector-class.md) se conecta al origen de eventos del recopilador de entrada de lápiz y habilita la entrada de lápiz en la ventana de entrada. A continuación, crea un [**objeto InkRecognizerGuide**](inkrecognizerguide-class.md) y usa la propiedad [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer) del recopilador de lápiz para convertir los rectángulos del cuadro de la guía de reconocimiento en espacio de entrada de lápiz. Por último, **el método OnCreate** crea un [**objeto InkWordList.**](inkwordlist-class.md)

## <a name="handling-ink-collector-events"></a>Control de eventos del recopilador de entrada de lápiz

El método **OnStroke** de la ventana controla el evento Stroke del recopilador de entrada [**manuscrita.**](inkcollector-stroke.md) El nuevo [**objeto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) se agrega a [inkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de la propiedad Ink del recopilador [**de**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) lápiz.

El método **OnGesture** de la ventana controla el evento Gesture del recopilador de entrada [**manuscrita.**](inkcollector-gesture.md) El **método OnGesture** identifica el gesto, usando primero el gesto de mayor confianza y comprueba si la ventana admite este gesto en particular. Si se admite el gesto, se invalida el cuadro de límite del gesto, ya que se quita de la colección de trazos. Si no se admite el gesto, se cancela el **evento Gesto,** lo que hace que el recopilador de lápiz genera un [**evento Stroke.**](inkcollector-stroke.md) Por último, se actualiza la ventana de resultados.

## <a name="handling-recognizer-context-events"></a>Control de eventos de contexto de reconocedor

El método **OnRecognitionWithAlternates** de la ventana controla el evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) del contexto del reconocedor. El **método OnRecognitionWithAlternates** muestra los resultados del reconocimiento en la ventana de resultados.

## <a name="handling-menu-commands"></a>Controlar comandos de menú

El método **OnRecognizer de** la ventana controla los comandos del menú Reconocedor. Si se **ha** seleccionado el comando Default, se usa el método [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) de [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) para recuperar el reconocedor predeterminado; De lo contrario, se recupera el reconocedor seleccionado. A continuación, se crea y se usa un contexto de reconocedor, y se actualizan el menú y la barra de estado.

El método **OnFactoidWordlist** de la ventana controla el comando **Usar lista** de palabras en el **menú Factoid.** La propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor se establece en **NULL** para restablecer el contexto del reconocedor. Si la **opción Usar lista de** palabras está desactivada, la propiedad [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del contexto del reconocedor se establece en **NULL**; De lo contrario, la propiedad **WordList** del contexto del reconocedor se establece en el [**objeto InkWordList**](inkwordlist-class.md) que se creó en **el método OnCreate.** Por último, se vuelve a separar [inkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de lápiz al contexto del reconocedor, se llama al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor y se actualiza el menú.

El método **OnFactoid** de la ventana controla los comandos factoid en el **menú Factoid.** En primer lugar, establece la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor en **NULL,** establece la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del contexto del reconocedor en el factoid seleccionado y reasigna las [inkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de lápiz al contexto del reconocedor. Si el contexto del reconocedor admite el objeto [Factoid,](factoid-constants.md) se llama al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor. De lo contrario, se muestra un mensaje de error. Por último, se actualizan el menú y la barra de estado.

El método **OnGuide** de la ventana controla los comandos del **menú** Guía. Si el contexto del reconocedor admite las opciones de la guía, el método **OnGuide** establece la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor en **NULL,** establece la propiedad [**Guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) del contexto del reconocedor en la configuración de guía seleccionada, reasigna las [inkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de lápiz al contexto del reconocedor y llama al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor. De lo contrario, se muestra un mensaje de error. Por último, se actualizan la ventana de entrada, el menú y la barra de estado.

El método **OnMode** de la ventana controla los comandos en el **menú** Modo. Deshabilita el recopilador de entrada de lápiz, actualiza la propiedad [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) del recopilador de entrada de lápiz, actualiza el menú y muestra u oculta las listas de gestos. Por último, el recopilador de entrada de lápiz está habilitado.

El método **OnRecognize de** la ventana controla el **comando Recognize** en el menú De entrada manuscrita. Llama al método [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) del contexto del reconocedor para evitar que se agrega lápiz al contexto del reconocedor. Esto a veces es necesario, ya que no todos los reconocedores admiten el reconocimiento parcial. A continuación, llama al método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del contexto del reconocedor y pasa los resultados al **método OnRecognitionWithAlternates** de la ventana. Por último, [las inkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de lápiz se reasignan al contexto del reconocedor.

El método **OnClear** de la ventana controla el **comando Borrar** en el menú **De entrada** manuscrita. Elimina los trazos de la propiedad [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) del recopilador de lápiz, libera la colección de trazos antiguos, crea uno nuevo para la propiedad **Ink** del recopilador de lápiz y asocia la nueva colección de trazos al contexto del reconocedor.

El método **OnExit** de la ventana controla el **comando Exit** en el **menú Ink** y genera el evento WM \_ CLOSE.

## <a name="helper-methods"></a>métodos del asistente

El método **LoadMenu** de la ventana se llama desde el método **Run** de la ventana y agrega la lista de reconocedores admitidos y la lista de factoids admitidos al menú. En primer lugar, recupera [inkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)). A continuación, recorre en iteración los reconocedores disponibles y solo selecciona los que tienen una lista de idiomas en la propiedad **Idiomas,** que agrega al **menú Reconocedor.** Por último, rellena el menú **Factoid** con la lista de factoids definida como una constante global.

Se llama al **método UseRecognizer** de la ventana desde el método **OnRecognizer** de la ventana cuando el usuario selecciona un nuevo reconocedor. Crea un contexto de reconocedor, separa el contexto anterior del receptor de eventos del reconocedor, borra y libera el contexto anterior y asocia el nuevo contexto al receptor de eventos del reconocedor.

A continuación, **el método UseRecognizer** comprueba la propiedad [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del reconocedor, que devuelve un [**valor InkRecognizerCapabilities.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities) Si el reconocedor admite entradas alineadas, el **comando Líneas** del **menú** Guía está habilitado. Si el reconocedor admite la entrada boxed, el **comando Boxes** está habilitado. Si el reconocedor no admite la entrada gratuita, el **comando None** está deshabilitado. Si no se admite la selección de la guía actual, se actualizan la propiedad [**Guía**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) del contexto del reconocedor y el menú.

A continuación, **el método UseRecognizer** intenta establecer las propiedades [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) y [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del contexto del reconocedor. Si el reconocedor no admite cualquiera de las opciones, se usa el valor predeterminado y se actualiza el menú.

Por último, el método **UseRecognizer** asocia la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del objeto [**InkDisp**](inkdisp-class.md) del recopilador de lápiz al contexto del reconocedor, cambia la fuente de la ventana de salida a una compatible con el lenguaje del reconocedor, restablece la ventana de salida y actualiza los resultados del reconocimiento llamando al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor.

Se llama al **método GetGestureName de** la ventana desde el **método OnGesture de la** ventana. Busca el gesto y devuelve un índice al nombre del gesto, que se almacena en una tabla de cadenas en el archivo AdvReco.rc.

 

 
