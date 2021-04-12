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
# <a name="how-to-create-an-xapo"></a>Cómo: crear un XAPO

La API de XAPO proporciona la interfaz [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y la clase [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para crear nuevos tipos XAPO. La interfaz **IXAPO** contiene todos los métodos que deben implementarse para crear un nuevo XAPO. La clase **CXAPOBase** proporciona una implementación básica de la interfaz **IXAPO** . **CXAPOBase** implementa todos los métodos de interfaz **IXAPO** , excepto el método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , que es único para cada XAPO.

## <a name="to-create-a-new-static-xapo"></a>Para crear un nuevo XAPO estático

1.  Derive una nueva clase XAPO de la clase base [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

    > [!Note]  
    > XAPOs implementa la interfaz **IUnknown** . Las interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluyen los tres métodos **IUnknown** : **QueryInterface**, **AddRef** y **Release**. [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) proporciona implementaciones de los tres métodos **IUnknown** . Una nueva instancia de **CXAPOBase** tendrá un recuento de referencias de 1. Se destruirá cuando su recuento de referencias se convierta en 0. Para permitir que XAudio2 destruya una instancia de XAPO cuando ya no sea necesaria, llame a **IUnknown:: Release** en XAPO una vez que se haya agregado a una cadena de efectos de XAudio2. Consulte [Cómo: usar un xapo en xaudio2](how-to--use-an-xapo-in-xaudio2.md) para más información sobre el uso de un Xapo con xaudio2.

     

2.  Invalide la implementación de la clase [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) del método [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .

    Invalidar [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) permite almacenar información sobre el formato de los datos de audio para su uso en [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

3.  Implemente el método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .

    XAudio2 llama al método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) siempre que un XAPO necesite procesar datos de audio. El **proceso** contiene la mayor parte del código de un XAPO.

## <a name="implementing-the-process-method"></a>Implementar el método Process

El método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) acepta búferes de secuencia para los datos de audio de entrada y salida. Un XAPO típico esperará un búfer de flujo de entrada y un búfer de flujo de salida. Debe basar el procesamiento de los datos del búfer del flujo de entrada en el formato especificado en la función [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) y cualquier marcador que se pase a la función **Process** con el búfer de flujo de entrada. Copie los datos de búfer de flujo de entrada procesados en el búfer de flujo de salida. Establezca el parámetro BufferFlags del búfer del flujo de salida como búfer de [**xapo \_ \_ válido**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) o **búfer de xapo en \_ \_ silencio**.

En el ejemplo siguiente se muestra una implementación de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) y [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que simplemente copia los datos de un búfer de entrada en un búfer de salida. Sin embargo, no hay ningún procesamiento si el búfer de entrada se marca con [**búfer de XAPO \_ \_ silencioso**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).


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



Al escribir un método de [**proceso**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , es importante tener en cuenta que los datos de audio de XAudio2 se intercalan. Esto significa que los datos de cada canal son adyacentes para un número de muestra determinado. Por ejemplo, si hay una onda de 4 canales jugando en una voz de origen de XAudio2, los datos de audio son un ejemplo de canal 0, una muestra de canal 1, una muestra de canal 2, una muestra de canal 3 y, a continuación, la siguiente muestra de los canales 0, 1, 2, 3, etc.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Información general de XAPO](xapo-overview.md)
</dt> </dl>

 

 
