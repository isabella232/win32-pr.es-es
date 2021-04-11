---
description: Puede pensar en la transformación proyección como el control de los elementos internos de la cámara. es análogo a elegir una lente para la cámara.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Transformación de proyección (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274733"
---
# <a name="projection-transform-direct3d-9"></a>Transformación de proyección (Direct3D 9)

Puede pensar en la transformación proyección como el control de los elementos internos de la cámara. es análogo a elegir una lente para la cámara. Este es el más complicado de los tres tipos de transformación. Esta explicación de la transformación proyección se organiza en los temas siguientes.

La matriz de proyección es normalmente una proyección de escala y perspectiva. La transformación proyección convierte el frustum de visualización en una forma Cuboid. Dado que el extremo cercano del frustum de visualización es más pequeño que el extremo, tiene el efecto de expandir los objetos que están cerca de la cámara. así es cómo se aplica la perspectiva a la escena.

En [el frustum de visualización](viewports-and-clipping.md), la distancia entre la cámara y el origen del espacio de la transformación de visualización se define arbitrariamente como D, por lo que la matriz de proyección es similar a la siguiente ilustración.

![Ilustración de la matriz de proyección](images/projmat1.png)

La matriz de visualización traduce la cámara al origen mediante la conversión de la dirección z por D. La matriz de traslación es similar a la siguiente ilustración.

![Ilustración de la matriz de traslación](images/projmat2.png)

La multiplicación de la matriz de traslación por la matriz de proyección (T \* P) proporciona la matriz de proyección compuesta, tal como se muestra en la siguiente ilustración.

![Ilustración de la matriz de proyección compuesta](images/projmat3.png)

La transformación perspectiva convierte un frustum de visualización en un nuevo espacio de coordenadas. Observe que el frustum se convierte en CUBOID y que el origen se desplaza desde la esquina superior derecha de la escena hasta el centro, tal como se muestra en el diagrama siguiente.

![diagrama de cómo cambia la transformación de perspectiva el frustum de visualización en un nuevo espacio de coordenadas](images/cuboid.png)

En la transformación perspectiva, los límites de las direcciones x e y son-1 y 1. Los límites de la dirección z son 0 para el plano frontal y 1 para el plano trasero.

Esta matriz convierte y escala los objetos en función de una distancia especificada de la cámara al plano de recorte cercano, pero no tiene en cuenta el campo de vista (hipercampo) y los valores z que genera para los objetos de la distancia pueden ser prácticamente idénticos, lo que dificulta las comparaciones de profundidad. La siguiente matriz aborda estos problemas y ajusta los vértices para que tengan en cuenta la relación de aspecto de la ventanilla, lo que lo convierte en una buena opción para la proyección en perspectiva.

![Ilustración de una matriz para la proyección en perspectiva](images/prjmatx1.png)

En esta matriz, Zn es el valor z del plano de recorte cercano. Las variables w, h y Q tienen los significados siguientes. Tenga en cuenta que el campo de campo y el fovk representan los campos de vista<sub>horizontal y vertical</sub> de la ventanilla, en radianes.

![ecuaciones de los significados de variables](images/prjmatx2.png)

En el caso de la aplicación, el uso de ángulos de campo de vista para definir los coeficientes de escalado x e y podría no ser tan práctico como usar las dimensiones horizontal y vertical de la ventanilla (en el espacio de la cámara). A medida que la matemáticas funciona, las dos ecuaciones siguientes para w y h usan las dimensiones de la ventanilla y son equivalentes a las ecuaciones anteriores.

![ecuaciones de los significados de las variables w y h](images/prjmatx3.png)

En estas fórmulas, Zn representa la posición del plano de recorte cercano y las variables V<sub>w</sub> y VH representan el ancho y el alto de la ventanilla, en el espacio de la cámara.

En el caso de una aplicación de C++, estas dos dimensiones se corresponden directamente con los miembros width y height de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) .

Sea cual sea la fórmula que decida usar, asegúrese de establecer Zn en un valor tan grande como sea posible, ya que los valores z muy cercanos a la cámara no varían en gran medida. Esto realiza comparaciones de profundidad mediante el uso de búferes z de 16 bits, algo complicado.

Al igual que con las transformaciones mundo y ver, se llama al método [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para establecer la transformación de proyección.

## <a name="setting-up-a-projection-matrix"></a>Configuración de una matriz de proyección

La siguiente función de ejemplo ProjectionMatrix establece los planos de recorte delantero y posterior, así como el campo horizontal y vertical de los ángulos de vista. Los campos de la vista deben ser inferiores a PI radianes.


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



Después de crear la matriz, establézcala con [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) que especifique la \_ proyección D3DTS.

La biblioteca de utilidades de D3DX proporciona las siguientes funciones para ayudarle a configurar la matriz de proyección.

-   [**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
-   [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
-   [**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
-   [**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
-   [**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
-   [**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a>Matriz de proyección sencilla

Direct3D puede usar el componente w de un vértice transformado por las matrices World, View y proyecciones para realizar cálculos basados en la profundidad en el búfer de profundidad o en los efectos de niebla. Los cálculos como estos requieren que la matriz de proyección normalice w sea equivalente a la z de espacio universal. En Resumen, si la matriz de proyección incluye un coeficiente (3, 4) que no es 1, debe escalar todos los coeficientes mediante el inverso del coeficiente (3, 4) para crear una matriz adecuada. Si no proporciona una matriz compatible, los efectos de niebla y el almacenamiento en búfer de profundidad no se aplican correctamente.

En la ilustración siguiente se muestra una matriz de proyección no compatible y la misma matriz escalada para que se habilite la niebla relativa a la vista.

![ilustraciones de una matriz de proyección no compatible y una matriz con niebla relativa a la vista](images/eyerlmx.png)

En las matrices anteriores, se supone que todas las variables son distintos de cero. Para obtener más información sobre la niebla relativa a la vista, consulte la [profundidad relativa a la vista en relación con la base Z](pixel-fog.md). Para obtener información sobre el almacenamiento en búfer de profundidad basado en w, vea [búferes de profundidad (Direct3D 9)](depth-buffers.md).

Direct3D usa la matriz de proyección establecida actualmente en los cálculos de profundidad basados en w. Como resultado, las aplicaciones deben establecer una matriz de proyección compatible para recibir las características basadas en w deseadas, incluso si no usan Direct3D para las transformaciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transformaciones](transforms.md)
</dt> </dl>

 

 
