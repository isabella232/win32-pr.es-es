---
title: Funciones contenedoras de complementos
description: Funciones contenedoras que permiten llamar a una función pública en cualquier adaptador asociado a la canalización sin adquirir manualmente un puntero al adaptador.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- Windows API de Biometric Framework Windows BIOMETRIC Framework API, funciones contenedoras de complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b3f6991d0723f284bb95ecfd40d7931c48aa8647fb52e2b34a959791a7338b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101255"
---
# <a name="plug-in-wrapper-functions"></a>Funciones contenedoras de complementos

La API Windows Biometric Framework incluye funciones contenedoras que permiten llamar a una función pública en cualquier adaptador asociado a la canalización sin adquirir manualmente un puntero al adaptador. Cada contenedor comprueba los argumentos de entrada, recupera un puntero de adaptador y llama a la función solicitada. Por ejemplo, el **contenedor WbioEngineSetHashAlgorithm** tiene la firma siguiente.


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



La función comprueba que el argumento *Pipeline* no es **NULL,** que existe un adaptador de motor y que existe la función [**EngineAdapterSetHashAlgorithm.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) Todas las funciones contenedoras se definen en el archivo de encabezado \_ adapter.h de Winbio. En los temas siguientes se tratan los contenedores disponibles.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Contenedores del adaptador de motor](engine-adapter-wrappers.md)<br/>   | Funciones que puede usar para llamar a funciones en el adaptador del motor. Estas funciones se definen en Winbio \_ adapter.h.<br/>  |
| [Contenedores del adaptador de sensor](sensor-adapter-wrappers.md)<br/>   | Funciones que puede usar para llamar a funciones en el adaptador del sensor. Estas funciones se definen en Winbio \_ adapter.h.<br/>  |
| [Storage Contenedores de adaptadores](storage-adapter-wrappers.md)<br/> | Funciones que puede usar para llamar a funciones en el adaptador de almacenamiento. Estas funciones se definen en Winbio \_ adapter.h.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del complemento](plug-in-reference.md)
</dt> </dl>

 

 





