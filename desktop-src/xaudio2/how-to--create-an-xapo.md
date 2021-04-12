---
description: La API de XAPO proporciona la interfaz IXAPO y la clase CXAPOBase para crear nuevos tipos XAPO.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Cómo: crear un XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549739462a0e76cbb437f0aa1403b099f72f5224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279366"
---
# <a name="how-to-create-an-xapo"></a><span data-ttu-id="4bb16-103">Cómo: crear un XAPO</span><span class="sxs-lookup"><span data-stu-id="4bb16-103">How to: Create an XAPO</span></span>

<span data-ttu-id="4bb16-104">La API de XAPO proporciona la interfaz [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y la clase [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para crear nuevos tipos XAPO.</span><span class="sxs-lookup"><span data-stu-id="4bb16-104">The XAPO API provides the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class for building new XAPO types.</span></span> <span data-ttu-id="4bb16-105">La interfaz **IXAPO** contiene todos los métodos que deben implementarse para crear un nuevo XAPO.</span><span class="sxs-lookup"><span data-stu-id="4bb16-105">The **IXAPO** interface contains all of the methods that need to be implemented to create a new XAPO.</span></span> <span data-ttu-id="4bb16-106">La clase **CXAPOBase** proporciona una implementación básica de la interfaz **IXAPO** .</span><span class="sxs-lookup"><span data-stu-id="4bb16-106">The **CXAPOBase** class provides a basic implementation of the **IXAPO** interface.</span></span> <span data-ttu-id="4bb16-107">**CXAPOBase** implementa todos los métodos de interfaz **IXAPO** , excepto el método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , que es único para cada XAPO.</span><span class="sxs-lookup"><span data-stu-id="4bb16-107">**CXAPOBase** implements all of the **IXAPO** interface methods except the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, which is unique to each XAPO.</span></span>

## <a name="to-create-a-new-static-xapo"></a><span data-ttu-id="4bb16-108">Para crear un nuevo XAPO estático</span><span class="sxs-lookup"><span data-stu-id="4bb16-108">To create a new static XAPO</span></span>

1.  <span data-ttu-id="4bb16-109">Derive una nueva clase XAPO de la clase base [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .</span><span class="sxs-lookup"><span data-stu-id="4bb16-109">Derive a new XAPO class from the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) base class.</span></span>

    > [!Note]  
    > <span data-ttu-id="4bb16-110">XAPOs implementa la interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="4bb16-110">XAPOs implement the **IUnknown** interface.</span></span> <span data-ttu-id="4bb16-111">Las interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluyen los tres métodos **IUnknown** : **QueryInterface**, **AddRef** y **Release**.</span><span class="sxs-lookup"><span data-stu-id="4bb16-111">The [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) and [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interfaces include the three **IUnknown** methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="4bb16-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) proporciona implementaciones de los tres métodos **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="4bb16-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) provides implementations of all three of the **IUnknown** methods.</span></span> <span data-ttu-id="4bb16-113">Una nueva instancia de **CXAPOBase** tendrá un recuento de referencias de 1.</span><span class="sxs-lookup"><span data-stu-id="4bb16-113">A new instance of **CXAPOBase** will have a reference count of 1.</span></span> <span data-ttu-id="4bb16-114">Se destruirá cuando su recuento de referencias se convierta en 0.</span><span class="sxs-lookup"><span data-stu-id="4bb16-114">It will be destroyed when its reference count becomes 0.</span></span> <span data-ttu-id="4bb16-115">Para permitir que XAudio2 destruya una instancia de XAPO cuando ya no sea necesaria, llame a **IUnknown:: Release** en XAPO una vez que se haya agregado a una cadena de efectos de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="4bb16-115">To allow XAudio2 to destroy an instance of an XAPO when it is no longer needed, call **IUnknown::Release** on the XAPO after it is added to an XAudio2 effect chain.</span></span> <span data-ttu-id="4bb16-116">Consulte [Cómo: usar un xapo en xaudio2](how-to--use-an-xapo-in-xaudio2.md) para más información sobre el uso de un Xapo con xaudio2.</span><span class="sxs-lookup"><span data-stu-id="4bb16-116">See [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) for more information about using an XAPO with XAudio2.</span></span>

     

2.  <span data-ttu-id="4bb16-117">Invalide la implementación de la clase [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) del método [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .</span><span class="sxs-lookup"><span data-stu-id="4bb16-117">Override the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class implementation of the [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) method.</span></span>

    <span data-ttu-id="4bb16-118">Invalidar [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) permite almacenar información sobre el formato de los datos de audio para su uso en [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="4bb16-118">Overriding [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) allows information about the format of audio data to be stored for use in [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

3.  <span data-ttu-id="4bb16-119">Implemente el método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .</span><span class="sxs-lookup"><span data-stu-id="4bb16-119">Implement the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method.</span></span>

    <span data-ttu-id="4bb16-120">XAudio2 llama al método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) siempre que un XAPO necesite procesar datos de audio.</span><span class="sxs-lookup"><span data-stu-id="4bb16-120">XAudio2 calls the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method whenever an XAPO needs to process audio data.</span></span> <span data-ttu-id="4bb16-121">El **proceso** contiene la mayor parte del código de un XAPO.</span><span class="sxs-lookup"><span data-stu-id="4bb16-121">**Process** contains the bulk of the code for an XAPO.</span></span>

## <a name="implementing-the-process-method"></a><span data-ttu-id="4bb16-122">Implementar el método Process</span><span class="sxs-lookup"><span data-stu-id="4bb16-122">Implementing the Process Method</span></span>

<span data-ttu-id="4bb16-123">El método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) acepta búferes de secuencia para los datos de audio de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="4bb16-123">The [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method accepts stream buffers for input and output audio data.</span></span> <span data-ttu-id="4bb16-124">Un XAPO típico esperará un búfer de flujo de entrada y un búfer de flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="4bb16-124">A typical XAPO will expect one input stream buffer and one output stream buffer.</span></span> <span data-ttu-id="4bb16-125">Debe basar el procesamiento de los datos del búfer del flujo de entrada en el formato especificado en la función [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) y cualquier marcador que se pase a la función **Process** con el búfer de flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="4bb16-125">You should base the processing of data from the input stream buffer on the format specified in the [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) function and any flags passed to the **Process** function with the input stream buffer.</span></span> <span data-ttu-id="4bb16-126">Copie los datos de búfer de flujo de entrada procesados en el búfer de flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="4bb16-126">Copy the processed input stream buffer data to the output stream buffer.</span></span> <span data-ttu-id="4bb16-127">Establezca el parámetro BufferFlags del búfer del flujo de salida como búfer de [**xapo \_ \_ válido**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) o **búfer de xapo en \_ \_ silencio**.</span><span class="sxs-lookup"><span data-stu-id="4bb16-127">Set the output stream buffer's BufferFlags parameter as either [**XAPO\_BUFFER\_VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) or **XAPO\_BUFFER\_SILENT**.</span></span>

<span data-ttu-id="4bb16-128">En el ejemplo siguiente se muestra una implementación de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) y [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que simplemente copia los datos de un búfer de entrada en un búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="4bb16-128">The following example demonstrates a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) and [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation that simply copies data from an input buffer to an output buffer.</span></span> <span data-ttu-id="4bb16-129">Sin embargo, no hay ningún procesamiento si el búfer de entrada se marca con [**búfer de XAPO \_ \_ silencioso**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span><span class="sxs-lookup"><span data-stu-id="4bb16-129">However, there is no processing if the input buffer is marked with [**XAPO\_BUFFER\_SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span></span>


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



<span data-ttu-id="4bb16-130">Al escribir un método de [**proceso**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , es importante tener en cuenta que los datos de audio de XAudio2 se intercalan.</span><span class="sxs-lookup"><span data-stu-id="4bb16-130">When writing a [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, it is important to note XAudio2 audio data is interleaved.</span></span> <span data-ttu-id="4bb16-131">Esto significa que los datos de cada canal son adyacentes para un número de muestra determinado.</span><span class="sxs-lookup"><span data-stu-id="4bb16-131">This means data from each channel is adjacent for a particular sample number.</span></span> <span data-ttu-id="4bb16-132">Por ejemplo, si hay una onda de 4 canales jugando en una voz de origen de XAudio2, los datos de audio son un ejemplo de canal 0, una muestra de canal 1, una muestra de canal 2, una muestra de canal 3 y, a continuación, la siguiente muestra de los canales 0, 1, 2, 3, etc.</span><span class="sxs-lookup"><span data-stu-id="4bb16-132">For example, if there is a 4-channel wave playing into an XAudio2 source voice, the audio data is a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bb16-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bb16-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bb16-134">Efectos de audio</span><span class="sxs-lookup"><span data-stu-id="4bb16-134">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="4bb16-135">Información general de XAPO</span><span class="sxs-lookup"><span data-stu-id="4bb16-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
