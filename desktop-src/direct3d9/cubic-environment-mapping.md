---
description: Los mapas de entornos cúbicas ,a veces denominados mapas de cubos, son texturas que contienen datos de imagen que representan la escena que rodea a un objeto, como si el objeto estuviera en el centro de un cubo.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Asignación de entorno cúbica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b02f86528c52c2e8e9376eb92e4452735c2613cc9b7dda08a8a07e8473193ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565344"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Asignación de entorno cúbica (Direct3D 9)

Los mapas de entornos cúbicas ,a veces denominados mapas de cubos, son texturas que contienen datos de imagen que representan la escena que rodea a un objeto, como si el objeto estuviera en el centro de un cubo. Cada cara del mapa de entorno cúbica cubre un campo de vista de 90 grados en horizontal y vertical, y hay seis caras por mapa de cubo. La orientación de las caras se muestra en la ilustración siguiente.

![ilustración de un cubo con ejes de coordenadas centrales para caras de cubo](images/cubemap-cube.png)

Cada cara del cubo está orientada al plano x/y, y/z o x/z, en el espacio del mundo. En la ilustración siguiente se muestra cómo se corresponde cada plano con una cara.

![ilustración de caras de cubo con proyecciones de coordenadas desde planos](images/cube-faces.png)

Los mapas de entornos cúbicas se implementan como una serie de objetos de textura. Las aplicaciones pueden usar imágenes estáticas para la asignación de entornos cúbicas o se pueden representar en las caras del mapa de cubo para realizar la asignación dinámica del entorno. Esta técnica requiere que las superficies de mapa de cubo sean superficies de destino de representación válidas, creadas con la marca RENDERTARGET de D3DUSAGE \_ establecida.

Las caras de un mapa de cubo no necesitan contener representaciones extremadamente detalladas de la escena circundante. En la mayoría de los casos, los mapas de entorno se aplican a superficies curvas. Dada la cantidad de curvación usada por la mayoría de las aplicaciones, la distorsión reflectante resultante hace que los detalles extremos del mapa de entorno se desperdifien en términos de memoria y sobrecarga de representación.

## <a name="mipmapped-cubic-environment-maps"></a>Mipmapped Cubic Environment Mapas

Los mapas de cubos pueden ser mipmapped. Para crear un mapa de cubo mipmapped, establezca el parámetro Levels del [**método CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) en el número de niveles que desee. Puede imaginar la topografía de estas superficies como se muestra en el diagrama siguiente.

![diagrama de un mapa de cubo mipmapped con n niveles de mip](images/cubemap-mipped.png)

Las aplicaciones que crean mapas de entornos cúbicas mipmapped pueden acceder a cada cara mediante una llamada al [**método GetCubeMapSurface.**](/windows/desktop/api) Empiece estableciendo el valor adecuado del tipo enumerado [**D3DCUBEMAP \_ FACES,**](./d3dcubemap-faces.md) como se describe en Creación de superficies de mapa de entorno [cúbica (Direct3D 9).](creating-cubic-environment-map-surfaces.md) A continuación, seleccione el nivel que desea recuperar estableciendo el parámetro de nivel **GetCubeMapSurface** en el nivel de mapa mip que desee. Recuerde que 0 se corresponde con la imagen de nivel superior.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>Coordenadas de textura para el entorno cúbica Mapas

Las coordenadas de textura que indexa un mapa de entorno cúbica no son coordenadas de estilo u, v simples, como se usa cuando se aplican texturas estándar. De hecho, los mapas de entornos cúbicas no usan coordenadas de textura. En lugar de un conjunto de coordenadas de textura, los mapas de entornos cúbicas requieren un vector 3D. Debe tener cuidado de especificar un formato de vértice adecuado. Además de decir al sistema cuántos conjuntos de coordenadas de textura usa la aplicación, debe proporcionar información sobre cuántos elementos hay en cada conjunto. Direct3D ofrece el conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para este propósito. Estas macros aceptan un único parámetro, que identifica el índice del conjunto de coordenadas de textura para el que se describe el tamaño. En el caso de un vector 3D, se incluye el patrón de bits creado por la macro D3DFVF \_ TEXCOORDSIZE3. En el ejemplo de código siguiente se muestra cómo se usa esta macro.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



En algunos casos, como la asignación de luz difusa, se usa el vértice de espacio de cámara normal para el vector. En otros casos, como la asignación de entorno especular, se usa un vector de reflexión. Dado que las normales de vértice transformadas se entienden ampliamente, la información aquí se centra en calcular un vector de reflexión.

La computación de un vector de reflexión por su cuenta requiere comprender la posición de cada vértice y de un vector desde el punto de vista hasta ese vértice. Direct3D puede calcular automáticamente los vectores de reflexión de la geometría. El uso de esta característica ahorra memoria porque no es necesario incluir coordenadas de textura para el mapa de entorno. También reduce el ancho de banda y, en el caso de un dispositivo T&L LOL, puede ser significativamente más rápido que los cálculos que la aplicación puede realizar por sí sola. Para usar esta característica, en la fase de textura que contiene el mapa de entorno cúbica, establezca el estado de la fase de textura D3DTSS TEXCOORDINDEX en una combinación del miembro \_ \_ TCI \_ CAMERASPACEREFLECTIONVECTOR de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) y el índice de un conjunto de coordenadas de textura. En algunas situaciones, como la asignación de luz difusa, puede usar el miembro \_ \_ CAMERASPACENORMAL de **D3DTEXTURESTAGESTATETYPE** de D3DTSS, lo que hace que el sistema use el vértice normal transformado, espacio de cámara y como vector de direccionamiento de la textura. El sistema solo usa el índice para determinar el modo de ajuste de la textura.

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



Al habilitar la generación automática de coordenadas de textura, el sistema usa una de las dos fórmulas para calcular el vector de reflexión para cada vértice. Cuando el estado de representación de LOCALVIEWER de D3DRS \_ se establece en **TRUE,** se usa la fórmula siguiente.

![fórmula del vector de reflexión (r = 2(exn)n-e)](images/reflection-vector-local.png)

En la fórmula anterior, R es el vector de reflexión que se está calculando, E es el vector de posición a ojo normalizado y N es el vértice del espacio de la cámara normal.

Cuando el estado de representación de LOCALVIEWER de D3DRS \_ se establece en **FALSE,** el sistema usa la siguiente fórmula.

![fórmula del vector de reflexión (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Los elementos R y N de esta fórmula son idénticos a la fórmula anterior. El elemento N<sub>Z</sub> es el espacio mundial z del vértice normal, y yo es el vector (0,0,1) de un punto de vista infinitamente lejano. El sistema usa el vector de reflexión de cualquiera de las fórmulas para seleccionar y dirigir la cara adecuada del mapa del cubo.

> [!Note]  
> En la mayoría de los casos, las aplicaciones deben habilitar la normalización automática de los normales de vértice. Para ello, establezca D3DRS \_ NORMALIZENORMALS en **TRUE.** Si no habilita este estado de representación, la apariencia del mapa de entorno será drásticamente diferente de la esperada.

 

En el tema siguiente se incluye información adicional.

-   [Creación de superficies de mapa de entorno cúbica (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de entorno](environment-mapping.md)
</dt> </dl>

 

 
