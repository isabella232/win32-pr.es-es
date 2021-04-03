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
# <a name="matrix-stacks-direct3d-9"></a><span data-ttu-id="5a47b-103">Pilas de matrices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5a47b-103">Matrix Stacks (Direct3D 9)</span></span>

<span data-ttu-id="5a47b-104">La biblioteca de utilidades de D3DX proporciona la interfaz [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="5a47b-104">The D3DX utility library provides the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span> <span data-ttu-id="5a47b-105">Proporciona un mecanismo para permitir que las matrices se inserten en una pila de matriz y se extraigan de ella.</span><span class="sxs-lookup"><span data-stu-id="5a47b-105">It supplies a mechanism to enable matrices to be pushed onto and popped off of a matrix stack.</span></span> <span data-ttu-id="5a47b-106">Implementar una pila de matriz es una manera eficaz de realizar un seguimiento de las matrices mientras se atraviesa una jerarquía de transformación.</span><span class="sxs-lookup"><span data-stu-id="5a47b-106">Implementing a matrix stack is an efficient way to track matrices while traversing a transform hierarchy.</span></span>

<span data-ttu-id="5a47b-107">La biblioteca de utilidades de D3DX usa una pila de matrices para almacenar transformaciones como matrices.</span><span class="sxs-lookup"><span data-stu-id="5a47b-107">The D3DX utility library uses a matrix stack to store transformations as matrices.</span></span> <span data-ttu-id="5a47b-108">Los distintos métodos de la interfaz [**ID3DXMATRIXStack**](id3dxmatrixstack.md) se ocupan de la matriz actual o de la matriz que se encuentra en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="5a47b-108">The various methods of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface deal with the current matrix, or the matrix located on top of the stack.</span></span> <span data-ttu-id="5a47b-109">Puede borrar la matriz actual con el método [**ID3DXMATRIXStack:: LoadIdentity**](id3dxmatrixstack--loadidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="5a47b-109">You can clear the current matrix with the [**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md) method.</span></span> <span data-ttu-id="5a47b-110">Para especificar explícitamente una matriz determinada que se va a cargar como la matriz de transformación actual, use el método [**ID3DXMATRIXStack:: LoadMatrix**](id3dxmatrixstack--loadmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="5a47b-110">To explicitly specify a certain matrix to load as the current transformation matrix, use the [**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md) method.</span></span> <span data-ttu-id="5a47b-111">Después, puede llamar al método [**ID3DXMATRIXStack:: MultMatrix**](id3dxmatrixstack--multmatrix.md) o [**ID3DXMATRIXStack:: MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) para multiplicar la matriz actual por la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="5a47b-111">Then you can call either the [**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) method or the [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) method to multiply the current matrix by the specified matrix.</span></span>

<span data-ttu-id="5a47b-112">El método [**ID3DXMATRIXStack::P OP**](id3dxmatrixstack--pop.md) permite volver a la matriz de transformación anterior y el método [**ID3DXMATRIXStack::P uscripción**](id3dxmatrixstack--push.md) agrega una matriz de transformación a la pila.</span><span class="sxs-lookup"><span data-stu-id="5a47b-112">The [**ID3DXMATRIXStack::Pop**](id3dxmatrixstack--pop.md) method enables you to return to the previous transformation matrix and the [**ID3DXMATRIXStack::Push**](id3dxmatrixstack--push.md) method adds a transformation matrix to the stack.</span></span>

<span data-ttu-id="5a47b-113">Las matrices individuales de la pila de matriz se representan como matrices homogéneas 4x4, definidas por la estructura [**D3DXMATRIX**](d3dxmatrix.md) de la biblioteca de utilidades de D3DX.</span><span class="sxs-lookup"><span data-stu-id="5a47b-113">The individual matrices on the matrix stack are represented as 4x4 homogeneous matrices, defined by the D3DX utility library [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

<span data-ttu-id="5a47b-114">La biblioteca de utilidades de D3DX proporciona una pila de matriz a través de un objeto de modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="5a47b-114">The D3DX utility library provides a matrix stack through a component object model (COM) object.</span></span>

## <a name="implementing-a-scene-hierarchy"></a><span data-ttu-id="5a47b-115">Implementar una jerarquía de escenas</span><span class="sxs-lookup"><span data-stu-id="5a47b-115">Implementing a Scene Hierarchy</span></span>

<span data-ttu-id="5a47b-116">Una pila de matriz simplifica la construcción de modelos jerárquicos, en los que los objetos complicados se construyen a partir de una serie de objetos más simples.</span><span class="sxs-lookup"><span data-stu-id="5a47b-116">A matrix stack simplifies the construction of hierarchical models, in which complicated objects are constructed from a series of simpler objects.</span></span>

<span data-ttu-id="5a47b-117">Normalmente, una estructura de datos de árbol representa una escena o una transformación.</span><span class="sxs-lookup"><span data-stu-id="5a47b-117">A scene, or transform, hierarchy is usually represented by a tree data structure.</span></span> <span data-ttu-id="5a47b-118">Cada nodo de la estructura de datos de árbol contiene una matriz.</span><span class="sxs-lookup"><span data-stu-id="5a47b-118">Each node in the tree data structure contains a matrix.</span></span> <span data-ttu-id="5a47b-119">Una matriz determinada representa el cambio en los sistemas de coordenadas del elemento primario del nodo al nodo.</span><span class="sxs-lookup"><span data-stu-id="5a47b-119">A particular matrix represents the change in coordinate systems from the node's parent to the node.</span></span> <span data-ttu-id="5a47b-120">Por ejemplo, si está modelando un brazo humano, podría implementar la jerarquía que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="5a47b-120">For example, if you are modeling a human arm, you might implement the hierarchy that is shown in the following diagram.</span></span>

![diagrama de la jerarquía de un brazo humano](images/stack1.png)

<span data-ttu-id="5a47b-122">En esta jerarquía, la matriz de cuerpo coloca el cuerpo del mundo.</span><span class="sxs-lookup"><span data-stu-id="5a47b-122">In this hierarchy, the Body matrix places the body in the world.</span></span> <span data-ttu-id="5a47b-123">La matriz UpperArm contiene el giro del hombro, la matriz LowerArm contiene el giro del codo y la matriz de la mano contiene el giro de la muñeca.</span><span class="sxs-lookup"><span data-stu-id="5a47b-123">The UpperArm matrix contains the rotation of the shoulder, the LowerArm matrix contains the rotation of the elbow, and the Hand matrix contains the rotation of the wrist.</span></span> <span data-ttu-id="5a47b-124">Para determinar si la mano es relativa al mundo, debe multiplicar todas las matrices del cuerpo hacia abajo a la mano.</span><span class="sxs-lookup"><span data-stu-id="5a47b-124">To determine where the hand is relative to the world, you multiply all the matrices from Body down through Hand together.</span></span>

<span data-ttu-id="5a47b-125">La jerarquía anterior es demasiado simplista, porque cada nodo solo tiene un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="5a47b-125">The previous hierarchy is overly simplistic, because each node has only one child.</span></span> <span data-ttu-id="5a47b-126">Si empieza a modelar la mano con más detalle, probablemente agregará dedos y un control Thumb.</span><span class="sxs-lookup"><span data-stu-id="5a47b-126">If you begin to model the hand in more detail, you will probably add fingers and a thumb.</span></span> <span data-ttu-id="5a47b-127">Cada dígito puede agregarse a la jerarquía como elemento secundario, tal y como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="5a47b-127">Each digit can be added to the hierarchy as children of Hand, as shown in the following diagram.</span></span>

![diagrama de la jerarquía de una mano](images/stack2.png)

<span data-ttu-id="5a47b-129">Si recorre el gráfico completo del brazo en orden con prioridad a la profundidad, recorriendo el recorrido hasta un trazado como sea posible antes de pasar a la siguiente ruta de acceso: para dibujar la escena, realice una secuencia de representación segmentada.</span><span class="sxs-lookup"><span data-stu-id="5a47b-129">If you traverse the complete graph of the arm in depth-first order - traversing as far down one path as possible before moving on to the next path - to draw the scene, you perform a sequence of segmented rendering.</span></span> <span data-ttu-id="5a47b-130">Por ejemplo, para representar la mano y los dedos, implemente el siguiente patrón.</span><span class="sxs-lookup"><span data-stu-id="5a47b-130">For example, to render the hand and fingers, you implement the following pattern.</span></span>

1.  <span data-ttu-id="5a47b-131">Inserte la matriz de mano en la pila de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a47b-131">Push the Hand matrix onto the matrix stack.</span></span>
2.  <span data-ttu-id="5a47b-132">Dibuje la mano.</span><span class="sxs-lookup"><span data-stu-id="5a47b-132">Draw the hand.</span></span>
3.  <span data-ttu-id="5a47b-133">Inserte la matriz Thumb en la pila de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a47b-133">Push the Thumb matrix onto the matrix stack.</span></span>
4.  <span data-ttu-id="5a47b-134">Dibuje el control Thumb.</span><span class="sxs-lookup"><span data-stu-id="5a47b-134">Draw the thumb.</span></span>
5.  <span data-ttu-id="5a47b-135">Extrae la matriz Thumb de la pila.</span><span class="sxs-lookup"><span data-stu-id="5a47b-135">Pop the Thumb matrix off the stack.</span></span>
6.  <span data-ttu-id="5a47b-136">Inserte el dedo 1 matriz en la pila de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a47b-136">Push the Finger 1 matrix onto the matrix stack.</span></span>
7.  <span data-ttu-id="5a47b-137">Dibuje el primer dedo.</span><span class="sxs-lookup"><span data-stu-id="5a47b-137">Draw the first finger.</span></span>
8.  <span data-ttu-id="5a47b-138">Extrae la matriz de dedo 1 de la pila.</span><span class="sxs-lookup"><span data-stu-id="5a47b-138">Pop the Finger 1 matrix off the stack.</span></span>
9.  <span data-ttu-id="5a47b-139">Inserte el dedo 2 matriz en la pila de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a47b-139">Push the Finger 2 matrix onto the matrix stack.</span></span> <span data-ttu-id="5a47b-140">Puede continuar de esta manera hasta que se representen todos los dedos y el control de posición.</span><span class="sxs-lookup"><span data-stu-id="5a47b-140">You continue in this manner until all the fingers and thumb are rendered.</span></span>

<span data-ttu-id="5a47b-141">Una vez que haya terminado de representar los dedos, verá la matriz de mano fuera de la pila.</span><span class="sxs-lookup"><span data-stu-id="5a47b-141">After you have completed rendering the fingers, you would pop the Hand matrix off the stack.</span></span>

<span data-ttu-id="5a47b-142">Puede seguir este proceso básico en el código con los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="5a47b-142">You can follow this basic process in code with the following examples.</span></span> <span data-ttu-id="5a47b-143">Cuando se encuentra un nodo durante la búsqueda con prioridad a la profundidad de la estructura de datos de árbol, inserte la matriz en la parte superior de la pila de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a47b-143">When you encounter a node during the depth-first search of the tree data structure, push the matrix onto the top of the matrix stack.</span></span>


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



<span data-ttu-id="5a47b-144">Cuando haya terminado con un nodo, desactive la matriz de la parte superior de la pila de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a47b-144">When you are finished with a node, pop the matrix off the top of the matrix stack.</span></span>


```
MatrixStack->Pop();
```



<span data-ttu-id="5a47b-145">De esta manera, la matriz de la parte superior de la pila siempre representa la transformación mundial del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="5a47b-145">In this way, the matrix on the top of the stack always represents the world-transform of the current node.</span></span> <span data-ttu-id="5a47b-146">Por lo tanto, antes de dibujar cada nodo, debe establecer la matriz de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5a47b-146">Therefore, before drawing each node, you should set the Direct3D matrix.</span></span>


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



<span data-ttu-id="5a47b-147">Para obtener más información sobre los métodos específicos que se pueden realizar en una pila de matrices de D3DX, vea el tema de referencia de [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="5a47b-147">For more information about the specific methods that you can perform on a D3DX matrix stack, see the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) reference topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a47b-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a47b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a47b-149">Canalización de vértices</span><span class="sxs-lookup"><span data-stu-id="5a47b-149">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



