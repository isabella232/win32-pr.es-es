---
description: Direct3D permite a una aplicación aumentar el realismo de sus escenas mediante la representación de objetos poligonales segmentados (especialmente caracteres) que tienen uniones mezcladas sin problemas.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Combinación de geometría (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71bb449b592c69ae2cf41487aef229718149eb4c1465d90f8b358d30458b69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122181"
---
# <a name="geometry-blending-direct3d-9"></a>Combinación de geometría (Direct3D 9)

Direct3D permite a una aplicación aumentar el realismo de sus escenas mediante la representación de objetos poligonales segmentados (especialmente caracteres) que tienen uniones mezcladas sin problemas. Estos efectos se conocen a menudo como desnasado. El sistema logra este efecto aplicando matrices de transformación del mundo adicionales a un único conjunto de vértices para crear varios resultados y, a continuación, realizando una combinación lineal entre los vértices resultantes para crear un único conjunto de geometría para la representación. En la siguiente ilustración de un tordo se muestra este proceso.

![ilustración del proceso para combinar dos objetos con textura de manzana](images/geometry-blend.png)

En la ilustración anterior se muestra cómo puede imaginar el proceso de combinación de geometría. En una sola llamada de representación, el sistema toma los vértices del manzana, los transforma dos veces (una vez sin modificación y otra con una rotación simple) y combina los resultados para crear un torticera. El sistema combina la posición del vértice, así como el vértice normal cuando se habilita la iluminación. Las aplicaciones no se limitan a dos rutas de acceso de combinación; Direct3D puede combinar geometría entre hasta cuatro matrices del mundo, incluida la matriz del mundo estándar, [**D3DTS \_ WORLD.**](d3dts-world.md)

> [!Note]
>
> Cuando la iluminación está habilitada, las normales de vértice se transforman mediante una matriz inversa de vista inversa correspondiente, ponderada de la misma manera que los cálculos de posición del vértice. El sistema normaliza el vector normal resultante si el estado de representación NORMALIZENORMALS de D3DRS \_ está establecido en **TRUE.**

 

Sin la combinación de geometría, los modelos articulados dinámicos a menudo se representan en segmentos. Por ejemplo, considere un modelo 3D del brazo humano. En la vista más sencilla, un arm tiene dos partes: el arm superior que se conecta al cuerpo y el arm inferior, que se conecta a la mano. Los dos están conectados en el ala y el brazo inferior gira en ese punto. Una aplicación que representa un arm podría conservar los datos de vértices para el arm superior e inferior, cada uno con una matriz de transformación del mundo independiente. En el siguiente ejemplo código se muestra cómo hacerlo.


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



Para representar el arm, se realizan dos llamadas de representación, como se muestra en el código siguiente.


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



La siguiente ilustración es un manzana, modificado para usar esta técnica.

![ilustración de un manzana mezclada sin mezcla de geometría](images/noblend.png)

Las diferencias entre la geometría mezclada y la geometría no desconsolada son obvias. Este ejemplo es algo extremo. En una aplicación real, las uniones de los modelos segmentados están diseñadas para que las uniones no sean tan obvias. Sin embargo, las juntas son visibles a veces, lo que presenta desafíos constantes para los diseñadores de modelos.

La combinación de geometría en Direct3D presenta una alternativa al escenario clásico de modelado segmentado. Sin embargo, la calidad visual mejorada de los objetos segmentados se produce a costa de los cálculos de combinación durante la representación. Para minimizar el impacto de estas operaciones adicionales, la canalización de geometría de Direct3D está optimizada para combinar geometría con la menor sobrecarga posible. Las aplicaciones que usan de forma inteligente los servicios de combinación de geometría que ofrece Direct3D pueden mejorar el realismo de sus caracteres, al tiempo que evitan graves consecuencias en el rendimiento.

## <a name="blending-transform-and-render-states"></a>Combinar estados de transformación y representación

El [**método IDirect3DDevice9::SetTransform**](/windows/desktop/api) reconoce las macros [**D3DTS \_ WORLD**](d3dts-world.md) y [**D3DTS \_ WORLDn,**](d3dts-worldn.md) que corresponden a valores que se pueden definir mediante la macro [**\_ WORLDMATRIX de D3DTS.**](d3dts-worldmatrix.md) Estas macros se usan para identificar las matrices entre las que se combinará la geometría.

El [**tipo enumerado D3DRENDERSTATETYPE**](./d3drenderstatetype.md) incluye el estado de representación VERTEXBLEND de D3DRS para habilitar y controlar la combinación \_ de geometría. El tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) define los valores válidos para este estado de representación. Si la combinación de geometría está habilitada, el formato de vértice debe incluir el número adecuado de pesos de mezcla.

## <a name="blending-weights"></a>Mezclar pesos

Un peso combinado, a veces denominado peso beta, controla hasta qué punto una matriz mundial determinada afecta a un vértice. Las ponderaciones de combinación son valores de punto flotante que oscilan entre 0,0 y 1,0, codificados en el formato de vértice, donde un valor de 0,0 significa que el vértice no se combina con esa matriz y 1,0 significa que el vértice se ve afectado en su totalidad por la matriz.

Los pesos de combinación de geometría se codifican en el formato de vértice, que aparece inmediatamente después de la posición de cada vértice, como se describe en Códigos FVF de función fija [(Direct3D 9).](fixed-function-fvf-codes.md) Para comunicar el número de pesos de mezcla en el formato de vértice, incluya una de las constantes FVF en la descripción del vértice que proporcione a los [métodos](d3dfvf.md) de representación.

El sistema realiza una combinación lineal entre los resultados ponderados de las matrices de mezcla. La ecuación siguiente es la fórmula de combinación completa.

![ecuación de combinación lineal, mediante matrices de transformación mundial](images/vert-blend-formula.png)

En la ecuación anterior, vBlend es el vértice de salida, los elementos v son los vértices producidos por la matriz del mundo aplicada [**(D3DTS \_ WORLDn**](d3dts-worldn.md)). Los elementos W son los valores de peso correspondientes en el formato de vértice. Un vértice combinado entre n matrices puede tener - 1 valores de peso de mezcla, uno para cada matriz de mezcla, excepto el último. El sistema genera automáticamente el peso de la matriz del último mundo para que la suma de todas las ponderaciones sea 1,0, expresada aquí en notación sigma. Esta fórmula se puede simplificar para cada uno de los casos admitidos por Direct3D, que se muestra en las ecuaciones siguientes.

![ecuaciones de combinación lineal para tres casos de combinación](images/vert-blend-formulas-simple.png)

Estas son las formas simplificadas de la fórmula de combinación completa para los dos, tres y cuatro casos de matriz de mezcla.

> [!Note]  
> Aunque Direct3D incluye descriptores FVF para definir vértices que contienen hasta cinco pesos de combinación, solo se pueden usar tres en esta versión de DirectX.

 

En los temas siguientes se incluye información adicional.

-   [Uso de la combinación de geometría (Direct3D 9)](using-geometry-blending.md)
-   [Mezcla de vértices indexados (Direct3D 9)](indexed-vertex-blending.md)
-   [Interpolación de vértices (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 
