---
description: Este ejemplo muestra las características avanzadas de la interfaz de programación de aplicaciones (API) de automatización de MicrosoftTablet PC que se usa para el reconocimiento de escritura a mano.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Ejemplo de varios reconocedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a21d24001e3544be16dde4d288a8adc7ea0081f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659932"
---
# <a name="multiple-recognizers-sample"></a><span data-ttu-id="54a73-103">Ejemplo de varios reconocedores</span><span class="sxs-lookup"><span data-stu-id="54a73-103">Multiple Recognizers Sample</span></span>

<span data-ttu-id="54a73-104">Este ejemplo muestra las características avanzadas de la interfaz de programación de aplicaciones (API) de automatización de MicrosoftTablet PC que se usa para el reconocimiento de *escritura a mano* .</span><span class="sxs-lookup"><span data-stu-id="54a73-104">This sample demonstrates advanced features of the MicrosoftTablet PC Automation application programming interface (API) used for *handwriting* recognition.</span></span>

<span data-ttu-id="54a73-105">Incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="54a73-105">It includes the following:</span></span>

-   <span data-ttu-id="54a73-106">Enumerar los reconocedores instalados</span><span class="sxs-lookup"><span data-stu-id="54a73-106">Enumerating the installed recognizers</span></span>
-   <span data-ttu-id="54a73-107">Crear un *contexto de reconocedor* con un reconocedor de idioma específico</span><span class="sxs-lookup"><span data-stu-id="54a73-107">Creating a *recognizer context* with a specific language recognizer</span></span>
-   <span data-ttu-id="54a73-108">Serialización de los resultados del reconocimiento con una colección de trazos</span><span class="sxs-lookup"><span data-stu-id="54a73-108">Serializing recognition results with a stroke collection</span></span>
-   <span data-ttu-id="54a73-109">Organizar colecciones de trazos en una colección personalizada dentro del objeto [**InkDisp**](inkdisp-class.md)</span><span class="sxs-lookup"><span data-stu-id="54a73-109">Organizing stroke collections into a custom collection within the [**InkDisp**](inkdisp-class.md) object</span></span>
-   <span data-ttu-id="54a73-110">Serializar objetos de *entrada manuscrita* y recuperarlos de un archivo de *formato serializado de tinta (ISF)*</span><span class="sxs-lookup"><span data-stu-id="54a73-110">Serializing *ink* objects to and retrieving them from an *ink serialized format (ISF)* file</span></span>
-   <span data-ttu-id="54a73-111">Configuración de guías de entrada de reconocedor</span><span class="sxs-lookup"><span data-stu-id="54a73-111">Setting recognizer input guides</span></span>
-   <span data-ttu-id="54a73-112">Uso del reconocimiento sincrónico y asincrónico</span><span class="sxs-lookup"><span data-stu-id="54a73-112">Using synchronous and asynchronous recognition</span></span>

## <a name="ink-headers"></a><span data-ttu-id="54a73-113">Encabezados de entrada manuscrita</span><span class="sxs-lookup"><span data-stu-id="54a73-113">Ink Headers</span></span>

<span data-ttu-id="54a73-114">En primer lugar, incluya los encabezados de las interfaces de automatización de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="54a73-114">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="54a73-115">Se instalan con el kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="54a73-115">These are installed with the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="54a73-116">El archivo EventSinks. h define las interfaces IInkEventsImpl y IInkRecognitionEventsImpl.</span><span class="sxs-lookup"><span data-stu-id="54a73-116">The EventSinks.h file defines the IInkEventsImpl and IInkRecognitionEventsImpl interfaces.</span></span>


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a><span data-ttu-id="54a73-117">Enumerar los reconocedores instalados</span><span class="sxs-lookup"><span data-stu-id="54a73-117">Enumerating the Installed Recognizers</span></span>

<span data-ttu-id="54a73-118">El método LoadMenu de la aplicación rellena el menú crear nuevos trazos con los reconocedores disponibles.</span><span class="sxs-lookup"><span data-stu-id="54a73-118">The application's LoadMenu method populates the Create New Strokes menu with the available recognizers.</span></span> <span data-ttu-id="54a73-119">Se crea un [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="54a73-119">An [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is created.</span></span> <span data-ttu-id="54a73-120">Si la propiedad [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) de un objeto **InkRecognizers** no está vacía, el reconocedor es un *reconocedor de texto* y el valor de su propiedad [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) se agrega al menú.</span><span class="sxs-lookup"><span data-stu-id="54a73-120">If the [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property of an **InkRecognizers** object is not empty, then the recognizer is a *text recognizer*, and the value of its [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) property is added to the menu.</span></span>


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



## <a name="creating-an-ink-collector"></a><span data-ttu-id="54a73-121">Crear un recopilador de tinta</span><span class="sxs-lookup"><span data-stu-id="54a73-121">Creating an Ink Collector</span></span>

<span data-ttu-id="54a73-122">El método de creación de la aplicación crea un objeto [**InkCollector**](inkcollector-class.md) , lo conecta a su origen de eventos y habilita la colección de entradas de lápiz.</span><span class="sxs-lookup"><span data-stu-id="54a73-122">The application's OnCreate method creates an [**InkCollector**](inkcollector-class.md) object, connects it to its event source, and enables ink collection.</span></span>


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a><span data-ttu-id="54a73-123">Crear un contexto de reconocedor</span><span class="sxs-lookup"><span data-stu-id="54a73-123">Creating a Recognizer Context</span></span>

<span data-ttu-id="54a73-124">El método CreateRecoContext de la aplicación crea e inicializa un nuevo contexto de reconocedor y configura las guías admitidas por el lenguaje asociado.</span><span class="sxs-lookup"><span data-stu-id="54a73-124">The application's CreateRecoContext method creates and initializes a new recognizer context, and sets up the guides supported by the associated language.</span></span> <span data-ttu-id="54a73-125">El método [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) del objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) crea un objeto [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) para el lenguaje.</span><span class="sxs-lookup"><span data-stu-id="54a73-125">The [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method creates a [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) object for the language.</span></span> <span data-ttu-id="54a73-126">Si es necesario, se reemplaza el contexto del reconocedor antiguo.</span><span class="sxs-lookup"><span data-stu-id="54a73-126">If necessary, the old recognizer context is replaced.</span></span> <span data-ttu-id="54a73-127">El contexto está conectado a su origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="54a73-127">The context is connected to its event source.</span></span> <span data-ttu-id="54a73-128">Por último, se comprueba la propiedad [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del contexto del reconocedor para las guías que admite el contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="54a73-128">Finally, the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the recognizer context is checked for which guides the recognizer context supports.</span></span>


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



## <a name="collecting-strokes-and-displaying-recognition-results"></a><span data-ttu-id="54a73-129">Recopilar trazos y mostrar los resultados del reconocimiento</span><span class="sxs-lookup"><span data-stu-id="54a73-129">Collecting Strokes and Displaying Recognition Results</span></span>

<span data-ttu-id="54a73-130">El método [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de la aplicación actualiza el recolector de tintas, cancela las solicitudes de reconocimiento asincrónicas existentes y crea una solicitud de reconocimiento en el contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="54a73-130">The application's OnStroke method updates the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) of the ink collector, cancels existing asynchronous recognition requests, and creates a recognition request on the recognizer context.</span></span>


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



<span data-ttu-id="54a73-131">El método de la aplicación `OnRecognition` envía los resultados de la solicitud de reconocimiento al método de la ventana de salida `UpdateString` .</span><span class="sxs-lookup"><span data-stu-id="54a73-131">The application's `OnRecognition` method sends the results of the recognition request to the output window's `UpdateString` method.</span></span>


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a><span data-ttu-id="54a73-132">Eliminar trazos y resultados de reconocimiento</span><span class="sxs-lookup"><span data-stu-id="54a73-132">Deleting Strokes and Recognition Results</span></span>

<span data-ttu-id="54a73-133">El método unclear de la aplicación elimina todos los trazos y los resultados de reconocimiento del objeto [**InkDisp**](inkdisp-class.md) y borra las ventanas.</span><span class="sxs-lookup"><span data-stu-id="54a73-133">The application's OnClear method deletes all strokes and recognition results from the [**InkDisp**](inkdisp-class.md) object and clears the windows.</span></span> <span data-ttu-id="54a73-134">Se quita la Asociación del contexto del reconocedor con su colección [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="54a73-134">The recognizer context's association with its [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is removed.</span></span>


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



## <a name="changing-recognizer-contexts"></a><span data-ttu-id="54a73-135">Cambiar contextos de reconocedor</span><span class="sxs-lookup"><span data-stu-id="54a73-135">Changing Recognizer Contexts</span></span>

<span data-ttu-id="54a73-136">Se llama al método OnNewStrokes de la aplicación cuando el usuario selecciona un reconocedor en el menú crear nuevos trazos.</span><span class="sxs-lookup"><span data-stu-id="54a73-136">The application's OnNewStrokes method is called when the user selects a recognizer in the Create New Strokes menu.</span></span> <span data-ttu-id="54a73-137">Se guarda el [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) actual.</span><span class="sxs-lookup"><span data-stu-id="54a73-137">The current [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) is saved.</span></span> <span data-ttu-id="54a73-138">Si se ha seleccionado un reconocedor de idioma diferente, se crea un nuevo contexto de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="54a73-138">If a different language recognizer was selected, a new recognizer context is created.</span></span> <span data-ttu-id="54a73-139">A continuación, se adjunta un nuevo **InkStrokes** al nuevo contexto de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="54a73-139">Then, a new **InkStrokes** is attached to the new recognizer context.</span></span>


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



<span data-ttu-id="54a73-140">A continuación, llama a StartNewStrokeCollection, que crea un [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) vacío y lo adjunta al contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="54a73-140">It then calls StartNewStrokeCollection, which creates an empty [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) and attaches it to the recognizer context.</span></span>

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a><span data-ttu-id="54a73-141">Guardar la colección de trazos para un contexto de reconocedor</span><span class="sxs-lookup"><span data-stu-id="54a73-141">Saving the Strokes Collection for a Recognizer Context</span></span>

<span data-ttu-id="54a73-142">El método de la aplicación `SaveStrokeCollection` comprueba un contexto de reconocedor existente y finaliza el reconocimiento de la colección de trazos actual.</span><span class="sxs-lookup"><span data-stu-id="54a73-142">The application's `SaveStrokeCollection` method checks for an existing recognizer context, and finalizes the recognition of the current strokes collection.</span></span> <span data-ttu-id="54a73-143">A continuación, la colección [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) se agrega a la [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) del objeto de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="54a73-143">Then the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is added to the [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) of the ink object.</span></span>


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



 

 
