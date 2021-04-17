---
description: Los informes de presión de memoria permiten a una aplicación de Direct3D determinar si el espacio de trabajo de la memoria de vídeo ha crecido demasiado.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Informes de presión de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677599"
---
# <a name="memory-pressure-reporting"></a><span data-ttu-id="fff02-103">Informes de presión de memoria</span><span class="sxs-lookup"><span data-stu-id="fff02-103">Memory Pressure Reporting</span></span>

<span data-ttu-id="fff02-104">Los informes de presión de memoria permiten a una aplicación de Direct3D determinar si el espacio de trabajo de la memoria de vídeo ha crecido demasiado.</span><span class="sxs-lookup"><span data-stu-id="fff02-104">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span>

<span data-ttu-id="fff02-105">La *presión de memoria* es la demanda que una aplicación coloca en el subsistema de memoria.</span><span class="sxs-lookup"><span data-stu-id="fff02-105">*Memory pressure* is the demand placed on the memory subsystem by an application.</span></span> <span data-ttu-id="fff02-106">Aunque cualquier aplicación de Direct3D puede usar los informes de presión de memoria, esta característica es especialmente útil para las aplicaciones que representan vídeo mediante Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fff02-106">While any Direct3D application can use memory pressure reporting, this feature is especially useful for applications that render video by using Direct3D.</span></span> <span data-ttu-id="fff02-107">La reproducción de vídeo suele beneficiarse de grandes cantidades de almacenamiento en búfer, por lo que los marcos se pueden descodificar de antemano.</span><span class="sxs-lookup"><span data-stu-id="fff02-107">Video playback typically benefits from large amounts of buffering, so that frames can be decoded in advance.</span></span> <span data-ttu-id="fff02-108">Aunque el almacenamiento en búfer suele tener como resultado una reproducción más fluida, realmente puede degradar el rendimiento si el espacio de trabajo aumenta demasiado, debido a los siguientes factores:</span><span class="sxs-lookup"><span data-stu-id="fff02-108">While buffering generally results in smoother playback, it can actually degrade performance if the working set grows too large, due to the following factors:</span></span>

-   <span data-ttu-id="fff02-109">Es posible que la memoria se expulse de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="fff02-109">Memory might be evicted from the cache.</span></span> <span data-ttu-id="fff02-110">En el peor de los casos, esto puede ocurrir en cada fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fff02-110">In the worst case, this can occur on every video frame.</span></span>
-   <span data-ttu-id="fff02-111">Las asignaciones de memoria se pueden colocar en segmentos de memoria no óptimos.</span><span class="sxs-lookup"><span data-stu-id="fff02-111">Memory allocations might be placed in nonoptimal memory segments.</span></span>

<span data-ttu-id="fff02-112">A partir de Windows 7, Direct3D puede informar de algunas estadísticas sobre la presión de memoria de vídeo:</span><span class="sxs-lookup"><span data-stu-id="fff02-112">Starting in Windows 7, Direct3D can report some statistics about the video memory pressure:</span></span>

-   <span data-ttu-id="fff02-113">Número de bytes expulsados por el proceso en un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fff02-113">The number of bytes evicted by the process over an interval of time.</span></span>
-   <span data-ttu-id="fff02-114">Cantidad de memoria colocada en segmentos de memoria no óptimos.</span><span class="sxs-lookup"><span data-stu-id="fff02-114">The amount of memory placed in nonoptimal memory segments.</span></span>
-   <span data-ttu-id="fff02-115">Una indicación aproximada de la eficacia total de las asignaciones de memoria colocadas en memoria no óptima.</span><span class="sxs-lookup"><span data-stu-id="fff02-115">A rough indication of the overall efficiency of the memory allocations placed in nonoptimal memory.</span></span>

<span data-ttu-id="fff02-116">Esta información puede ayudar a una aplicación a mantener un espacio de trabajo razonable.</span><span class="sxs-lookup"><span data-stu-id="fff02-116">This information can help an application to maintain a reasonable working set.</span></span>

## <a name="using-memory-pressure-reporting"></a><span data-ttu-id="fff02-117">Uso de informes de presión de memoria</span><span class="sxs-lookup"><span data-stu-id="fff02-117">Using Memory Pressure Reporting</span></span>

<span data-ttu-id="fff02-118">Los informes de presión de memoria usan la interfaz **IDirect3DQuery9** existente para consultar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fff02-118">Memory pressure reporting uses the existing **IDirect3DQuery9** interface to query the device.</span></span> <span data-ttu-id="fff02-119">Se ha agregado un nuevo tipo de consulta a la enumeración **D3DQUERYTYPE** .</span><span class="sxs-lookup"><span data-stu-id="fff02-119">A new query type has been added to the **D3DQUERYTYPE** enumeration.</span></span>


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



<span data-ttu-id="fff02-120">Para usar esta consulta, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="fff02-120">To use this query, perform the following steps:</span></span>

1.  <span data-ttu-id="fff02-121">Llame a **IDirect3DDevice9Ex:: CreateQuery** con la marca **\_ MEMORYPRESSURE de D3DQUERYTYPE** .</span><span class="sxs-lookup"><span data-stu-id="fff02-121">Call **IDirect3DDevice9Ex::CreateQuery** with the **D3DQUERYTYPE\_MEMORYPRESSURE** flag.</span></span> <span data-ttu-id="fff02-122">Este método devuelve un puntero a la interfaz **IDirect3DQuery9** .</span><span class="sxs-lookup"><span data-stu-id="fff02-122">This method returns a pointer to the **IDirect3DQuery9** interface.</span></span>
2.  <span data-ttu-id="fff02-123">Llame a **IDirect3DQuery9:: Issue** con la marca de **\_ Inicio D3DISSUE** para comenzar el intervalo de medición.</span><span class="sxs-lookup"><span data-stu-id="fff02-123">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_BEGIN** flag to begin the measurement interval.</span></span>
3.  <span data-ttu-id="fff02-124">Llame a **IDirect3DQuery9:: Issue** con la marca de **\_ finalización D3DISSUE** .</span><span class="sxs-lookup"><span data-stu-id="fff02-124">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_END** flag.</span></span>
4.  <span data-ttu-id="fff02-125">Llame a **IDirect3DQuery9:: GetData** para obtener el resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="fff02-125">Call **IDirect3DQuery9::GetData** to get the query result.</span></span> <span data-ttu-id="fff02-126">La consulta devuelve una estructura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="fff02-126">The query returns a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

## <a name="example-code"></a><span data-ttu-id="fff02-127">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="fff02-127">Example Code</span></span>

<span data-ttu-id="fff02-128">En el ejemplo siguiente se muestran dos funciones que miden la presión de memoria.</span><span class="sxs-lookup"><span data-stu-id="fff02-128">The following example shows two functions that measure memory pressure.</span></span> <span data-ttu-id="fff02-129">El primero comienza el intervalo de medición y el segundo recupera los resultados de la medida.</span><span class="sxs-lookup"><span data-stu-id="fff02-129">The first begins the measurement interval, and the second retrieves the results of the measurement.</span></span>


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fff02-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fff02-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fff02-131">API de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="fff02-131">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 



