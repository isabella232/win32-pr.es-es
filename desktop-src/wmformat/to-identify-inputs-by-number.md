---
title: Para identificar entradas por número
description: Para identificar entradas por número
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Advanced Systems Format (ASF), identificación de entradas por número
- ASF (formato de sistemas avanzados), identificar entradas por número
- perfiles, identificación de entradas por número
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077305"
---
# <a name="to-identify-inputs-by-number"></a><span data-ttu-id="ffab9-106">Para identificar entradas por número</span><span class="sxs-lookup"><span data-stu-id="ffab9-106">To Identify Inputs By Number</span></span>

<span data-ttu-id="ffab9-107">Cada muestra que se pasa al escritor debe estar asociada a un número de entrada.</span><span class="sxs-lookup"><span data-stu-id="ffab9-107">Every sample you pass to the writer must be associated with an input number.</span></span> <span data-ttu-id="ffab9-108">Cada número de entrada corresponde a una o más secuencias en el perfil que utiliza el escritor para escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="ffab9-108">Each input number corresponds to one or more streams in the profile that the writer is using to write the file.</span></span> <span data-ttu-id="ffab9-109">En un perfil, los orígenes multimedia se identifican mediante un nombre de conexión.</span><span class="sxs-lookup"><span data-stu-id="ffab9-109">In a profile, media sources are identified by a connection name.</span></span> <span data-ttu-id="ffab9-110">El escritor asocia un número de entrada con cada nombre de conexión cuando se establece el perfil para el escritor.</span><span class="sxs-lookup"><span data-stu-id="ffab9-110">The writer associates an input number with each connection name when you set the profile for the writer.</span></span> <span data-ttu-id="ffab9-111">Antes de poder pasar ejemplos al escritor, debe determinar qué datos esperan cada entrada.</span><span class="sxs-lookup"><span data-stu-id="ffab9-111">Before you can pass samples to the writer, you must determine what data each input is expecting.</span></span> <span data-ttu-id="ffab9-112">No se puede suponer que las entradas estarán en el mismo orden que los flujos de un perfil, aunque este sea el caso a menudo.</span><span class="sxs-lookup"><span data-stu-id="ffab9-112">You cannot assume that the inputs will be in the same order as the streams in a profile, even if this is often the case.</span></span> <span data-ttu-id="ffab9-113">Por lo tanto, la única manera confiable de hacer coincidir las entradas con secuencias es comparar el nombre de conexión de la entrada con el nombre de conexión de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ffab9-113">Therefore, the only reliable way to match inputs with streams is to compare the connection name of the input with the connection name of the stream.</span></span>

<span data-ttu-id="ffab9-114">Para identificar los nombres de conexión y los números de entrada correspondientes para un perfil cargado, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ffab9-114">To identify the connection names and corresponding input numbers for a loaded profile, perform the following steps:</span></span>

1.  <span data-ttu-id="ffab9-115">Cree un objeto de escritor y establezca un perfil para usarlo.</span><span class="sxs-lookup"><span data-stu-id="ffab9-115">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="ffab9-116">Para obtener más información sobre la configuración de perfiles en el escritor, vea [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="ffab9-116">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="ffab9-117">Debe conocer los nombres de conexión que se usan para las secuencias en el perfil.</span><span class="sxs-lookup"><span data-stu-id="ffab9-117">You should know the connection names used for the streams in the profile.</span></span> <span data-ttu-id="ffab9-118">Puede obtener el nombre de conexión desde dentro del perfil obteniendo el objeto de configuración de secuencia para cada flujo y llamando a [**IWMStreamConfig:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="ffab9-118">You can get the connection name from within the profile by getting the stream configuration object for each stream and calling [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span></span> <span data-ttu-id="ffab9-119">Para obtener más información sobre los perfiles y los objetos de configuración de secuencias, vea [trabajar con perfiles](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="ffab9-119">For more information about profiles and stream configuration objects, see [Working with Profiles](working-with-profiles.md).</span></span>
2.  <span data-ttu-id="ffab9-120">Recupere el número total de entradas mediante una llamada a [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span><span class="sxs-lookup"><span data-stu-id="ffab9-120">Retrieve the total number of inputs by calling [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span></span>
3.  <span data-ttu-id="ffab9-121">Recorra en bucle todas las entradas y realice los pasos siguientes para cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="ffab9-121">Loop through all of the inputs, performing the following steps for each.</span></span>
    -   <span data-ttu-id="ffab9-122">Recupere la interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para la entrada mediante una llamada a [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="ffab9-122">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
    -   <span data-ttu-id="ffab9-123">Recupere el nombre de conexión que corresponde al número de entrada mediante una llamada a [**IWMInputMediaProps:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="ffab9-123">Retrieve the connection name that corresponds to the input number by calling [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span></span> <span data-ttu-id="ffab9-124">Una vez que tenga el nombre de la conexión, conocerá los flujos que están asociados a los números de entrada asignados por el escritor.</span><span class="sxs-lookup"><span data-stu-id="ffab9-124">After you have the connection name, you know the streams that are associated with the input numbers assigned by the writer.</span></span>

<span data-ttu-id="ffab9-125">En el ejemplo de código siguiente se muestra el nombre de la conexión para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="ffab9-125">The following example code displays the connection name for each input.</span></span> <span data-ttu-id="ffab9-126">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ffab9-126">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="ffab9-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffab9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffab9-128">**Interfaz IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="ffab9-128">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="ffab9-129">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="ffab9-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




