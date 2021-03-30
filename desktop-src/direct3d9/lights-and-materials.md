---
description: Las luces se usan para iluminar los objetos de una escena.
ms.assetid: 0751bb76-611a-41c4-aab2-aa6f68b61b0e
title: Luces y materiales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f44a12c1be1e7a14f7bfe176d7f391901d2dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422750"
---
# <a name="lights-and-materials-direct3d-9"></a>Luces y materiales (Direct3D 9)

Las luces se usan para iluminar los objetos de una escena. Cuando se habilita la iluminación, Direct3D calcula el color de cada vértice del objeto en función de una combinación de:

> [!Note]  
> Esta sección es solo para la canalización de funciones fijas. Los sombreadores programables realizan toda la iluminación explícitamente.

 

-   El color del material actual y el textura de un mapa de texturas asociado.
-   Colores difusos y especulares en el vértice, si se especifican.
-   El color y la intensidad de la luz producidos por las fuentes luminosas de la escena o el nivel de luz ambiente de la escena.

Al usar la iluminación y los materiales de Direct3D, permite que Direct3D controle los detalles de la iluminación. Los usuarios avanzados pueden realizar la iluminación por sí solos, si lo desea.

La forma de trabajar con la iluminación y los materiales hace una gran diferencia en la apariencia de la escena representada. Los materiales definen cómo se refleja la luz en una superficie. Los niveles de luz directa y de luz ambiente definen la luz que se refleja. Debe usar materiales para representar una escena si está habilitada la iluminación. No se necesitan luces para representar una escena, pero los detalles de una escena representada sin luz no son visibles. Como mejor, la representación de una escena de sin iluminación da como resultado una silueta de los objetos de la escena. Esto no es suficiente para la mayoría de los propósitos.

## <a name="direct-light-vs-ambient-light"></a>Luz directa frente a luz ambiente

Aunque la luz directa y ambiente iluminan objetos en una escena, son independientes entre sí, tienen efectos muy diferentes y requieren que trabaje con ellos de maneras completamente diferentes.

Direct Light es justamente eso: Direct. Direct Light siempre tiene la dirección y el color, y es un factor para los algoritmos de sombreado, como el sombreado Gouraud. Los diferentes tipos de luces emiten luz directa de maneras diferentes, lo que crea efectos de atenuación especiales. Puede crear un conjunto de parámetros de luz para la luz directa llamando al método [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight) .

La luz ambiente es eficaz en cualquier parte de una escena. Puede considerarse como un nivel general de luz que rellena toda una escena, independientemente de los objetos y sus ubicaciones en esa escena. La luz ambiente no tiene posición ni dirección, solo el color y la intensidad. Cada luz se agrega a la luz ambiente global de una escena. Establezca el nivel de luz ambiente con una llamada al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) , especificando D3DRS \_ ambiente como el parámetro de *Estado* y el color RGBA deseado como parámetro de valor.

El color de luz ambiente adopta la forma de un valor RGBA, donde cada componente es un valor entero comprendido entre 0 y 255. Esto no es lo mismo que la mayoría de los valores de color de Direct3D.

Puede usar la macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) para generar valores RGBA. Los componentes rojo, verde y azul se combinan para crear el color final de la luz ambiente. El componente alfa controla la transparencia del color. Cuando se usa la aceleración de hardware o la emulación de RGB, se omite el componente alfa.

## <a name="direct3d-light-model-vs-nature"></a>Modelo de Direct3D Light frente a naturaleza

Por naturaleza, cuando se emite Light desde un origen, se refleja en cientos, si no miles o millones de objetos antes de llegar al ojo del usuario. Cada vez que se refleja, algunas luces se absorben por una superficie, algunas están dispersas en direcciones aleatorias y el resto se dirige a otra superficie o al ojo del usuario. Este proceso continúa hasta que la luz se reduce a nada o el usuario percibe la luz.

Obviamente, los cálculos necesarios para simular perfectamente el comportamiento natural de Light son demasiado lentos para usarlos en los gráficos de Direct3D en tiempo real. Por lo tanto, teniendo en cuenta la velocidad, el modelo de Direct3D Light se aproxima a la manera en que funciona la luz en el mundo natural. Direct3D describe la luz en términos de componentes rojo, verde y azul que se combinan para crear un color final.

En Direct3D, cuando la luz se refleja fuera de una superficie, el color claro interactúa matemáticamente con la propia superficie para crear el color que se muestra en la pantalla. Para obtener información específica sobre los algoritmos que usa Direct3D, vea [matemáticas de iluminación (Direct3D 9)](mathematics-of-lighting.md).

El modelo Direct3D Light generaliza la luz en dos tipos: luz ambiente y luz directa. Cada una tiene atributos diferentes, y cada interactúa con el material de una superficie de maneras diferentes. La luz ambiente es una luz que se ha disperso, de modo que su dirección y origen son indeterminados: mantiene un nivel bajo de intensidad en todo el mundo. La iluminación indirecta utilizada por los fotógrafos es un buen ejemplo de luz ambiente. Luz ambiente en Direct3D, como por naturaleza, no tiene ninguna dirección o origen real, solo un color e intensidad. De hecho, el nivel de luz ambiente es completamente independiente de los objetos de una escena que generan luz. La luz ambiente no contribuye a la reflexión especular.

Direct Light es la luz generada por un origen dentro de una escena. siempre tiene color e intensidad y se desplaza en una dirección especificada. Direct Light interactúa con el material de una superficie para crear reflejos especulares y su dirección se usa como un factor en los algoritmos de sombreado, incluido el sombreado Gouraud. Cuando se refleja la luz directa, no contribuye al nivel de luz ambiente en una escena. Los orígenes de una escena que generan luz directa tienen características diferentes que afectan al modo en que iluminan una escena.

Además, el material de un polígono tiene propiedades que afectan al modo en que ese polígono refleja la luz que recibe. Establezca un rasgo de reflectancia único que describa cómo refleja el material la luz ambiente y establezca rasgos individuales para determinar la reflexión especular y difusa del material. Para obtener más información, vea [materiales (Direct3D 9)](materials.md).

## <a name="color-values-for-lights-and-materials"></a>Valores de color para las luces y los materiales

Direct3D describe el color en términos de cuatro componentes (rojo, verde, azul y alfa) que se combinan para crear un color final. La estructura de C++ de [**D3DCOLORVALUE**](d3dcolorvalue.md) se define para que contenga valores para cada componente. Cada miembro es un valor de punto flotante que suele oscilar entre 0,0 y 1,0, ambos incluidos. Aunque tanto las luces como los materiales utilizan la misma estructura para describir el color, cada uno de los valores de la estructura se utiliza de forma ligeramente diferente.

Los valores de color de las fuentes de luz representan la cantidad de un componente de luz determinado que emite. Dado que las luces no usan un componente alfa, solo son relevantes los componentes rojo, verde y azul del color. Puede visualizar los tres componentes como los lentes rojo, verde y azul en un televisor de proyección. Es posible que cada lente esté desactivada (un valor de 0,0 en el miembro adecuado), podría ser tan brillante como sea posible (un valor de 1,0) o podría ser un cierto nivel entre. Los colores que entran en los objetivos se combinan para crear el color final de la luz. Una combinación como R (1.0), G (1.0), B (1.0) crea una luz blanca, donde R (0,0), G (0,0), B (0,0) no emite luz en absoluto. Puede crear una luz que emita un solo componente, lo que dará lugar a una luz roja, verde o azul pura; o bien, la luz podría usar combinaciones para emitir colores como amarillo o púrpura. Incluso puede establecer valores de componentes de color negativos para crear una "luz oscura" que realmente quita la luz de una escena. O bien, puede establecer los componentes en un valor superior a 1,0 para crear una luz muy brillante.

Por otro lado, con materiales, los valores de color representan la cantidad de un componente de luz que se refleja en una superficie que se representa con ese material. Un material cuyos componentes de color son R (1.0), G (1.0), B (1.0), A (1,0) refleja toda la luz que llega A su camino. Del mismo modo, un material con R (0,0), G (1.0), B (0,0), A (1,0) refleja toda la luz verde que se dirige a él. Los materiales tienen varios valores de reflectancia para crear varios tipos de efectos.

Se incluye información adicional en: [tipos de luz (Direct3D 9)](light-types.md)y [propiedades de luz (Direct3D 9)](light-properties.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
