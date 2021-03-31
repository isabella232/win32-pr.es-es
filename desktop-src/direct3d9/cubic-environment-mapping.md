---
description: 'Mapas de entorno cúbicos: a veces denominados mapas de cubo, son texturas que contienen datos de imagen que representan la escena que rodea un objeto, como si el objeto estuviera en el centro de un cubo.'
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Asignación de entorno cúbica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac83db067224195883485bcbd282aa82ae4b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423479"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Asignación de entorno cúbica (Direct3D 9)

Mapas de entorno cúbicos: a veces denominados mapas de cubo, son texturas que contienen datos de imagen que representan la escena que rodea un objeto, como si el objeto estuviera en el centro de un cubo. Cada cara del mapa del entorno cúbico cubre un campo de vista de 90 grados en horizontal y vertical, y hay seis caras por mapa de cubo. En la ilustración siguiente se muestra la orientación de las caras.

![Ilustración de un cubo con ejes de coordenadas centrales perpendiculares a caras del cubo](images/cubemap-cube.png)

Cada una de las caras del cubo está orientada de forma perpendicular al plano x/y, y/z o x/z, en el espacio universal. En la ilustración siguiente se muestra cómo cada plano corresponde a una esfera.

![Ilustración de caras de cubo con proyecciones de coordenadas de planos](images/cube-faces.png)

Las asignaciones de entorno cúbicas se implementan como una serie de objetos de textura. Las aplicaciones pueden usar imágenes estáticas para la asignación de entorno cúbica, o bien pueden representarse en las caras del mapa de cubo para realizar la asignación dinámica de entorno. Esta técnica requiere que las superficies del mapa de cubo sean superficies de representación-destino válidas, creadas con el \_ indicador D3DUSAGE RENDERTARGET establecido.

No es necesario que las caras de un mapa de cubo contengan representaciones muy detalladas de la escena circundante. En la mayoría de los casos, los mapas de entorno se aplican a las superficies curvas. Dada la cantidad de curvatura usada por la mayoría de las aplicaciones, la distorsión reflectante resultante hace que los detalles extremos en el mapa del entorno desaparezcan en términos de memoria y sobrecarga de representación.

## <a name="mipmapped-cubic-environment-maps"></a>Mipmapped mapas de entorno cúbicos

Los mapas de cubos pueden ser mipmapped. Para crear una asignación de cubo mipmapped, establezca el parámetro Levels del método [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) en el número de niveles que desee. Puede imaginar la topografía de estas superficies tal y como se muestra en el diagrama siguiente.

![diagrama de una asignación de cubo mipmapped con n niveles de MIP](images/cubemap-mipped.png)

Las aplicaciones que crean mapas de entorno cúbicos de mipmapped pueden acceder a cada una de las caras llamando al método [**GetCubeMapSurface**](/windows/desktop/api) . Empiece por establecer el valor adecuado del tipo enumerado [**D3DCUBEMAP \_ Facet**](./d3dcubemap-faces.md) , como se describe en [crear superficies de mapa de entorno cúbica (Direct3D 9)](creating-cubic-environment-map-surfaces.md). A continuación, seleccione el nivel que desea recuperar estableciendo el parámetro de nivel **GetCubeMapSurface** en el nivel de mipmap que desee. Recuerde que 0 corresponde a la imagen de nivel superior.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>Coordenadas de textura para mapas de entorno cúbicos

Las coordenadas de textura que indexan una asignación de entorno cúbica no son coordenadas de estilo u, v simples, tal y como se usan cuando se aplican texturas estándar. De hecho, los mapas de entorno cúbicos no usan coordenadas de textura. En lugar de un conjunto de coordenadas de textura, los mapas de entorno cúbicos requieren un vector 3D. Debe tener cuidado de especificar un formato de vértice adecuado. Además de indicar al sistema Cuántos conjuntos de coordenadas de textura usa la aplicación, debe proporcionar información sobre el número de elementos que hay en cada conjunto. Direct3D ofrece el conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para este propósito. Estas macros aceptan un solo parámetro, identificando el índice del conjunto de coordenadas de textura para el que se describe el tamaño. En el caso de un vector 3D, se incluye el patrón de bits creado por la \_ macro D3DFVF TEXCOORDSIZE3. En el ejemplo de código siguiente se muestra cómo se utiliza esta macro.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



En algunos casos, como la asignación de luz difusa, se usa el vértice del espacio de la cámara normal para el vector. En otros casos, como la asignación del entorno especular, se usa un vector de reflexión. Dado que las normales de vértice transformados se entienden ampliamente, la información aquí se concentra en el cálculo de un vector de reflexión.

Calcular un vector de reflexión por su cuenta requiere comprender la posición de cada vértice y un vector desde el punto de vista hasta ese vértice. Direct3D puede calcular automáticamente los vectores de reflexión para la geometría. El uso de esta característica ahorra memoria porque no es necesario incluir coordenadas de textura para el mapa de entorno. También reduce el ancho de banda y, en el caso de un dispositivo HAL T&L, puede ser mucho más rápido que los cálculos que la aplicación puede realizar por sí mismo. Para usar esta característica, en la fase de textura que contiene la asignación de entorno cúbica, establezca el estado de la fase de D3DTSS \_ TEXCOORDINDEX Texture en una combinación del \_ miembro D3DTSS TCI \_ CAMERASPACEREFLECTIONVECTOR de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) y el índice de un conjunto de coordenadas de textura. En algunas situaciones, como la asignación de luz difusa, podría usar el \_ miembro D3DTSS TCI \_ CAMERASPACENORMAL de **D3DTEXTURESTAGESTATETYPE**, que hace que el sistema use el vértice transformado, el espacio de la cámara, el vértice normal como el vector de direccionamiento de la textura. El sistema solo usa el índice para determinar el modo de ajuste de la textura.

En el ejemplo de código siguiente se muestra cómo se usa este valor.


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



Al habilitar la generación automática de coordenadas de textura, el sistema utiliza una de las dos fórmulas para calcular el vector de reflexión para cada vértice. Cuando el estado de representación de D3DRS \_ LOCALVIEWER se establece en **true**, se utiliza la fórmula siguiente.

![fórmula del vector de reflexión (r = 2 (EXN () n-e)](images/reflection-vector-local.png)

En la fórmula anterior, R es el vector de reflexión que se está calculando, E es el vector de posición a ojo normalizado y N es el vértice de espacio de la cámara normal.

Cuando el estado de representación de D3DRS \_ LOCALVIEWER se establece en **false**, el sistema utiliza la siguiente fórmula.

![fórmula del vector de reflexión (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Los elementos R y N de esta fórmula son idénticos a los de la fórmula anterior. El elemento N<sub>z</sub> es el Z de espacio mundial del vértice normal y I es el vector (0, 0, 1) de un punto de vista infinitamente distante. El sistema utiliza el vector de reflexión de cualquier fórmula para seleccionar y abordar la superficie adecuada del mapa de cubo.

> [!Note]  
> En la mayoría de los casos, las aplicaciones deben habilitar la normalización automática de las normales de vértices. Para ello, establezca D3DRS \_ NORMALIZENORMALS en **true**. Si no habilita este estado de representación, la apariencia del mapa de entorno será drásticamente diferente de lo que cabría esperar.

 

En el tema siguiente se incluye información adicional.

-   [Crear superficies de mapa de entorno cúbica (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de entorno](environment-mapping.md)
</dt> </dl>

 

 
