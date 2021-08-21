---
description: Puede pensar que la transformación de proyección controla el interior de la cámara. es análogo a elegir una lente para la cámara.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Transformación de proyección (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad15ee0f4d23401563a9a51b8767be3da6e47dfee9dc76d580154ef1d524d02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092727"
---
# <a name="projection-transform-direct3d-9"></a>Transformación de proyección (Direct3D 9)

Puede pensar que la transformación de proyección controla el interior de la cámara. es análogo a elegir una lente para la cámara. Este es el más complicado de los tres tipos de transformación. Esta explicación de la transformación de proyección se organiza en los temas siguientes.

La matriz de proyección suele ser una proyección de escala y perspectiva. La transformación de proyección convierte el frustum de visualización en una forma cuboid. Dado que el extremo cercano del frustum de visualización es menor que el extremo lejano, esto tiene el efecto de expandir objetos que están cerca de la cámara. así es cómo se aplica la perspectiva a la escena.

En [la frustum](viewports-and-clipping.md)de visualización, la distancia entre la cámara y el origen del espacio de transformación de visualización se define arbitrariamente como D, por lo que la matriz de proyección tiene un aspecto similar al de la ilustración siguiente.

![ilustración de la matriz de proyección](images/projmat1.png)

La matriz de visualización traduce la cámara al origen mediante la traducción en la dirección z por - D. La matriz de traducción es como la ilustración siguiente.

![ilustración de la matriz de traducción](images/projmat2.png)

Multiplicar la matriz de traducción por la matriz de proyección (T P) proporciona la matriz de proyección compuesta, como se \* muestra en la ilustración siguiente.

![ilustración de la matriz de proyección compuesta](images/projmat3.png)

La transformación de perspectiva convierte un frustum de visualización en un nuevo espacio de coordenadas. Observe que el frustum se convierte en cuboid y que el origen se mueve desde la esquina superior derecha de la escena hasta el centro, como se muestra en el diagrama siguiente.

![diagrama de cómo la transformación de perspectiva cambia el frustum de visualización en un nuevo espacio de coordenadas](images/cuboid.png)

En la transformación de perspectiva, los límites de las direcciones x e y son -1 y 1. Los límites de la dirección Z son 0 para el plano frontal y 1 para el plano posterior.

Esta matriz traduce y escala objetos en función de una distancia especificada desde la cámara al plano de recorte cercano, pero no considera el campo de vista (fov), y los valores z que genera para los objetos a distancia pueden ser casi idénticos, lo que dificulta las comparaciones de profundidad. La siguiente matriz aborda estos problemas y ajusta los vértices para tener en cuenta la relación de aspecto de la ventanilla, lo que la hace una buena elección para la proyección de perspectiva.

![ilustración de una matriz para la proyección de perspectiva](images/prjmatx1.png)

En esta matriz, Zn es el valor z del plano de recorte cercano. Las variables w, h y Q tienen los significados siguientes. Tenga en cuenta que fov<sub>w</sub> y fovk representan los campos de vista horizontal y vertical de la ventanilla, en radianes.

![ecuaciones de los significados de las variables](images/prjmatx2.png)

Para la aplicación, el uso de ángulos de campo de vista para definir los coeficientes de escalado X e Y podría no ser tan cómodo como usar las dimensiones horizontal y vertical de la ventanilla (en el espacio de la cámara). A medida que las matemáticas funcionan, las dos ecuaciones siguientes para w y h usan las dimensiones de la ventanilla y son equivalentes a las ecuaciones anteriores.

![ecuaciones de los significados de las variables w y h](images/prjmatx3.png)

En estas fórmulas, Zn representa la posición del plano de recorte cercano, y las variables V<sub>w</sub> y Vh representan el ancho y el alto de la ventanilla, en el espacio de la cámara.

Para una aplicación de C++, estas dos dimensiones corresponden directamente a los miembros Width y Height de la [**estructura D3DVIEWPORT9.**](d3dviewport9.md)

Sea cual sea la fórmula que decida usar, asegúrese de establecer Zn en un valor lo más grande posible, ya que los valores z muy cercanos a la cámara no varían mucho. Esto hace que las comparaciones de profundidad con búferes z de 16 bits sea algo complicada.

Al igual que con las transformaciones world y view, se llama al método [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para establecer la transformación de proyección.

## <a name="setting-up-a-projection-matrix"></a>Configuración de una matriz de proyección

La siguiente función de ejemplo ProjectionMatrix establece los planos de recorte frontal y posterior, así como el campo horizontal y vertical de los ángulos de vista. Los campos de vista deben ser menores que pi radianes.


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



Después de crear la matriz, esta establezca con [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) especificando D3DTS \_ PROJECTION.

La biblioteca de utilidades D3DX proporciona las siguientes funciones para ayudarle a configurar la matriz de proyección.

-   [**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
-   [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
-   [**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
-   [**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
-   [**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
-   [**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a>Una matriz de proyección W-Friendly

Direct3D puede usar el componente w de un vértice que se ha transformado por el mundo, la vista y las matrices de proyección para realizar cálculos basados en profundidad en efectos de búfer de profundidad o sombreado. Los cálculos como estos requieren que la matriz de proyección normalice w para que sea equivalente al espacio mundial z. En resumen, si la matriz de proyección incluye un coeficiente (3,4) que no es 1, debe escalar todos los coeficientes por el inverso del coeficiente (3,4) para crear una matriz adecuada. Si no proporciona una matriz compatible, no se aplican correctamente los efectos de efecto y el almacenamiento en búfer de profundidad.

En la ilustración siguiente se muestra una matriz de proyección no conforme y la misma matriz se escale para que se habilite el ángulo relativo a los ojos.

![ilustraciones de una matriz de proyección no conforme y una matriz con ángulo relativo a los ojos](images/eyerlmx.png)

En las matrices anteriores, se supone que todas las variables son distintas de cero. Para obtener más información sobre los ojos relativos a los ojos, vea [Eye-Relative vs. Z-Based Depth](pixel-fog.md). Para obtener información sobre el almacenamiento en búfer de profundidad basado en w, vea [Búferes de profundidad (Direct3D 9).](depth-buffers.md)

Direct3D usa la matriz de proyección establecida actualmente en sus cálculos de profundidad basados en w. Como resultado, las aplicaciones deben establecer una matriz de proyección compatible para recibir las características deseadas basadas en w, incluso si no usan Direct3D para las transformaciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transformaciones](transforms.md)
</dt> </dl>

 

 
