---
description: La API de XAPO proporciona la interfaz IXAPO y la clase CXAPOBase para crear nuevos tipos XAPO.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Cómo: crear un XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17729c5a6d872d98443c85f79dc72e8eee6dd2233b99f31e189a9eb28708e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583855"
---
# <a name="how-to-create-an-xapo"></a>Cómo: crear un XAPO

La API de XAPO proporciona la [**interfaz IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y la [**clase CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para crear nuevos tipos XAPO. La **interfaz IXAPO** contiene todos los métodos que deben implementarse para crear un nuevo XAPO. La **clase CXAPOBase** proporciona una implementación básica de la **interfaz IXAPO.** **CXAPOBase** implementa todos los métodos de interfaz **IXAPO,** excepto el método [**IXAPO::P rocess,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que es único para cada XAPO.

## <a name="to-create-a-new-static-xapo"></a>Para crear un nuevo XAPO estático

1.  Derive una nueva clase XAPO de la clase base [**CXAPOBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)

    > [!Note]  
    > Los XAPO implementan **la interfaz IUnknown.** Las [**interfaces IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluyen los tres métodos **IUnknown:** **QueryInterface,** **AddRef** y **Release.** [**CXAPOBase proporciona**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) implementaciones de los tres métodos **IUnknown.** Una nueva instancia de **CXAPOBase** tendrá un recuento de referencias de 1. Se destruirá cuando su recuento de referencias se convierta en 0. Para permitir que XAudio2 destruya una instancia de un XAPO cuando ya no se necesite, llame a **IUnknown::Release** en el XAPO después de agregarlo a una cadena de efectos XAudio2. Consulte [Cómo: Usar un XAPO en XAudio2](how-to--use-an-xapo-in-xaudio2.md) para obtener más información sobre el uso de un XAPO con XAudio2.

     

2.  Invalide [**la implementación de la clase CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) del método [**IXAPO::LockForProcess.**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)

    La [**invalidación de LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) permite almacenar información sobre el formato de los datos de audio para su uso en [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

3.  Implemente [**el método IXAPO::P rocess.**](/windows/win32/api/xapo/nf-xapo-ixapo-process)

    XAudio2 llama al [**método IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) cada vez que un XAPO necesita procesar datos de audio. **El** proceso contiene la mayor parte del código de un XAPO.

## <a name="implementing-the-process-method"></a>Implementar el método Process

El [**método IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) acepta búferes de flujo para los datos de audio de entrada y salida. Un XAPO típico esperará un búfer de flujo de entrada y un búfer de flujo de salida. Debe basar el procesamiento de datos del búfer de flujo de entrada en el formato especificado en la función [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) y cualquier marca que se pase a la función **Process** con el búfer de flujo de entrada. Copie los datos del búfer de flujo de entrada procesado en el búfer de flujo de salida. Establezca el parámetro BufferFlags del búfer del flujo de salida como [**XAPO \_ BUFFER \_ VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) o **XAPO \_ BUFFER \_ SILENT.**

En el ejemplo siguiente se muestra una [**implementación LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) [**y Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que simplemente copia datos de un búfer de entrada a un búfer de salida. Sin embargo, no hay ningún procesamiento si el búfer de entrada está marcado con [**XAPO \_ BUFFER \_ SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).


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



Al escribir un [**método Process,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) es importante tener en cuenta que los datos de audio XAudio2 están intercalados. Esto significa que los datos de cada canal son adyacentes para un número de muestra determinado. Por ejemplo, si hay una onda de 4 canales que se reproduce en una voz de origen XAudio2, los datos de audio son una muestra del canal 0, una muestra del canal 1, una muestra del canal 2, una muestra del canal 3 y, a continuación, la siguiente muestra de los canales 0, 1, 2, 3, y así sucesivamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Información general sobre XAPO](xapo-overview.md)
</dt> </dl>

 

 
