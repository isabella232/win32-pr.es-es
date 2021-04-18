---
description: La parte de Direct3D que envía la geometría a través de la canalización de geometría de función fija es el motor de transformación.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transformaciones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423148"
---
# <a name="transforms-direct3d-9"></a>Transformaciones (Direct3D 9)

La parte de Direct3D que envía la geometría a través de la canalización de geometría de función fija es el motor de transformación. Busca el modelo y el visor en el mundo, proyecta los vértices para su presentación en la pantalla y recorta los vértices en la ventanilla. El motor de transformación también realiza cálculos de iluminación para determinar los componentes difusos y especulares en cada vértice.

La canalización de geometría toma los vértices como entrada. El motor de transformación aplica las transformaciones mundo, vista y proyección a los vértices, recorta el resultado y pasa todo al rasterizador.

En el encabezado de la canalización, los vértices de un modelo se declaran en relación con un sistema de coordenadas local. Se trata de un origen local y una orientación. Esta orientación de las coordenadas se denomina a menudo espacio de modelo y las coordenadas individuales se denominan coordenadas del modelo.

La primera fase de la canalización de geometría transforma los vértices de un modelo de su sistema de coordenadas local en un sistema de coordenadas que usan todos los objetos de una escena. El proceso de reorientar los vértices se denomina transformación universal. Esta nueva orientación se conoce comúnmente como espacio universal y cada vértice en el espacio universal se declara mediante coordenadas universales.

En la fase siguiente, los vértices que describen el mundo 3D están orientados con respecto a una cámara. Es decir, la aplicación elige un punto de vista para la escena y las coordenadas del espacio universal se reubican y giran alrededor de la vista de la cámara, lo que convierte el espacio universal en el espacio de la cámara. Esta es la transformación de la vista.

La siguiente fase es la transformación de proyección. En esta parte de la canalización, los objetos normalmente se escalan con relación a su distancia desde el visor para dar la sensación de profundidad a una escena. los objetos de cierre se realizan para que aparezcan más grandes que los objetos lejanos, y así sucesivamente. Para simplificar, en esta documentación se hace referencia al espacio en el que los vértices existen después de la transformación de proyección como espacio de proyección. Algunos libros de gráficos pueden hacer referencia al espacio de proyección como espacio homogéneo posterior a la perspectiva. No todas las transformaciones de proyección escalan el tamaño de los objetos en una escena. Una proyección como esta se denomina a veces una proyección afín o ortogonal.

En la parte final de la canalización, se quitan los vértices que no serán visibles en la pantalla, de modo que el rasterizador no dedique tiempo a calcular los colores y el sombreado para algo que nunca se verá. Este proceso se denomina recorte. Después del recorte, los vértices restantes se escalan según los parámetros de la ventanilla y se convierten en coordenadas de pantalla. Los vértices resultantes, que se muestran en la pantalla cuando se rasteriza la escena, existen en el espacio de pantalla.

Las transformaciones se usan para convertir la geometría de objeto de un espacio de coordenadas a otro. Direct3D usa matrices para realizar transformaciones 3D. En esta sección se explica cómo las matrices crean transformaciones 3D, se describen algunos usos comunes de las transformaciones y se detalla cómo se pueden combinar matrices para generar una sola matriz que abarque varias transformaciones.

-   [Universal Transform (Direct3D 9)](world-transform.md) : conversión del espacio de modelo al espacio universal
-   [Transformación de vista (Direct3D 9)](view-transform.md) : conversión del espacio universal al espacio de vista
-   [Transformación de proyección (Direct3D 9)](projection-transform.md) : conversión del espacio de vista al espacio de proyección

## <a name="matrix-transforms"></a>Transformaciones de matriz

En las aplicaciones que funcionan con gráficos 3D, puede usar transformaciones geométricas para hacer lo siguiente:

-   Expresar la ubicación de un objeto con respecto a otro objeto.
-   Rotar y ajustar el tamaño de los objetos.
-   Cambiar las posiciones, las direcciones y las perspectivas de visualización.

Puede transformar cualquier punto (x, y, z) en otro punto (x ', y ', z ') mediante una matriz 4x4, tal como se muestra en la siguiente ecuación.

![ecuación de transformar cualquier punto en otro punto](images/matmult.png)

Realice las ecuaciones siguientes en (x, y, z) y en la matriz para generar el punto (x ', y ', z ').

![ecuaciones para el nuevo punto](images/matexpnd.png)

Las transformaciones más comunes son traducción, rotación y escalado. Puede combinar las matrices que producen estos efectos en una sola matriz para calcular varias transformaciones a la vez. Por ejemplo, puede crear una matriz única para traducir y girar una serie de puntos.

Las matrices se escriben en orden de fila y columna. Una matriz que escala uniformemente los vértices a lo largo de cada eje, conocido como escala uniforme, se representa mediante la siguiente matriz mediante notación matemática.

![ecuación de una matriz para el escalado uniforme](images/matrix.png)

En C++, Direct3D declara las matrices como una matriz bidimensional mediante la estructura [**D3DMATRIX**](d3dmatrix.md) . En el ejemplo siguiente se muestra cómo inicializar una estructura **D3DMATRIX** para que actúe como una matriz de escalado uniforme.


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a>Translate

La ecuación siguiente traduce el punto (x, y, z) a un nuevo punto (x ', y ', z ').

![ecuación de una matriz de traslación para un nuevo punto](images/transl8.png)

Puede crear manualmente una matriz de traducción en C++. En el ejemplo siguiente se muestra el código fuente de una función que crea una matriz para traducir los vértices.


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



Para mayor comodidad, la biblioteca de utilidades de D3DX proporciona la función [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) .

## <a name="scale"></a>Escala

La ecuación siguiente escala el punto (x, y, z) mediante valores arbitrarios en las direcciones x-, y-y z-a un punto nuevo (x ', y ', z ').

![ecuación de una matriz de escala para un nuevo punto](images/matscale.png)

## <a name="rotate"></a>Girar

Las transformaciones que se describen aquí son para los sistemas de coordenadas de la mano izquierda y, por tanto, pueden ser diferentes de las matrices de transformación que se han encontrado en otro lugar.

La siguiente ecuación gira el punto (x, y, z) alrededor del eje x, lo que produce un nuevo punto (x ', y ', z ').

![ecuación de una matriz de rotación x para un nuevo punto](images/matxrot.png)

La siguiente ecuación gira el punto alrededor del eje y.

![ecuación de una matriz de rotación y para un nuevo punto](images/matyrot.png)

La siguiente ecuación gira el punto alrededor del eje z.

![ecuación de una matriz de rotación z para un nuevo punto](images/matzrot.png)

En estas matrices de ejemplo, la letra griega Theta representa el ángulo de rotación, en radianes. Los ángulos se miden en el sentido de las agujas del reloj al mirar el eje de giro hacia el origen.

En una aplicación de C++, use las funciones [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)y [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) que proporciona la biblioteca de utilidades de D3DX para crear matrices de rotación. A continuación se encuentra el código de la función **D3DXMatrixRotationX** .


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a>Concatenación de matrices

Una ventaja de usar matrices es que se pueden combinar los efectos de dos o más matrices multiplicándolos. Esto significa que, para girar un modelo y, a continuación, convertirlo en una ubicación, no es necesario aplicar dos matrices. En su lugar, se multiplican las matrices de traslación y rotación para producir una matriz compuesta que contiene todos sus efectos. Este proceso, denominado concatenación de matriz, se puede escribir con la siguiente ecuación.

![ecuación de concatenación de matriz](images/matrxcat.png)

En esta ecuación, C es la matriz compuesta que se está creando y M ₁ a MN son las matrices individuales. En la mayoría de los casos, solo se concatenan dos o tres matrices, pero no hay ningún límite.

Use la función [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) para realizar la multiplicación de matrices.

El orden en el que se realiza la multiplicación de matrices es fundamental. La fórmula anterior refleja la regla de izquierda a derecha de la concatenación de matrices. Es decir, los efectos visibles de las matrices que se usan para crear una matriz compuesta se producen en orden de izquierda a derecha. En el ejemplo siguiente se muestra una matriz universal típica. Imagine que va a crear la matriz mundial para un típica volando Saucer. Probablemente quiera girar el Saucer volando en torno a su centro, el eje y del espacio del modelo, y convertirlo en otra ubicación de la escena. Para lograr este efecto, primero se crea una matriz de rotación y, a continuación, se multiplica por una matriz de traslación, tal como se muestra en la siguiente ecuación.

![ecuación de giro basada en una matriz de rotación y una matriz de traslación](images/wrldexpl.png)

En esta fórmula, R<sub>y</sub> es una matriz de rotación sobre el eje y, y T<sub>w</sub> es una traducción a alguna posición en coordenadas universales.

El orden en que se multiplican las matrices es importante porque, a diferencia de la multiplicación de dos valores escalares, la multiplicación de matrices no es conmutativa. La multiplicación de las matrices en el orden opuesto tiene el efecto visual de traducir el Saucer volando a su posición de espacio mundial y, a continuación, girarlo alrededor del origen mundial.

Independientemente del tipo de matriz que cree, recuerde la regla de izquierda a derecha para asegurarse de que se obtienen los efectos esperados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 



