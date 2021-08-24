---
description: Los informes de presión de memoria permiten a una aplicación Direct3D determinar cuándo su espacio de trabajo de memoria de vídeo ha aumentado demasiado.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Informes de presión de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dc0df8db30281c6f7225309bdca5edfdbd3759f21a9e61cdc848f534dcce41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723775"
---
# <a name="memory-pressure-reporting"></a>Informes de presión de memoria

Los informes de presión de memoria permiten a una aplicación Direct3D determinar cuándo su espacio de trabajo de memoria de vídeo ha aumentado demasiado.

*La presión de* memoria es la demanda que una aplicación aplica al subsistema de memoria. Aunque cualquier aplicación de Direct3D puede usar informes de presión de memoria, esta característica es especialmente útil para las aplicaciones que representan vídeo mediante Direct3D. Normalmente, la reproducción de vídeo se beneficia de grandes cantidades de almacenamiento en búfer, por lo que los fotogramas se pueden descodificar de antemano. Aunque el almacenamiento en búfer suele dar lugar a una reproducción más fluida, en realidad puede degradar el rendimiento si el espacio de trabajo crece demasiado, debido a los siguientes factores:

-   La memoria podría expulsarse de la memoria caché. En el peor de los casos, esto puede ocurrir en cada fotograma de vídeo.
-   Las asignaciones de memoria se pueden colocar en segmentos de memoria no no eficientes.

A partir Windows 7, Direct3D puede notificar algunas estadísticas sobre la presión de memoria de vídeo:

-   Número de bytes expulsados por el proceso durante un intervalo de tiempo.
-   Cantidad de memoria colocada en segmentos de memoria nopópticos.
-   Una indicación aproximada de la eficacia general de las asignaciones de memoria colocadas en memoria no óptima.

Esta información puede ayudar a una aplicación a mantener un conjunto de trabajo razonable.

## <a name="using-memory-pressure-reporting"></a>Uso de informes de presión de memoria

Los informes de presión de memoria usan la interfaz **IDirect3DQuery9** existente para consultar el dispositivo. Se ha agregado un nuevo tipo de consulta a la **enumeración D3DQUERYTYPE.**


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Para usar esta consulta, realice los pasos siguientes:

1.  Llame **a IDirect3DDevice9Ex::CreateQuery con** la marca **\_ MEMORYPRESSURE D3DQUERYTYPE.** Este método devuelve un puntero a la **interfaz IDirect3DQuery9.**
2.  Llame **a IDirect3DQuery9::Issue** con la **marca \_ BEGIN de D3DISSUE** para comenzar el intervalo de medición.
3.  Llame **a IDirect3DQuery9::Issue** con la **marca END D3DISSUE. \_**
4.  Llame **a IDirect3DQuery9::GetData** para obtener el resultado de la consulta. La consulta devuelve una [**estructura D3DMEMORYPRESSURE.**](d3dmemorypressure.md)

## <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se muestran dos funciones que miden la presión de memoria. La primera comienza el intervalo de medida y la segunda recupera los resultados de la medida.


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

 

 



