---
description: La biblioteca de utilidades D3DX proporciona la interfaz ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Pilas de matriz (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a480236bc42142b725e232a9fb92807be73fb03097104a0cc4fc08643f4361af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044342"
---
# <a name="matrix-stacks-direct3d-9"></a>Pilas de matriz (Direct3D 9)

La biblioteca de utilidades D3DX proporciona la [**interfaz ID3DXMATRIXStack.**](id3dxmatrixstack.md) Proporciona un mecanismo para permitir que las matrices se puedan insertar y sacar de una pila de matriz. La implementación de una pila de matrices es una manera eficaz de realizar un seguimiento de las matrices mientras se recorre una jerarquía de transformación.

La biblioteca de utilidades D3DX usa una pila de matrices para almacenar transformaciones como matrices. Los distintos métodos de la [**interfaz ID3DXMATRIXStack**](id3dxmatrixstack.md) tratan con la matriz actual o la matriz ubicada en la parte superior de la pila. Puede borrar la matriz actual con el [**método ID3DXMATRIXStack::LoadIdentity.**](id3dxmatrixstack--loadidentity.md) Para especificar explícitamente una determinada matriz que se cargará como la matriz de transformación actual, use el [**método ID3DXMATRIXStack::LoadMatrix.**](id3dxmatrixstack--loadmatrix.md) A continuación, puede llamar al método [**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) o al método [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) para multiplicar la matriz actual por la matriz especificada.

El [**método ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md) permite volver a la matriz de transformación anterior y el método [**ID3DXMATRIXStack::P ush**](id3dxmatrixstack--push.md) agrega una matriz de transformación a la pila.

Las matrices individuales de la pila de matrices se representan como matrices homogéneos 4x4, definidas por la estructura D3DXMATRIX de la biblioteca de utilidades [**D3DXMATRIX.**](d3dxmatrix.md)

La biblioteca de utilidades D3DX proporciona una pila de matrices a través de un objeto de modelo de objetos componentes (COM).

## <a name="implementing-a-scene-hierarchy"></a>Implementación de una jerarquía de escena

Una pila de matriz simplifica la construcción de modelos jerárquicos, en los que los objetos complicados se construyen a partir de una serie de objetos más sencillos.

Una jerarquía de escena o transformación normalmente se representa mediante una estructura de datos de árbol. Cada nodo de la estructura de datos de árbol contiene una matriz. Una matriz determinada representa el cambio en los sistemas de coordenadas del nodo primario al nodo. Por ejemplo, si está modelando un arm humano, puede implementar la jerarquía que se muestra en el diagrama siguiente.

![diagrama de la jerarquía de un arm humano](images/stack1.png)

En esta jerarquía, la matriz Body coloca el cuerpo en el mundo. La matriz UpperArm contiene la rotación del cuello, la matriz LowerArm contiene la rotación del cuello y la matriz hand contiene la rotación de la mano. Para determinar dónde está la mano en relación con el mundo, se multiplican todas las matrices de Cuerpo hacia abajo por Mano juntas.

La jerarquía anterior es demasiado simplista, porque cada nodo tiene solo un elemento secundario. Si empieza a modelar la mano con más detalle, probablemente agregará dedos y un dedo. Cada dígito se puede agregar a la jerarquía como elementos secundarios de Hand, como se muestra en el diagrama siguiente.

![diagrama de la jerarquía de una mano humana](images/stack2.png)

Si recorre el gráfico completo del arm en primer lugar en profundidad (recorriendo un trazado lo más lejos posible antes de pasar a la ruta de acceso siguiente) para dibujar la escena, realizará una secuencia de representación segmentada. Por ejemplo, para representar la mano y los dedos, implemente el siguiente patrón.

1.  Insertar la matriz hand en la pila de matriz.
2.  Dibuje la mano.
3.  Inserta la matriz Thumb en la pila de matriz.
4.  Dibuje el control.
5.  Quitar la matriz Thumb de la pila.
6.  Inserta la matriz Finger 1 en la pila de matriz.
7.  Dibuje el primer dedo.
8.  Quitar la matriz Dedo 1 de la pila.
9.  Inserta la matriz Finger 2 en la pila de matriz. Continúe de esta manera hasta que se represente todos los dedos y el dedo.

Una vez que haya terminado de representar los dedos, quitaría la matriz Hand de la pila.

Puede seguir este proceso básico en el código con los ejemplos siguientes. Cuando encuentre un nodo durante la búsqueda por primera vez en profundidad de la estructura de datos del árbol, presione la matriz en la parte superior de la pila de matrices.


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



Cuando haya terminado con un nodo, despeda la matriz de la parte superior de la pila de matrices.


```
MatrixStack->Pop();
```



De este modo, la matriz de la parte superior de la pila siempre representa la transformación mundial del nodo actual. Por lo tanto, antes de dibujar cada nodo, debe establecer la matriz de Direct3D.


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



Para obtener más información sobre los métodos específicos que puede realizar en una pila de matriz D3DX, vea el tema de referencia [**ID3DXMATRIXStack.**](id3dxmatrixstack.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 



