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
# <a name="plug-in-wrapper-functions"></a><span data-ttu-id="2f7f9-104">Funciones de contenedor de complementos</span><span class="sxs-lookup"><span data-stu-id="2f7f9-104">Plug-in Wrapper Functions</span></span>

<span data-ttu-id="2f7f9-105">La API de Plataforma de biometría de Windows incluye funciones contenedoras que permiten llamar a una función pública en cualquier adaptador conectado a la canalización sin adquirir manualmente un puntero al adaptador.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-105">The Windows Biometric Framework API includes wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span> <span data-ttu-id="2f7f9-106">Cada contenedor comprueba los argumentos de entrada, recupera un puntero de adaptador y llama a la función solicitada.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-106">Each wrapper checks the input arguments, retrieves an adapter pointer, and calls the requested function.</span></span> <span data-ttu-id="2f7f9-107">Por ejemplo, el contenedor **WbioEngineSetHashAlgorithm** tiene la siguiente firma.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-107">For example, the **WbioEngineSetHashAlgorithm** wrapper has the following signature.</span></span>


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



<span data-ttu-id="2f7f9-108">La función comprueba que el argumento de *canalización* no es **null**, que existe un adaptador de motor y que existe la función [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) .</span><span class="sxs-lookup"><span data-stu-id="2f7f9-108">The function verifies that the *Pipeline* argument is not **NULL**, that an engine adapter exists, and that the [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) function exists.</span></span> <span data-ttu-id="2f7f9-109">Todas las funciones de contenedor se definen en el \_ archivo de encabezado Adapter. h de Winbio.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-109">All wrapper functions are defined in the Winbio\_adapter.h header file.</span></span> <span data-ttu-id="2f7f9-110">En los temas siguientes se describen los contenedores disponibles.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-110">The following topics discuss the available wrappers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f7f9-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2f7f9-111">In this section</span></span>



| <span data-ttu-id="2f7f9-112">Tema</span><span class="sxs-lookup"><span data-stu-id="2f7f9-112">Topic</span></span>                                                               | <span data-ttu-id="2f7f9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f7f9-113">Description</span></span>                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f7f9-114">Contenedores de adaptadores de motor</span><span class="sxs-lookup"><span data-stu-id="2f7f9-114">Engine Adapter Wrappers</span></span>](engine-adapter-wrappers.md)<br/>   | <span data-ttu-id="2f7f9-115">Funciones que se pueden usar para llamar a funciones en el adaptador de motor.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-115">Functions that you can use to call functions on your engine adapter.</span></span> <span data-ttu-id="2f7f9-116">Estas funciones se definen en Winbio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-116">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="2f7f9-117">Contenedores de adaptador de sensor</span><span class="sxs-lookup"><span data-stu-id="2f7f9-117">Sensor Adapter Wrappers</span></span>](sensor-adapter-wrappers.md)<br/>   | <span data-ttu-id="2f7f9-118">Funciones que se pueden usar para llamar a funciones en el adaptador de sensor.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-118">Functions that you can use to call functions on your sensor adapter.</span></span> <span data-ttu-id="2f7f9-119">Estas funciones se definen en Winbio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-119">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="2f7f9-120">Contenedores del adaptador de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="2f7f9-120">Storage Adapter Wrappers</span></span>](storage-adapter-wrappers.md)<br/> | <span data-ttu-id="2f7f9-121">Funciones que se pueden usar para llamar a funciones en el adaptador de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-121">Functions that you can use to call functions on your storage adapter.</span></span> <span data-ttu-id="2f7f9-122">Estas funciones se definen en Winbio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="2f7f9-122">These functions are defined in Winbio\_adapter.h.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2f7f9-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f7f9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f7f9-124">Referencia del complemento</span><span class="sxs-lookup"><span data-stu-id="2f7f9-124">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> </dl>

 

 





