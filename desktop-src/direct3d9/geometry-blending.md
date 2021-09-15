---
description: Direct3D permite a una aplicación aumentar el realismo de sus escenas mediante la representación de objetos poligonales segmentados (especialmente caracteres) que tienen uniones mezcladas sin problemas.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Mezcla de geometría (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565969"
---
# <a name="geometry-blending-direct3d-9"></a>Mezcla de geometría (Direct3D 9)

Direct3D permite a una aplicación aumentar el realismo de sus escenas mediante la representación de objetos poligonales segmentados (especialmente caracteres) que tienen uniones mezcladas sin problemas. Estos efectos se conocen a menudo como despejado. Para lograr este efecto, el sistema aplica matrices de transformación del mundo adicionales a un único conjunto de vértices para crear varios resultados y, a continuación, realiza una combinación lineal entre los vértices resultantes para crear un único conjunto de geometría para la representación. En la siguiente ilustración de un plátano se muestra este proceso.

![ilustración del proceso para combinar dos objetos con textura de textura de textura de textura](images/geometry-blend.png)

En la ilustración anterior se muestra cómo puede imaginar el proceso de mezcla de geometría. En una sola llamada de representación, el sistema toma los vértices del ingrediente, los transforma dos veces ( una vez sin modificación y otra con una rotación simple) y combina los resultados para crear un topo. El sistema combina la posición del vértice, así como el vértice normal cuando la iluminación está habilitada. Las aplicaciones no se limitan a dos rutas de acceso de combinación; Direct3D puede combinar geometría entre hasta cuatro matrices del mundo, incluida la matriz del mundo estándar, [**D3DTS \_ WORLD.**](d3dts-world.md)

> [!Note]
>
> Cuando se habilita la iluminación, las normales de vértice se transforman mediante una matriz de vista del mundo inversa correspondiente, ponderada de la misma manera que los cálculos de la posición del vértice. El sistema normaliza el vector normal resultante si el estado de representación NORMALIZENORMALS de D3DRS \_ está establecido en **TRUE.**

 

Sin la combinación de geometría, los modelos articulados dinámicos a menudo se representan en segmentos. Por ejemplo, considere un modelo 3D del arm humano. En la vista más sencilla, un arm tiene dos partes: el arm superior que se conecta al cuerpo y el arm inferior, que se conecta a la mano. Los dos están conectados en el reo, y el arm inferior gira en ese punto. Una aplicación que representa un arm podría conservar los datos de vértices para el arm superior e inferior, cada uno con una matriz de transformación world independiente. En el siguiente ejemplo código se muestra cómo hacerlo.


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

![ilustración de un objeto de manzana mezclada sin mezcla de geometría](images/noblend.png)

Las diferencias entre la geometría mezclada y la geometría no entrelazada son obvias. Este ejemplo es algo extremo. En una aplicación real, las uniones de los modelos segmentados están diseñadas para que las uniones no sean tan obvias. Sin embargo, las juntas son visibles en ocasiones, lo que presenta desafíos constantes para los diseñadores de modelos.

La combinación de geometría en Direct3D presenta una alternativa al escenario clásico de modelado segmentado. Sin embargo, la calidad visual mejorada de los objetos segmentados se produce a costa de los cálculos de combinación durante la representación. Para minimizar el impacto de estas operaciones adicionales, la canalización de geometría de Direct3D está optimizada para combinar geometría con la menor sobrecarga posible. Las aplicaciones que usan de forma inteligente los servicios de combinación de geometría que ofrece Direct3D pueden mejorar el realismo de sus caracteres, al tiempo que se evitan graves repercusiones en el rendimiento.

## <a name="blending-transform-and-render-states"></a>Combinar estados de transformación y representación

El [**método IDirect3DDevice9::SetTransform**](/windows/desktop/api) reconoce las macros [**D3DTS \_ WORLD**](d3dts-world.md) y [**D3DTS \_ WORLDn,**](d3dts-worldn.md) que corresponden a valores que se pueden definir mediante la macro [**\_ WORLDMATRIX de D3DTS.**](d3dts-worldmatrix.md) Estas macros se usan para identificar las matrices entre las que se combinará la geometría.

El [**tipo enumerado D3DRENDERSTATETYPE**](./d3drenderstatetype.md) incluye el estado de representación D3DRS VERTEXBLEND para habilitar y controlar la combinación \_ de geometría. Los valores válidos para este estado de representación se definen mediante el tipo enumerado [**D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) Si la mezcla de geometría está habilitada, el formato de vértice debe incluir el número adecuado de pesos de mezcla.

## <a name="blending-weights"></a>Mezclar pesos

Un peso de mezcla, a veces denominado peso beta, controla hasta qué punto una matriz mundial determinada afecta a un vértice. Las ponderaciones de mezcla son valores de punto flotante que oscilan entre 0,0 y 1,0, codificados en el formato de vértice, donde un valor de 0,0 significa que el vértice no se mezcla con esa matriz y 1,0 significa que el vértice se ve afectado en su totalidad por la matriz.

Los pesos de mezcla de geometría se codifican en el formato de vértice, que aparece inmediatamente después de la posición de cada vértice, como se describe en Códigos FVF de función fija [(Direct3D 9).](fixed-function-fvf-codes.md) Para comunicar el número de pesos de mezcla en formato de vértice, incluya una de las constantes FVF en la descripción del vértice que proporcione a los [métodos](d3dfvf.md) de representación.

El sistema realiza una mezcla lineal entre los resultados ponderados de las matrices de mezcla. La siguiente ecuación es la fórmula de combinación completa.

![ecuación de mezcla lineal, mediante matrices de transformación mundial](images/vert-blend-formula.png)

En la ecuación anterior, vBlend es el vértice de salida, los elementos v son los vértices producidos por la matriz mundial aplicada ([**D3DTS \_ WORLDn**](d3dts-worldn.md)). Los elementos W son los valores de peso correspondientes dentro del formato de vértice. Un vértice combinado entre n matrices puede tener - 1 valores de peso de mezcla, uno para cada matriz de mezcla, excepto el último. El sistema genera automáticamente el peso de la última matriz mundial para que la suma de todos los pesos sea 1,0, expresado aquí en notación sigma. Esta fórmula se puede simplificar para cada uno de los casos admitidos por Direct3D, que se muestra en las siguientes ecuaciones.

![ecuaciones de mezcla lineal para tres casos de mezcla](images/vert-blend-formulas-simple.png)

Estas son las formas simplificadas de la fórmula de combinación completa para los dos, tres y cuatro casos de matriz de mezcla.

> [!Note]  
> Aunque Direct3D incluye descriptores FVF para definir vértices que contienen hasta cinco pesos de mezcla, solo se pueden usar tres en esta versión de DirectX.

 

En los temas siguientes se incluye información adicional.

-   [Uso de geometry blending (Direct3D 9)](using-geometry-blending.md)
-   [Mezcla de vértices indexados (Direct3D 9)](indexed-vertex-blending.md)
-   [Interpolación de vértices (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 
