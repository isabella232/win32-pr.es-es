---
title: Usar la priorización de flujos
description: Usar la priorización de flujos
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- Windows Media Format SDK, priorización de flujos
- perfiles, priorización de flujos
- flujos, priorización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a6b0bd3d49db9523ef9ea5585803b4c703c279
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994927"
---
# <a name="using-stream-prioritization"></a><span data-ttu-id="7759b-106">Usar la priorización de flujos</span><span class="sxs-lookup"><span data-stu-id="7759b-106">Using Stream Prioritization</span></span>

<span data-ttu-id="7759b-107">La priorización de flujos permite tener más control sobre la reproducción de contenido permitiéndole especificar el orden de prioridad de las secuencias en un perfil.</span><span class="sxs-lookup"><span data-stu-id="7759b-107">Stream prioritization enables you to have more control over the playback of content by allowing you to specify priority order for the streams in a profile.</span></span> <span data-ttu-id="7759b-108">Cuando el lector y el servidor de streaming detectan una escasez de ancho de banda durante la reproducción, es posible que se deban quitar ejemplos para proporcionar una reproducción ininterrumpida.</span><span class="sxs-lookup"><span data-stu-id="7759b-108">When the reader and streaming server encounter a bandwidth shortage during playback, samples may have to be dropped to provide uninterrupted playback.</span></span> <span data-ttu-id="7759b-109">Si especifica un orden de prioridad con un objeto de priorización de flujo en el perfil, los ejemplos se quitarán primero de las secuencias de prioridad más baja.</span><span class="sxs-lookup"><span data-stu-id="7759b-109">If you specify a priority order with a stream prioritization object in the profile, samples will be dropped from the lowest priority streams first.</span></span>

<span data-ttu-id="7759b-110">A diferencia de los objetos de uso compartido de ancho de banda y de exclusión mutua, un objeto de priorización de flujo no utiliza la interfaz [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) para realizar un seguimiento de la lista de secuencias.</span><span class="sxs-lookup"><span data-stu-id="7759b-110">Unlike bandwidth sharing and mutual exclusion objects, a stream prioritization object does not use the [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) interface to keep track of the list of streams.</span></span> <span data-ttu-id="7759b-111">En su lugar, debe usar una matriz de estructuras de [**registro de prioridad de secuencia de WM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) .</span><span class="sxs-lookup"><span data-stu-id="7759b-111">Instead, you must use an array of [**WM\_STREAM\_PRIORITY\_RECORD**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) structures.</span></span> <span data-ttu-id="7759b-112">Las estructuras deben organizarse en la matriz en orden descendente de prioridad.</span><span class="sxs-lookup"><span data-stu-id="7759b-112">The structures must be organized in the array in descending order of priority.</span></span> <span data-ttu-id="7759b-113">Además de contener un número de secuencia, la estructura de prioridad de flujo también le permite especificar si una secuencia es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="7759b-113">In addition to holding a stream number, the stream priority structure also enables you to specify whether a stream is mandatory.</span></span> <span data-ttu-id="7759b-114">Los flujos obligatorios no se quitarán, independientemente de su posición en la lista.</span><span class="sxs-lookup"><span data-stu-id="7759b-114">Mandatory streams will not be dropped, regardless of their position in the list.</span></span>

<span data-ttu-id="7759b-115">En el ejemplo de código siguiente se muestra cómo incluir una priorización de flujo en un perfil.</span><span class="sxs-lookup"><span data-stu-id="7759b-115">The following example code shows how to include a stream prioritization in a profile.</span></span> <span data-ttu-id="7759b-116">Este perfil es para una presentación en aulas, con una secuencia de audio del hablante, una secuencia de vídeo del profesor y un flujo de vídeo que captura las diapositivas de presentación.</span><span class="sxs-lookup"><span data-stu-id="7759b-116">This profile is for a classroom presentation, with an audio stream of the lecturer speaking, a video stream of the lecturer, and a video stream capturing the presentation slides.</span></span> <span data-ttu-id="7759b-117">La secuencia de audio es la más importante y será obligatoria.</span><span class="sxs-lookup"><span data-stu-id="7759b-117">The audio stream is the most important and will be mandatory.</span></span> <span data-ttu-id="7759b-118">Las diapositivas de presentación tendrán la prioridad más baja, ya que la imagen será bastante constante, por lo que algunos fotogramas se perderán aquí y no habrá mucha diferencia.</span><span class="sxs-lookup"><span data-stu-id="7759b-118">The presentation slides will have the lowest priority because the image will be pretty constant, so a few frames lost here and there won't make much difference.</span></span>


```C++
IWMProfileManager*       pProfileMgr = NULL;
IWMProfile*              pProfileTmp = NULL;
IWMProfile3*             pProfile    = NULL;
IWMStreamPrioritization* pPriority   = NULL;

WM_STREAM_PRIORITY_RECORD StreamArray[3];
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfileTmp)

// Get the IWMProfile3 for the new profile, then release the old one.
hr = pProfileTmp->QueryInterface(IID_IWMProfile3, (void**)&pProfile);
pProfileTmp->Release();
pProfileTmp = NULL;

// Give the new profile a name and description.
hr = pProfile->SetName(L"Prioritization_Example");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Audio, &pStream);

// TODO: configure the stream as needed for the scenario.

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Give the stream a name for clarity.
hr = pStream->SetStreamName(L"Lecturer_Audio");

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// Repeat for the other two streams.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(2);
hr = pStream->SetStreamName(L"Lecturer_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(3);
hr = pStream->SetStreamName(L"Slide_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Create a stream prioritization object.
hr = pProfile->CreateNewStreamPrioritization(&pPriority);

// Fill the array with data.
StreamArray[0].wStreamNum = 1;
StreamArray[0].fMandatory = TRUE;

StreamArray[1].wStreamNum = 2;
StreamArray[1].fMandatory = FALSE;

StreamArray[2].wStreamNum = 3;
StreamArray[2].fMandatory = FALSE;

// Assign the stream array to the stream prioritization object.
hr = pPriority->SetPriorityRecords(StreamArray, 3);

// Add the stream prioritization to the profile.
hr = pProfile->SetStreamPrioritization(pPriority);

// Release the stream prioritization object.
pPriority->Release();
pPriority = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release the remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="7759b-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7759b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7759b-120">**Trabajar con perfiles**</span><span class="sxs-lookup"><span data-stu-id="7759b-120">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




