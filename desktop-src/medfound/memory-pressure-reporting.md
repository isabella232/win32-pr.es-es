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
# <a name="memory-pressure-reporting"></a>Informes de presión de memoria

Los informes de presión de memoria permiten a una aplicación de Direct3D determinar si el espacio de trabajo de la memoria de vídeo ha crecido demasiado.

La *presión de memoria* es la demanda que una aplicación coloca en el subsistema de memoria. Aunque cualquier aplicación de Direct3D puede usar los informes de presión de memoria, esta característica es especialmente útil para las aplicaciones que representan vídeo mediante Direct3D. La reproducción de vídeo suele beneficiarse de grandes cantidades de almacenamiento en búfer, por lo que los marcos se pueden descodificar de antemano. Aunque el almacenamiento en búfer suele tener como resultado una reproducción más fluida, realmente puede degradar el rendimiento si el espacio de trabajo aumenta demasiado, debido a los siguientes factores:

-   Es posible que la memoria se expulse de la memoria caché. En el peor de los casos, esto puede ocurrir en cada fotograma de vídeo.
-   Las asignaciones de memoria se pueden colocar en segmentos de memoria no óptimos.

A partir de Windows 7, Direct3D puede informar de algunas estadísticas sobre la presión de memoria de vídeo:

-   Número de bytes expulsados por el proceso en un intervalo de tiempo.
-   Cantidad de memoria colocada en segmentos de memoria no óptimos.
-   Una indicación aproximada de la eficacia total de las asignaciones de memoria colocadas en memoria no óptima.

Esta información puede ayudar a una aplicación a mantener un espacio de trabajo razonable.

## <a name="using-memory-pressure-reporting"></a>Uso de informes de presión de memoria

Los informes de presión de memoria usan la interfaz **IDirect3DQuery9** existente para consultar el dispositivo. Se ha agregado un nuevo tipo de consulta a la enumeración **D3DQUERYTYPE** .


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Para usar esta consulta, siga estos pasos:

1.  Llame a **IDirect3DDevice9Ex:: CreateQuery** con la marca **\_ MEMORYPRESSURE de D3DQUERYTYPE** . Este método devuelve un puntero a la interfaz **IDirect3DQuery9** .
2.  Llame a **IDirect3DQuery9:: Issue** con la marca de **\_ Inicio D3DISSUE** para comenzar el intervalo de medición.
3.  Llame a **IDirect3DQuery9:: Issue** con la marca de **\_ finalización D3DISSUE** .
4.  Llame a **IDirect3DQuery9:: GetData** para obtener el resultado de la consulta. La consulta devuelve una estructura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .

## <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se muestran dos funciones que miden la presión de memoria. El primero comienza el intervalo de medición y el segundo recupera los resultados de la medida.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 



