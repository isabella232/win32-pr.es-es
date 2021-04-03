---
description: La biblioteca de utilidades de D3DX proporciona la interfaz ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Pilas de matrices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d535307fb99d8743b910f2f3f8c6d55e197748e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906668"
---
# <a name="matrix-stacks-direct3d-9"></a>Pilas de matrices (Direct3D 9)

La biblioteca de utilidades de D3DX proporciona la interfaz [**ID3DXMATRIXStack**](id3dxmatrixstack.md) . Proporciona un mecanismo para permitir que las matrices se inserten en una pila de matriz y se extraigan de ella. Implementar una pila de matriz es una manera eficaz de realizar un seguimiento de las matrices mientras se atraviesa una jerarquía de transformación.

La biblioteca de utilidades de D3DX usa una pila de matrices para almacenar transformaciones como matrices. Los distintos métodos de la interfaz [**ID3DXMATRIXStack**](id3dxmatrixstack.md) se ocupan de la matriz actual o de la matriz que se encuentra en la parte superior de la pila. Puede borrar la matriz actual con el método [**ID3DXMATRIXStack:: LoadIdentity**](id3dxmatrixstack--loadidentity.md) . Para especificar explícitamente una matriz determinada que se va a cargar como la matriz de transformación actual, use el método [**ID3DXMATRIXStack:: LoadMatrix**](id3dxmatrixstack--loadmatrix.md) . Después, puede llamar al método [**ID3DXMATRIXStack:: MultMatrix**](id3dxmatrixstack--multmatrix.md) o [**ID3DXMATRIXStack:: MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) para multiplicar la matriz actual por la matriz especificada.

El método [**ID3DXMATRIXStack::P OP**](id3dxmatrixstack--pop.md) permite volver a la matriz de transformación anterior y el método [**ID3DXMATRIXStack::P uscripción**](id3dxmatrixstack--push.md) agrega una matriz de transformación a la pila.

Las matrices individuales de la pila de matriz se representan como matrices homogéneas 4x4, definidas por la estructura [**D3DXMATRIX**](d3dxmatrix.md) de la biblioteca de utilidades de D3DX.

La biblioteca de utilidades de D3DX proporciona una pila de matriz a través de un objeto de modelo de objetos componentes (COM).

## <a name="implementing-a-scene-hierarchy"></a>Implementar una jerarquía de escenas

Una pila de matriz simplifica la construcción de modelos jerárquicos, en los que los objetos complicados se construyen a partir de una serie de objetos más simples.

Normalmente, una estructura de datos de árbol representa una escena o una transformación. Cada nodo de la estructura de datos de árbol contiene una matriz. Una matriz determinada representa el cambio en los sistemas de coordenadas del elemento primario del nodo al nodo. Por ejemplo, si está modelando un brazo humano, podría implementar la jerarquía que se muestra en el diagrama siguiente.

![diagrama de la jerarquía de un brazo humano](images/stack1.png)

En esta jerarquía, la matriz de cuerpo coloca el cuerpo del mundo. La matriz UpperArm contiene el giro del hombro, la matriz LowerArm contiene el giro del codo y la matriz de la mano contiene el giro de la muñeca. Para determinar si la mano es relativa al mundo, debe multiplicar todas las matrices del cuerpo hacia abajo a la mano.

La jerarquía anterior es demasiado simplista, porque cada nodo solo tiene un elemento secundario. Si empieza a modelar la mano con más detalle, probablemente agregará dedos y un control Thumb. Cada dígito puede agregarse a la jerarquía como elemento secundario, tal y como se muestra en el diagrama siguiente.

![diagrama de la jerarquía de una mano](images/stack2.png)

Si recorre el gráfico completo del brazo en orden con prioridad a la profundidad, recorriendo el recorrido hasta un trazado como sea posible antes de pasar a la siguiente ruta de acceso: para dibujar la escena, realice una secuencia de representación segmentada. Por ejemplo, para representar la mano y los dedos, implemente el siguiente patrón.

1.  Inserte la matriz de mano en la pila de la matriz.
2.  Dibuje la mano.
3.  Inserte la matriz Thumb en la pila de la matriz.
4.  Dibuje el control Thumb.
5.  Extrae la matriz Thumb de la pila.
6.  Inserte el dedo 1 matriz en la pila de la matriz.
7.  Dibuje el primer dedo.
8.  Extrae la matriz de dedo 1 de la pila.
9.  Inserte el dedo 2 matriz en la pila de la matriz. Puede continuar de esta manera hasta que se representen todos los dedos y el control de posición.

Una vez que haya terminado de representar los dedos, verá la matriz de mano fuera de la pila.

Puede seguir este proceso básico en el código con los ejemplos siguientes. Cuando se encuentra un nodo durante la búsqueda con prioridad a la profundidad de la estructura de datos de árbol, inserte la matriz en la parte superior de la pila de la matriz.


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



Cuando haya terminado con un nodo, desactive la matriz de la parte superior de la pila de la matriz.


```
MatrixStack->Pop();
```



De esta manera, la matriz de la parte superior de la pila siempre representa la transformación mundial del nodo actual. Por lo tanto, antes de dibujar cada nodo, debe establecer la matriz de Direct3D.


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



Para obtener más información sobre los métodos específicos que se pueden realizar en una pila de matrices de D3DX, vea el tema de referencia de [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 



