---
description: La interfaz ID3DXPRTEngine se usa para calcular una simulación de transferencia de Radiance precalculada (PRT). Normalmente, los métodos se usan sin conexión para calcular los vectores de transferencia por vértices o por textura en tiempo real del modelado 3D en tiempo real.
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: Interfaz ID3DXPRTEngine (D3DX9Mesh. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717697"
---
# <a name="id3dxprtengine-interface"></a>Interfaz ID3DXPRTEngine

La interfaz ID3DXPRTEngine se usa para calcular una simulación de transferencia de Radiance precalculada (PRT). Normalmente, los métodos se usan sin conexión para calcular los vectores de transferencia por vértices o por textura en tiempo real del modelado 3D en tiempo real.

## <a name="members"></a>Miembros

La interfaz **ID3DXPRTEngine** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTEngine** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXPRTEngine** tiene estos métodos.



| Método                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)                       | Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla. Si se encuentra una intersección, el método devuelve el índice de la superficie de malla más cercana que el rayo y las coordenadas Barycentric del punto de intersección.<br/>                                                                                                                                                                                |
| [**ComputeBounce**](id3dxprtengine--computebounce.md)                                     | Calcula el Radiance de origen resultante de un único rebote de luz interreflejada. Este método se puede usar para cualquier escena iluminada, incluido un modelo Radiance (PRT) precalculado basado en armónico (SH).<br/>                                                                                                                                                                                                                                                    |
| [**ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)                     | Calcula el Radiance de origen resultante de un único rebote de luz interreflejada mediante el muestreo adaptable. Este método genera nuevos vértices y caras en la malla para aproximar con más precisión la señal de transferencia Radiance (PRT) precalculada. Este método se puede usar para cualquier escena iluminada, incluido un modelo PRT basado en armónico (SH).<br/>                                                                                                                   |
| [**ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)                 | Calcula la contribución de iluminación directa a objetos 3D donde el Radiance de origen se representa mediante una aproximación de armónico (SH) esférica.<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | Calcula la contribución de iluminación directa a objetos 3D en los que el Radiance de origen se representa mediante una aproximación de armónico (SH) esférico, mediante el muestreo adaptable. Este método genera nuevos vértices y caras en la malla para aproximar con más precisión la señal de transferencia Radiance (PRT) precalculada.<br/>                                                                                                                                                           |
| [**ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)           | Usa la GPU para calcular la contribución de iluminación directa a objetos 3D donde el Radiance de origen se representa mediante una aproximación de armónico (SH) esférica. Calcular la iluminación en la GPU generalmente será mucho más rápido que en la CPU.<br/>                                                                                                                                                                                                                            |
| [**ComputeLDPRTCoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | Calcula los coeficientes de transferencia de Radiance precalculados (LDPRT) precalculados de forma local en relación con los vectores normales de cada muestra para minimizar el error de menos cuadrados con respecto a los datos de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada. Estos coeficientes se pueden usar con vectores normales con o sin máscaras para modelar los efectos globales en los objetos dinámicos.<br/>                                                                                                                     |
| [**No es un proceso**](id3dxprtengine--computess.md)                                             | Calcula el Radiance de origen resultante de la dispersión de subsuperficies, mediante las propiedades de material establecidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). Este método solo se puede usar para los materiales definidos por vértice en un objeto Mesh.<br/>                                                                                                                                                                                                       |
| [**ComputeSSAdaptive**](id3dxprtengine--computessadaptive.md)                             | Calcula un vector de transferencia que asigna Radiance de origen para salir de Radiance resultante de la dispersión de subsuperficies, mediante el muestreo adaptable y las propiedades de material establecidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). El método genera nuevos vértices y caras en la malla para aproximar con más precisión la señal de transferencia Radiance (PRT) precalculada. Este método solo se puede usar para los materiales definidos por vértice en un objeto Mesh.<br/> |
| [**ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)               | Calcula muestras de transferencia Radiance (PRT) precalculadas para un punto arbitrario (y un vector normal).<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)           | Calcula, en un punto arbitrario que no está en una malla, un vector de transferencia que asigna Radiance de origen (representado mediante una aproximación de armónico (SH)) para salir de radiance.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)                       | Calcula una proyección de la iluminación directa desde el rebote de luz anterior en vectores de base de armónicos esféricos (SH) que representan el incidente radiance en las ubicaciones especificadas.<br/>                                                                                                                                                                                                                                                                                         |
| [**ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)       | Calcula una proyección de iluminación distanl en vectores de base de armónicos esféricos (SH) que representan el incidente radiance en las ubicaciones especificadas.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ExtractPerVertexAlbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | Copia los valores de Albedo por vértice de una malla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**FreeBounceData**](id3dxprtengine--freebouncedata.md)                                   | Libera la memoria usada para los datos de simulación de luz rebotada temporal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**FreeSSData**](id3dxprtengine--freessdata.md)                                           | Libera la memoria usada para los datos de simulación de dispersión de la luz de subsuperficie temporal.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**GetAdaptedMesh**](id3dxprtengine--getadaptedmesh.md)                                   | Devuelve una malla con modificaciones resultantes del muestreo espacial adaptable. La malla devuelta solo contiene posiciones, normales y coordenadas de textura (si se definen).<br/>                                                                                                                                                                                                                                                                                                   |
| [**GetNumFaces**](id3dxprtengine--getnumfaces.md)                                         | Recupera el número de caras de la malla, incluidas las nuevas caras agregadas como resultado de un muestreo espacial adaptable.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetNumVerts**](id3dxprtengine--getnumverts.md)                                         | Recupera el número de vértices de la malla, incluido cualquier vértice nuevo agregado como resultado de un muestreo espacial adaptable.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetVertexAlbedo**](id3dxprtengine--getvertexalbedo.md)                                 | Recupera los valores de albedo de los vértices de malla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md)                                   | Multiplica cada vector de transferencia Radiance (PRT) precalculado por el albedo por vértice.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ResampleBuffer**](id3dxprtengine--resamplebuffer.md)                                   | Remuestrea un búfer de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada y lo guarda en un búfer de salida. Este método se puede usar para convertir un búfer de vértice en un búfer de textura y viceversa. También se puede usar para convertir búferes de canal único en búferes de 3 canales y viceversa.<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | Divide caras en una malla, lo que permite un muestreo adaptativo conservador que no eliminará características en la malla.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**ScaleMeshChunk**](id3dxprtengine--scalemeshchunk.md)                                   | Escala todos los ejemplos asociados a una submalla determinada. El método es útil para calcular la dispersión de subsuperficies.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetCallBack**](id3dxprtengine--setcallback.md)                                         | Establece un puntero a una función de devolución de llamada opcional que calcula el porcentaje de cálculos armónicos esférico (SH) completado y proporciona al llamador la opción de anular el simulador.<br/>                                                                                                                                                                                                                                                                               |
| [**SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)                               | Establece las propiedades de material de la malla en la escena 3D. Use este método para especificar parámetros de dispersión de subsuperficie.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)                     | Establece las distancias mínima y máxima de intersección entre los objetos 3D. Estos valores de distancia se pueden usar para controlar la distancia mínima o máxima con la que los objetos pueden sombrear o reflejar la luz. Por ejemplo, el método se puede utilizar para limitar el sombreado de las características cercanas de un modelo 3D.<br/>                                                                                                                                                                          |
| [**SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md)                             | Establece un valor de Albedo para cada textura, sobrescribiendo los valores de Albedo anteriores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**SetPerTexelNormal**](id3dxprtengine--setpertexelnormal.md)                             | Establece un vector normal para cada textura de un objeto Texture. Este método se usa para almacenar vectores normales de vértices de una malla (o normales de vértice interpolados si se está calculando la transferencia de Radiance precalculada basada en píxeles).<br/>                                                                                                                                                                                                                                          |
| [**SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)                           | Establece un valor de Albedo para cada vértice de la malla, sobrescribiendo los valores de Albedo anteriores.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)                                 | Establece las propiedades de muestreo utilizadas por el simulador Radiance Transfer (PRT) precalculado.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)                         | Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla. Normalmente se usa para determinar si un punto determinado está en sombra.<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

Para convertir los valores de RGB a luminancia, se usa la fórmula siguiente:


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



La interfaz **ID3DXPRTEngine** se obtiene mediante una llamada a la función [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) .

El tipo LPD3DXPRTENGINE se define como un puntero a la interfaz **ID3DXPRTEngine** .


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[Transferencia Radiance precalculada (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
