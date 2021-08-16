---
description: En este ejemplo se muestran las características avanzadas de la interfaz de programación de aplicaciones (API) de Automatización de PC de MicrosoftTablet que se usa para el reconocimiento de escritura a mano.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Ejemplo de varios reconocedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d687f1bddd1f3c57cc482070b8e5826126b6e5b0f716fa3649df01ad6eab30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856554"
---
# <a name="multiple-recognizers-sample"></a>Ejemplo de varios reconocedores

En este ejemplo se muestran las características avanzadas de la interfaz de programación de aplicaciones (API) de Automatización de PC de MicrosoftTablet que se usa para el *reconocimiento de escritura* a mano.

Incluye lo siguiente:

-   Enumeración de los reconocedores instalados
-   Creación de *un contexto de reconocedor* con un reconocedor de lenguaje específico
-   Serialización de resultados de reconocimiento con una colección de trazos
-   Organización de colecciones de trazos en una colección personalizada dentro del [**objeto InkDisp**](inkdisp-class.md)
-   Serializar *objetos de* entrada de lápiz en y recuperarlos de un archivo de formato serializado de entrada de lápiz *(ISF)*
-   Establecimiento de guías de entrada del reconocedor
-   Uso del reconocimiento sincrónico y asincrónico

## <a name="ink-headers"></a>Encabezados de entrada manuscrita

En primer lugar, incluya los encabezados de las interfaces de automatización de Tablet PC. Se instalan con el Kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



El archivo EventSinks.h define las interfaces IInkEventsImpl e IInkRecognitionEventsImpl.


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a>Enumerar los reconocedores instalados

El método LoadMenu de la aplicación rellena el menú Crear nuevos trazos con los reconocedores disponibles. Se [**crea un elemento InkRecognizers.**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) Si la propiedad [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) de un objeto **InkRecognizers** no está vacía, el reconocedor es un reconocedor de texto y el valor de su propiedad [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) se agrega al menú.


```C++
// Create the enumerator for the installed recognizers
hr = m_spIInkRecognizers.CoCreateInstance(CLSID_InkRecognizers);
...
    // Filter out non-language recognizers by checking for
    // the languages supported by the recognizer - there is not
    // any if it is a gesture or object recognizer.
    CComVariant vLanguages;
    if (SUCCEEDED(spIInkRecognizer->get_Languages(&vLanguages)))
    {
        if ((VT_ARRAY == (VT_ARRAY & vLanguages.vt))           // it should be an array
            && (NULL != vLanguages.parray)
            && (0 < vLanguages.parray->rgsabound[0].cElements)) // with at least one element
        {
            // This is a language recognizer. Add its name to the menu.
            CComBSTR bstrName;
            if (SUCCEEDED(spIInkRecognizer->get_Name(&bstrName)))
                ...
        }
    }
```



## <a name="creating-an-ink-collector"></a>Creación de un recopilador de entrada de lápiz

El método OnCreate de la aplicación crea un [**objeto InkCollector,**](inkcollector-class.md) lo conecta a su origen de eventos y habilita la recopilación de entrada de lápiz.


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a>Crear un contexto de reconocedor

El método CreateRecoContext de la aplicación crea e inicializa un nuevo contexto de reconocedor y configura las guías admitidas por el lenguaje asociado. El método [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) del objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) crea un objeto [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) para el lenguaje. Si es necesario, se reemplaza el contexto del reconocedor anterior. El contexto está conectado a su origen de eventos. Por último, [**se comprueba la**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) propiedad Capabilities del contexto del reconocedor para las guías que admite el contexto del reconocedor.


```C++
// Create a recognizer context
CComPtr<IInkRecognizerContext2> spNewContext;
if (FAILED(pIInkRecognizer2->CreateRecognizerContext(&spNewContext)))
    return false;

// Replace the current context with the new one
if (m_spIInkRecoContext != NULL)
{
    // Close the connection to the recognition events source
    IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventUnadvise(m_spIInkRecoContext);
}
m_spIInkRecoContext.Attach(spNewContext.Detach());

// Establish a connection with the recognizer context's event source
if (FAILED(IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkRecoContext)))
    ...

// Set the guide if it's supported by the recognizer and has been created 
int cRows = 0, cColumns = 0;
InkRecognizerCapabilities dwCapabilities = IRC_DontCare;
if (SUCCEEDED(pIInkRecognizer->get_Capabilities(&dwCapabilities)))
    ...
```



## <a name="collecting-strokes-and-displaying-recognition-results"></a>Recopilar trazos y mostrar los resultados del reconocimiento

El método OnStroke de la aplicación actualiza [**inkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) del recopilador de lápiz, cancela las solicitudes de reconocimiento asincrónico existentes y crea una solicitud de reconocimiento en el contexto del reconocedor.


```C++
// Add the new stroke to the current collection
hr = m_spIInkStrokes->Add(pIInkStroke);

if (SUCCEEDED(hr))
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();

    // Ask the context to update the recognition results with newly added strokes
    // When the results are ready, the recognizer context returns them
    // through the corresponding event RecognitionWithAlternates
    CComVariant vCustomData;
    m_spIInkRecoContext->BackgroundRecognize(vCustomData);
}
```



El método de la `OnRecognition` aplicación envía los resultados de la solicitud de reconocimiento al método de la ventana de `UpdateString` salida.


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a>Eliminación de trazos y resultados de reconocimiento

El método OnClear de la aplicación elimina todos los trazos y los resultados de reconocimiento del objeto [**InkDisp**](inkdisp-class.md) y borra las ventanas. Se quita la asociación del contexto del reconocedor con [**su colección InkStrokes.**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))


```C++
// Detach the current stroke collection from the recognizer context and release it
if (m_spIInkRecoContext != NULL)
    m_spIInkRecoContext->putref_Strokes(NULL);

m_spIInkStrokes.Release();

// Clear the custom strokes collection
if (m_spIInkCustomStrokes != NULL)
    m_spIInkCustomStrokes->Clear();

// Delete all strokes from the Ink object
// Passing NULL as a stroke collection pointer means asking to delete all strokes
m_spIInkDisp->DeleteStrokes(NULL);

// Get a new stroke collection from the ink object
...
// Ask for an empty collection by passing an empty variant 
if (SUCCEEDED(m_spIInkDisp->CreateStrokes(v, &m_spIInkStrokes)))
{
    // Attach it to the recognizer context
    if (FAILED(m_spIInkRecoContext->putref_Strokes(m_spIInkStrokes)))
        ...
}
```



## <a name="changing-recognizer-contexts"></a>Cambiar contextos de reconocedor

Se llama al método OnNewStrokes de la aplicación cuando el usuario selecciona un reconocedor en el menú Crear nuevos trazos. Se guardan [**las inkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) actuales. Si se ha seleccionado otro reconocedor de idioma, se crea un nuevo contexto de reconocedor. A continuación, **se adjunta un nuevo inkStrokes** al nuevo contexto del reconocedor.


```C++
// Save the current stroke collection if there is any
if (m_spIInkRecoContext != NULL)
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();
    
    // Let the context know that there'll be no more input 
    // for the attached stroke collection
    m_spIInkRecoContext->EndInkInput();

    // Add the stroke collection to the Ink object's CustomStrokes collection
    SaveStrokeCollection();
}
...
// If a different recognizer was selected, create a new recognizer context
// Else, reuse the same recognizer context
if (wID != m_nCmdRecognizer)
{
    // Get a pointer to the recognizer object from the recognizer collection  
    CComPtr<IInkRecognizer> spIInkRecognizer;
    if ((m_spIInkRecognizers == NULL)
        || FAILED(m_spIInkRecognizers->Item(wID - ID_RECOGNIZER_FIRST,
                                             &spIInkRecognizer))
        || (false == CreateRecoContext(spIInkRecognizer)))
    {
        // restore the cursor
        ::SetCursor(hCursor);
        return 0;
    }

    // Update the status bar
    m_bstrCurRecoName.Empty();
    spIInkRecognizer->get_Name(&m_bstrCurRecoName);
    UpdateStatusBar();

    // Store the selected recognizer's command id
    m_nCmdRecognizer = wID;
}
```



A continuación, llama a StartNewStrokeCollection, que crea un [**objeto InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) vacío y lo asocia al contexto del reconocedor.

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a>Guardar la colección de trazos para un contexto de reconocedor

El método de la aplicación comprueba si hay un contexto de reconocedor existente y completa el reconocimiento de `SaveStrokeCollection` la colección de trazos actual. A [**continuación, la colección InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) se agrega a [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) del objeto ink.


```C++
if (m_spIInkRecoContext != NULL)
{
    if (SUCCEEDED(m_spIInkStrokes->get_Count(&lCount)) && 0 != lCount)
    {
        CComPtr<IInkRecognitionResult> spIInkRecoResult;
        InkRecognitionStatus RecognitionStatus;
        if (SUCCEEDED(m_spIInkRecoContext->Recognize(&RecognitionStatus, &spIInkRecoResult)))
        {
            if (SUCCEEDED(spIInkRecoResult->SetResultOnStrokes()))
            {
                CComBSTR bstr;
                spIInkRecoResult->get_TopString(&bstr);
                m_wndResults.UpdateString(bstr);
            }
            ...
        }
    }
    // Detach the stroke collection from the old recognizer context
    m_spIInkRecoContext->putref_Strokes(NULL);
}

// Now add it to the ink's custom strokes collection
// Each item (stroke collection) of the custom strokes must be identified
// by a unique string. Here we generate a GUID for this.
if ((0 != lCount) && (m_spIInkCustomStrokes != NULL))
{
    GUID guid;
    WCHAR szGuid[40]; // format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"
    if (SUCCEEDED(::CoCreateGuid(&guid)) 
        && (::StringFromGUID2(guid, szGuid, countof(szGuid)) != 0))
    {
        CComBSTR bstrGuid(szGuid);
        if (FAILED(m_spIInkCustomStrokes->Add(bstrGuid, m_spIInkStrokes)))
            ...
```



 

 
