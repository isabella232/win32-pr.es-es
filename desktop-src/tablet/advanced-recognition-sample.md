---
description: En el ejemplo de reconocimiento avanzado se muestran las características avanzadas de la interfaz de programación de aplicaciones (API) de automatización de Microsoft Tablet PC que se usa para el reconocimiento de escritura a mano.
ms.assetid: 4c9b9f31-c317-43fd-8404-35295b41d093
title: Ejemplo de reconocimiento avanzado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e23a078ded9c6967f8e45780f8cb3a739b246f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807988"
---
# <a name="advanced-recognition-sample"></a>Ejemplo de reconocimiento avanzado

En el ejemplo de reconocimiento avanzado se muestran las características avanzadas de la interfaz de programación de aplicaciones (API) de automatización de Microsoft Tablet PC que se usa para el reconocimiento de escritura a mano.

Contiene las características siguientes:

-   Enumerar el reconocedor instalado
-   Crear un contexto de reconocedor con un idioma específico
-   Usar el objeto Recognizer
-   Configuración de Factoid de reconocimiento y listas de palabras
-   Usar guías para mejorar la calidad del reconocimiento
-   Reconocimiento en segundo plano dinámico
-   Reconocimiento de gestos

Las interfaces utilizadas son: [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer), **IInkRecoContext**, [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult), **IInkRecognitionGuide**, **IInkWordList**, [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture), **IInkCollector**, **IInkDisp**, **IInkRenderer**, **IInkDrawingAttributes**, **IInkStrokes** y **IInkStroke**.

## <a name="ink-and-project-headers"></a>Encabezados de lápiz y de proyecto

En primer lugar, incluya los encabezados de las interfaces de automatización de Tablet PC. Se instalan con el SDK de la plataforma de Tablet PC. El archivo TpcError. h contiene las definiciones de código de error de la API de Tablet PC.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
#include <TpcError.h>
```



El archivo EventSinks. h define las interfaces **IInkEventsImpl** y **IInkRecognitionEventsImpl** , y configura los eventos [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md), [**Stroke**](inkcollector-stroke.md)y [**gesto**](inkcollector-gesture.md) .


```C++
#include "EventSinks.h"
```



El archivo ChildWnds. h contiene las definiciones de las clases **CInkInputWnd** y **CRecoOutputWnd**, que se derivan del CWindowImpl de ATL y se usan para crear las ventanas secundarias del ejemplo.


```C++
#include "ChildWnds.h"
```



El archivo AdvReco. h declara la clase **CAdvRecoApp** , que es la clase de ventana de la aplicación para este ejemplo.


```C++
#include "AdvReco.h"
```



## <a name="initializing-the-application-window"></a>Inicialización de la ventana de la aplicación

El método de la ventana `Run` configura el objeto **CAdvRecoApp** , carga el menú y el icono de la ventana, crea un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) para el reconocedor predeterminado e inicia el bucle de mensajes de la ventana.

El método **alcrear** de la ventana controla el evento de **\_ creación de WM** y crea las ventanas secundarias. Un objeto [**InkCollector**](inkcollector-class.md) se conecta al origen de eventos del recopilador de tinta y habilita la entrada de lápiz en la ventana de entrada. A continuación, se crea un objeto [**InkRecognizerGuide**](inkrecognizerguide-class.md) y se usa la propiedad [**representador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer) del recopilador de tinta para convertir los rectángulos del cuadro guía de reconocimiento en el espacio de tinta. Por último, el método **alcrear** crea un objeto [**InkWordList**](inkwordlist-class.md) .

## <a name="handling-ink-collector-events"></a>Controlar eventos del recopilador de tinta

El método stroke de la ventana controla el evento [**Stroke**](inkcollector-stroke.md) del recopilador **de tinta** . El nuevo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) se agrega al [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de la propiedad [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) del recopilador de tinta.

El método de **gestos** de la ventana controla el evento de [**gesto**](inkcollector-gesture.md) del recopilador de tinta. El método de **gestos de movimiento** identifica el gesto, utilizando primero el gesto de mayor confianza y comprueba si la ventana admite este gesto en particular. Si se admite el gesto, se invalida el rectángulo de selección del gesto, ya que el gesto se quita de la colección de trazos. Si no se admite el gesto, se cancela el evento de **gesto** , lo que hace que el recopilador de tinta genere un evento de [**trazo**](inkcollector-stroke.md) . Por último, se actualiza la ventana resultados.

## <a name="handling-recognizer-context-events"></a>Controlar eventos de contexto de reconocedor

El método **OnRecognitionWithAlternates** de la ventana controla el evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) del contexto del reconocedor. El método **OnRecognitionWithAlternates** muestra los resultados del reconocimiento en la ventana resultados.

## <a name="handling-menu-commands"></a>Control de comandos de menú

El método de **reconocedor** de la ventana controla los comandos en el menú del reconocedor. Si se selecciona el comando **predeterminado** , se utiliza el método [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) de [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) para recuperar el reconocedor predeterminado; de lo contrario, se recupera el reconocedor seleccionado. A continuación, se crea y se usa un contexto de reconocedor y se actualiza el menú y la barra de estado.

El método **OnFactoidWordlist** de la ventana controla el comando usar la franja de **palabras** en el menú **Factoid** . La propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor se establece en **null** para restablecer el contexto del reconocedor. Si la opción usar la de **palabras** es desactivada, la propiedad de la definición de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del contexto del reconocedor se establece en **null**. de lo contrario, **la propiedad de** la definición de tipo del contexto del reconocedor se establece en el [**InkWordList**](inkwordlist-class.md) que se creó en el método **alcrear** . Por último, el [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de tinta se vuelve a adjuntar al contexto del reconocedor, se llama al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor y se actualiza el menú.

El método **OnFactoid** de la ventana controla los comandos Factoid en el menú **Factoid** . Primero establece la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor en **null**, establece la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del contexto del reconocedor en el Factoid seleccionado y reasigna el [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de tinta al contexto del reconocedor. Si el objeto [Factoid](factoid-constants.md) es compatible con el contexto del reconocedor, se llama al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor; de lo contrario, se muestra un mensaje de error. Por último, se actualizan el menú y la barra de estado.

El método en la **Guía** de la ventana controla los comandos del menú **Guía** . Si el contexto del reconocedor admite las **Opciones de la** guía, el método InkStrokes establece la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor en **null**, establece la propiedad [**Guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) del contexto del reconocedor en la configuración de la guía seleccionada, vuelve a asignar el [](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de tinta al contexto del reconocedor y llama al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor. De lo contrario, se muestra un mensaje de error. Por último, se actualizan la ventana de entrada, el menú y la barra de estado.

El método **bimode** de la ventana controla los comandos del menú **modo** . Deshabilita el recopilador de tinta, actualiza la propiedad [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) del recopilador de tinta, actualiza el menú y muestra u oculta las listas de gestos. Por último, el recopilador de tinta está habilitado.

El método **alrecognize** de la ventana controla el comando **Recognize** en el menú de entrada manuscrita. Llama al método [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) del contexto del reconocedor para mantener la entrada de lápiz en el contexto del reconocedor. A veces, esto es necesario, ya que no todos los reconocedores admiten el reconocimiento parcial. A continuación, llama al método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del contexto del reconocedor y pasa los resultados al método **OnRecognitionWithAlternates** de la ventana. Por último, el [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de tinta se reasigna al contexto del reconocedor.

El método **unclear** de la ventana controla el comando **Borrar** en el menú de **entrada manuscrita** . Elimina los trazos de la propiedad [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) del recopilador de tinta, libera la colección de trazos anteriores y crea una nueva para la propiedad **Ink** del recopilador de tinta y adjunta la nueva colección Strokes al contexto del reconocedor.

El **método OnExit** de la ventana controla el comando **Exit** en el menú de **entrada manuscrita** y genera el evento de cierre de WM \_ .

## <a name="helper-methods"></a>métodos del asistente

Se llama al método **LoadMenu** de la ventana desde el método **Run** de la ventana y se agrega la lista de reconocedores admitidos y la lista de Factoids admitidos al menú. En primer lugar, recupera el [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)). A continuación, recorre en iteración los reconocedores disponibles y solo selecciona aquellos que tengan una lista de idiomas en la propiedad **Languages** , que se agrega al menú de **reconocedor** . Por último, rellena el menú **Factoid** con la lista de Factoids definida como constante global.

El método **UseRecognizer** de la ventana se llama desde el método de **reconocedor** de la ventana cuando el usuario selecciona un nuevo reconocedor. Crea un contexto de reconocedor, Desasocia el contexto anterior del receptor de eventos del reconocedor, borra y libera el contexto anterior y asocia el nuevo contexto al receptor de eventos del reconocedor.

A continuación, el método **UseRecognizer** comprueba la propiedad [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del reconocedor, que devuelve un valor [**InkRecognizerCapabilities**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities) . Si el reconocedor admite la entrada alineada, el comando **líneas** del menú **Guía** está habilitado. Si el reconocedor admite la entrada de conversión boxing, el comando de **cuadros** está habilitado. Si el Reconocedor no admite la entrada libre, el comando **None** se deshabilita. Si no se admite la selección de la guía actual, se actualizan la propiedad [**Guía**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) del contexto del reconocedor y el menú.

A continuación, el método **UseRecognizer** intenta establecer las propiedades de la definición de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) y [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del contexto del reconocedor. Si el Reconocedor no admite cualquiera de las opciones de configuración, se usa el valor predeterminado y se actualiza el menú.

Por último, el método **UseRecognizer** asocia la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del objeto [**InkDisp**](inkdisp-class.md) del recopilador de tinta al contexto del reconocedor, cambia la fuente de la ventana de salida a una compatible con el idioma del reconocedor, restablece la ventana de salida y actualiza los resultados del reconocimiento llamando al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor.

Se llama al método **GetGestureName** de la ventana desde el método de **gestos** de la ventana. Busca el gesto y devuelve un índice al nombre del gesto, que se almacena en una tabla de cadenas en el archivo AdvReco. rc.

 

 
