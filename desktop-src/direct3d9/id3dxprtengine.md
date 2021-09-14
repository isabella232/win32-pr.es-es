---
description: La interfaz ID3DXPRTEngine se usa para calcular una simulación de transferencia de base de datos precalutada (PRT). Sus métodos se usan normalmente sin conexión para calcular vectores de transferencia por vértice o por texel antes del modelado 3D en tiempo real.
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: Interfaz ID3DXPRTEngine (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5507a79a60b2ffcb3cf801ea0454c7306bcde056
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974762"
---
# <a name="id3dxprtengine-interface"></a>Interfaz ID3DXPRTEngine

La interfaz ID3DXPRTEngine se usa para calcular una simulación de transferencia de base de datos precalutada (PRT). Sus métodos se usan normalmente sin conexión para calcular vectores de transferencia por vértice o por texel antes del modelado 3D en tiempo real.

## <a name="members"></a>Members

La **interfaz ID3DXPRTEngine** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTEngine** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXPRTEngine** tiene estos métodos.



| Método                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)                       | Usa un seguimiento eficaz de rayos en simulaciones de transferencia de radiancia precalutadas (PRT) para determinar si un rayo forma una intersección con una malla. Si se encuentra una intersección, el método devuelve el índice de la cara de malla más cercana alcanzado por el rayo y las coordenadas baricéntricas del punto de intersección.<br/>                                                                                                                                                                                |
| [**ComputeBounce**](id3dxprtengine--computebounce.md)                                     | Calcula el brillo de origen resultante de un único salto de luz interreferida. Este método se puede usar para cualquier escena de iluminación, incluido un modelo de transferencia de radiancia precalutada (PRT) basado en sh(sh).<br/>                                                                                                                                                                                                                                                    |
| [**ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)                     | Calcula el brillo de origen resultante de un único salto de luz interreferida, mediante el muestreo adaptable. Este método genera nuevos vértices y caras en la malla para aproximar de forma más precisa la señal de transferencia de radiancia precalutada (PRT). Este método se puede usar para cualquier escena de iluminación, incluido un modelo PRT basado en armónica esférica (SH).<br/>                                                                                                                   |
| [**ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)                 | Calcula la contribución de iluminación directa a objetos 3D donde el sonido de origen se representa mediante una aproximación esférica (SH).<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | Calcula la contribución de iluminación directa a los objetos 3D donde el sonido de origen se representa mediante una aproximación esférica (SH), mediante muestreo adaptable. Este método genera nuevos vértices y caras en la malla para aproximar de forma más precisa la señal de transferencia de radiancia precalutada (PRT).<br/>                                                                                                                                                           |
| [**ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)           | Usa la GPU para calcular la contribución de iluminación directa a objetos 3D en los que el sonido de origen se representa mediante una aproximación esférica (SH). La computación de la iluminación en la GPU suele ser mucho más rápida que en la CPU.<br/>                                                                                                                                                                                                                            |
| [**ComputeLDPRTCoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | Calcula los coeficientes de transferencia de base precalutada (LDPRT) que se pueden calcular localmente en relación con los vectores normales por muestra para minimizar el error de mínimos cuadrados con respecto a los datos [**id3DXPRTBuffer**](id3dxprtbuffer.md) de entrada. Estos coeficientes se pueden usar con vectores normales de máscara o transformados para modelar efectos globales en objetos dinámicos.<br/>                                                                                                                     |
| [**ComputeSS**](id3dxprtengine--computess.md)                                             | Calcula el brillo de origen resultante de la dispersión de subsuelo, utilizando las propiedades de material establecidas [**por ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). Este método solo se puede usar para materiales definidos por vértice en un objeto de malla.<br/>                                                                                                                                                                                                       |
| [**ComputeSSAdaptive**](id3dxprtengine--computessadaptive.md)                             | Calcula un vector de transferencia que asigna el brillo de origen para salir de la luminosidad resultante de la dispersión de subsuelo, mediante el muestreo adaptable y las propiedades de material establecidas por [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). El método genera nuevos vértices y caras en la malla para aproximar con más precisión la señal de transferencia de radiancia precalcida (PRT). Este método solo se puede usar para materiales definidos por vértice en un objeto de malla.<br/> |
| [**ComputeSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)               | Calcula muestras de transferencia de radiancia precalutadas (PRT) para un punto arbitrario (y vector normal).<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**ComputeSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)           | Calcula, en un punto arbitrario que no está en una malla, un vector de transferencia que asigna la radiancia de origen (representada por una aproximación de armónica esférica (SH) para salir de la luminosidad.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)                       | Calcula una proyección de la iluminación directa a partir de los vectores de base de la iluminación anterior en vectores de base esférica (SH) que representan el brillo de los incidentes en ubicaciones especificadas.<br/>                                                                                                                                                                                                                                                                                         |
| [**ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)       | Calcula una proyección de iluminación lejana en vectores de base armónicos esféricos (SH) que representan el brillo de los incidentes en ubicaciones especificadas.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ExtractPerVertexAlbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | Copia los valores de albedo por vértice de una malla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**FreeBounceData**](id3dxprtengine--freebouncedata.md)                                   | Libera la memoria usada para los datos temporales de simulación de luz desboda.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**FreeSSData**](id3dxprtengine--freessdata.md)                                           | Libera la memoria usada para los datos temporales de simulación de dispersión de luz de subsuelo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**GetAdaptedMesh**](id3dxprtengine--getadaptedmesh.md)                                   | Devuelve una malla con modificaciones resultantes del muestreo espacial adaptable. La malla devuelta solo contiene posiciones, normales y coordenadas de textura (si se definen).<br/>                                                                                                                                                                                                                                                                                                   |
| [**GetNumFaces**](id3dxprtengine--getnumfaces.md)                                         | Recupera el número de caras de la malla, incluidas las caras nuevas agregadas como resultado del muestreo espacial adaptable.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetNumVerts**](id3dxprtengine--getnumverts.md)                                         | Recupera el número de vértices de la malla, incluidos los nuevos vértices agregados como resultado del muestreo espacial adaptable.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetVertexAlbedo**](id3dxprtengine--getvertexalbedo.md)                                 | Recupera los valores albedo de los vértices de malla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md)                                   | Multiplica cada vector de transferencia de radiancia precalutada (PRT) por el albedo por vértice.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ResampleBuffer**](id3dxprtengine--resamplebuffer.md)                                   | Vuelve a muestrear un búfer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada y lo guarda en un búfer de salida. Este método se puede usar para convertir un búfer de vértices en un búfer de textura y viceversa. También se puede usar para convertir búferes de canal único en búferes de 3 canales y viceversa.<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | Subdivide caras en una malla, lo que permite un muestreo adaptable conservador que no eliminará las características de la malla.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**ScaleMeshChunk**](id3dxprtengine--scalemeshchunk.md)                                   | Escala todos los ejemplos asociados a un submesh determinado. El método es útil para calcular la dispersión de subsuelo.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetCallBack**](id3dxprtengine--setcallback.md)                                         | Establece un puntero a una función de devolución de llamada opcional que calcula el porcentaje de cálculos esféricos (SH) completados y ofrece al autor de la llamada la opción de anular el simulador.<br/>                                                                                                                                                                                                                                                                               |
| [**SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)                               | Establece las propiedades de material de malla en la escena 3D. Use este método para especificar parámetros de dispersión de subsuelo.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)                     | Establece las distancias mínima y máxima de intersección entre objetos 3D. Estos valores de distancia se pueden usar para controlar la distancia mínima o máxima que los objetos pueden sombrar o reflejar la luz. Por ejemplo, el método se puede usar para limitar el sombreado de las características cercanas de un modelo 3D.<br/>                                                                                                                                                                          |
| [**SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md)                             | Establece un valor albedo para cada texel, sobrescribiendo los valores anteriores de albedo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**SetPerTexelNormal**](id3dxprtengine--setpertexelnormal.md)                             | Establece un vector normal para cada elemento de textura de un objeto de textura. Este método se usa para almacenar vectores normales de vértice desde una malla (o normales de vértice interpolado si se está calculando la transferencia de radiancia precalentada (PRT) basada en píxeles).<br/>                                                                                                                                                                                                                                          |
| [**SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)                           | Establece un valor albedo para cada vértice de malla, sobrescribiendo los valores anteriores de albedo.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)                                 | Establece las propiedades de muestreo usadas por el simulador de transferencia de base de datos precalutada (PRT).<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)                         | Usa un seguimiento eficaz de rayos en simulaciones de transferencia de radiancia precalutadas (PRT) para determinar si un rayo forma una intersección con una malla. Normalmente se usa para determinar si un punto determinado está en la sombra.<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

Para convertir valores RGB a luminance, se usa la fórmula siguiente:


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



La **interfaz ID3DXPRTEngine** se obtiene llamando a la función [**D3DXCreatePRTEngine.**](d3dxcreateprtengine.md)

El tipo LPD3DXPRTENGINE se define como un puntero a la **interfaz ID3DXPRTEngine.**


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[Transferencia de radiancia precalcalada (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
