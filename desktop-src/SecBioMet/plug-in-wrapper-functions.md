---
title: Funciones de contenedor de complementos
description: Funciones contenedoras que permiten llamar a una función pública en cualquier adaptador conectado a la canalización sin adquirir manualmente un puntero al adaptador.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- Plataforma de biometría de Windows API Plataforma de biometría de Windows API, funciones de contenedor de complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903757"
---
# <a name="plug-in-wrapper-functions"></a>Funciones de contenedor de complementos

La API de Plataforma de biometría de Windows incluye funciones contenedoras que permiten llamar a una función pública en cualquier adaptador conectado a la canalización sin adquirir manualmente un puntero al adaptador. Cada contenedor comprueba los argumentos de entrada, recupera un puntero de adaptador y llama a la función solicitada. Por ejemplo, el contenedor **WbioEngineSetHashAlgorithm** tiene la siguiente firma.


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



La función comprueba que el argumento de *canalización* no es **null**, que existe un adaptador de motor y que existe la función [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) . Todas las funciones de contenedor se definen en el \_ archivo de encabezado Adapter. h de Winbio. En los temas siguientes se describen los contenedores disponibles.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Contenedores de adaptadores de motor](engine-adapter-wrappers.md)<br/>   | Funciones que se pueden usar para llamar a funciones en el adaptador de motor. Estas funciones se definen en Winbio \_ Adapter. h.<br/>  |
| [Contenedores de adaptador de sensor](sensor-adapter-wrappers.md)<br/>   | Funciones que se pueden usar para llamar a funciones en el adaptador de sensor. Estas funciones se definen en Winbio \_ Adapter. h.<br/>  |
| [Contenedores del adaptador de almacenamiento](storage-adapter-wrappers.md)<br/> | Funciones que se pueden usar para llamar a funciones en el adaptador de almacenamiento. Estas funciones se definen en Winbio \_ Adapter. h.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del complemento](plug-in-reference.md)
</dt> </dl>

 

 





