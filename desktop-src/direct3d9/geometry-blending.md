---
description: Direct3D permite que una aplicación aumente el realismo de sus escenas mediante la representación de objetos poligonales segmentados (especialmente caracteres) que tienen uniones mezcladas sin problemas.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Combinación de geometría (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805186"
---
# <a name="geometry-blending-direct3d-9"></a>Combinación de geometría (Direct3D 9)

Direct3D permite que una aplicación aumente el realismo de sus escenas mediante la representación de objetos poligonales segmentados (especialmente caracteres) que tienen uniones mezcladas sin problemas. Estos efectos se denominan a menudo como aspectos. Para lograr este efecto, el sistema aplica matrices de transformación universal adicionales a un único conjunto de vértices para crear varios resultados y, a continuación, realiza una mezcla lineal entre los vértices resultantes para crear un único conjunto de geometría para la representación. En la siguiente ilustración de un plátano se muestra este proceso.

![Ilustración del proceso para fusionar dos objetos con textura de banana](images/geometry-blend.png)

En la ilustración anterior se muestra cómo puede imaginarse el proceso de combinación de geometría. En una única llamada de representación, el sistema toma los vértices del banana, los transforma dos veces (una vez sin modificación) y una vez con una rotación simple, y combina los resultados para crear una banana doblada. El sistema combina la posición del vértice, así como el vértice normal cuando se habilita la iluminación. Las aplicaciones no se limitan a dos rutas de acceso de mezcla; Direct3D puede fusionar la geometría entre un máximo de cuatro matrices mundiales, incluida la matriz mundial del mundo, [**D3DTS \_ World**](d3dts-world.md).

> [!Note]
>
> Cuando se habilita la iluminación, las normales de vértice se transforman mediante una matriz de vista mundial inversa correspondiente, ponderada de la misma manera que los cálculos de posición de vértices. El sistema normaliza el vector normal resultante si el estado de \_ representación de D3DRS NORMALIZENORMALS se establece en **true**.

 

Sin la combinación de geometría, los modelos dinámicos articulados a menudo se representan en segmentos. Por ejemplo, considere un modelo 3D del brazo humano. En la vista más simple, un brazo tiene dos partes: el brazo superior que se conecta al cuerpo y el brazo inferior, que se conecta a la mano. Los dos están conectados en el codo y el brazo inferior gira en ese punto. Una aplicación que representa un brazo podría conservar los datos de vértice para el brazo superior e inferior, cada uno con una matriz de transformación internacional independiente. En el siguiente ejemplo código se muestra cómo hacerlo.


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



Para representar el ARM, se realizan dos llamadas de representación, como se muestra en el código siguiente.


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



La siguiente ilustración es un plátano, modificado para usar esta técnica.

![Ilustración de un plátano mezclado sin combinación de geometría](images/noblend.png)

Las diferencias entre la geometría combinada y la geometría no fusionada son obvias. Este ejemplo es algo extremo. En una aplicación real, las uniones de modelos segmentados están diseñadas para que las costuras no sean tan obvias. Sin embargo, las costuras son visibles en ocasiones, lo que presenta desafíos constantes para los diseñadores de modelos.

La combinación de geometría en Direct3D presenta una alternativa al escenario de modelado segmentado clásico. Sin embargo, la calidad visual mejorada de los objetos segmentados se refiere al costo de los cálculos de mezcla durante la representación. Para minimizar el impacto de estas operaciones adicionales, la canalización de geometría de Direct3D está optimizada para fusionar la geometría con la menor sobrecarga posible. Las aplicaciones que usan de forma inteligente los servicios de combinación de geometría que ofrece Direct3D pueden mejorar el realismo de sus caracteres a la vez que evitan repercusiones graves en el rendimiento.

## <a name="blending-transform-and-render-states"></a>Mezcla de Estados de transformación y representación

El método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) reconoce las macros [**D3DTS \_ World**](d3dts-world.md) y [**D3DTS \_ worldan**](d3dts-worldn.md) , que corresponden a los valores que se pueden definir mediante la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) . Estas macros se utilizan para identificar las matrices entre las que se combinará Geometry.

El tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) incluye el estado de representación de D3DRS \_ VERTEXBLEND para habilitar y controlar la combinación de geometría. Los valores válidos para este estado de representación se definen mediante el tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Si está habilitada la combinación de geometría, el formato de vértice debe incluir el número adecuado de pesos de fusión.

## <a name="blending-weights"></a>Pesos de fusión

Un peso de fusión, que a veces se denomina peso beta, controla la medida en que una matriz universal determinada afecta a un vértice. Los pesos de la mezcla son valores de punto flotante que van de 0,0 a 1,0, codificados en formato de vértice, donde un valor de 0,0 significa que el vértice no se combina con esa matriz y 1,0 significa que el vértice se ve afectado por la matriz.

Los pesos de la combinación de geometría se codifican en el formato de vértices, que aparecen inmediatamente después de la posición de cada vértice, como se describe en [códigos FVF de función fija (Direct3D 9)](fixed-function-fvf-codes.md). Para comunicar el número de pesos de fusión en el formato de vértice, incluya una de las [constantes FVF](d3dfvf.md) en la descripción del vértice que proporcione a los métodos de representación.

El sistema realiza una mezcla lineal entre los resultados ponderados de las matrices de Blend. La siguiente ecuación es la fórmula de combinación completa.

![ecuación de combinación lineal con matrices de transformación universal](images/vert-blend-formula.png)

En la ecuación anterior, vBlend es el vértice de salida, los elementos v son los vértices producidos por la matriz universal aplicada ([**D3DTS \_ worlda**](d3dts-worldn.md)). Los elementos W son los valores de peso correspondientes en el formato de vértice. Un vértice mezclado entre n matrices puede tener-1 valores de peso de fusión, uno para cada matriz de mezcla, excepto el último. El sistema genera automáticamente el peso de la matriz del último mundo, de modo que la suma de todos los pesos sea 1,0, expresada en la notación Sigma aquí. Esta fórmula se puede simplificar para cada uno de los casos que admite Direct3D, que se muestra en las siguientes ecuaciones.

![ecuaciones de combinación lineal para tres casos de combinación](images/vert-blend-formulas-simple.png)

Estas son las formas simplificadas de la fórmula de combinación completa para los dos, tres y cuatro casos de matriz de mezcla.

> [!Note]  
> Aunque Direct3D incluye descriptores de FVF para definir vértices que contengan hasta cinco pesos de fusión, solo se pueden usar tres en esta versión de DirectX.

 

En los temas siguientes se incluye información adicional.

-   [Usar la combinación de geometría (Direct3D 9)](using-geometry-blending.md)
-   [Fusión de vértices indizados (Direct3D 9)](indexed-vertex-blending.md)
-   [Interpolación de vértices (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 
