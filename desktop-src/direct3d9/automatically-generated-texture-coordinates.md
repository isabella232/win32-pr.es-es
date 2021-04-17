---
title: Coordenadas de textura generadas automáticamente (Direct3D 9)
description: El sistema puede utilizar la posición de espacio de la cámara transformada o la normal de un vértice como coordenadas de textura, o puede calcular los tres vectores de elemento que se usan para dirigirse a un mapa de entorno cúbico.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705351"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>Coordenadas de textura generadas automáticamente (Direct3D 9)

El sistema puede utilizar la posición de espacio de la cámara transformada o la normal de un vértice como coordenadas de textura, o puede calcular los tres vectores de elemento que se usan para dirigirse a un mapa de entorno cúbico. Al igual que las coordenadas de textura que se especifican explícitamente en un vértice, se pueden utilizar coordenadas de textura generadas automáticamente como entrada para las transformaciones de coordenadas de textura.

Las coordenadas de textura generadas automáticamente pueden reducir significativamente el ancho de banda necesario para los datos de geometría eliminando la necesidad de coordenadas de textura explícitas en el formato de vértices. En muchos casos, las coordenadas de textura que genera el sistema se pueden utilizar con transformaciones para producir efectos especiales. Por supuesto, se trata de una característica especial y usará coordenadas de textura explícitas para muchas ocasiones.

## <a name="configuring-automatically-generated-texture-coordinates"></a>Configurar coordenadas de textura generadas automáticamente

En C++, el \_ Estado D3DTSS TEXCOORDINDEX Texture-Stage (del tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) ) controla cómo el sistema genera coordenadas de textura.

Normalmente, este estado indica al sistema que use un conjunto determinado de coordenadas de textura codificadas en el formato de vértice. Al incluir las marcas D3DTSS \_ TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION o D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR en el valor que se asigna a este estado, el comportamiento del sistema es bastante diferente. Si cualquiera de estas marcas está presente, la fase de textura omite las coordenadas de textura en el formato de vértice en favor de las coordenadas que genera el sistema. Los significados de cada marca se muestran en la lista siguiente.

-   D3DTSS \_ TCI \_ CAMERASPACENORMAL

    Use el vértice normal, transformado en el espacio de la cámara, como coordenadas de textura de entrada.

-   D3DTSS \_ TCI \_ CAMERASPACEPOSITION

    Use la posición del vértice, transformada en el espacio de la cámara, como coordenadas de textura de entrada.

-   D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR

    Use el vector de reflexión, transformado en el espacio de la cámara, como coordenadas de textura de entrada. El vector de reflexión se calcula a partir de la posición del vértice de entrada y del vector normal.

Las marcas de índice de coordenadas de textura son mutuamente excluyentes. En este ejemplo se usa:

-   Posición del vértice (en el espacio de la cámara) como coordenadas de textura de entrada para esta fase de textura.
-   El modo de ajuste establecido en el \_ Estado de representación de D3DRENDERSTATE WRAP1


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



Las coordenadas de textura generadas automáticamente son más útiles como valores de entrada para una transformación de coordenadas de textura o para eliminar la necesidad de que la aplicación calcule vectores de tres elementos para las asignaciones de entorno cúbica.

La asignación de esferas usa un mapa de textura precalculado (en tiempo de modelo) que contiene todo el entorno tal y como se refleja en una esfera de Chrome. Direct3D tiene una característica de generación de coordenadas de textura que usa el estado de representación D3DTSS \_ TCI \_ CAMERASPACENORMAL, que toma el normal del vértice en el espacio de la cámara y lo coloca a través de una transformación de textura para generar coordenadas de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesamiento de coordenadas de textura](texture-coordinate-processing.md)
</dt> <dt>

[Transformaciones de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md)
</dt> <dt>

[Asignación de entorno cúbica (Direct3D 9)](cubic-environment-mapping.md)
</dt> </dl>

 

 
