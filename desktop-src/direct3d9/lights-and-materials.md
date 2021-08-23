---
description: Las luces se usan para iluminar los objetos de una escena.
ms.assetid: 0751bb76-611a-41c4-aab2-aa6f68b61b0e
title: Luces y materiales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5ace2a80bb79d192fadc5376256eedf9229be9a36fa1d200341ccf28e961fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119277525"
---
# <a name="lights-and-materials-direct3d-9"></a>Luces y materiales (Direct3D 9)

Las luces se usan para iluminar los objetos de una escena. Cuando la iluminación está habilitada, Direct3D calcula el color de cada vértice de objeto en función de una combinación de:

> [!Note]  
> Esta sección es solo para la canalización de función fija. Los sombreadores programables realizan toda la iluminación explícitamente.

 

-   Color del material actual y los elementos de textura de un mapa de textura asociado.
-   Los colores difusos y especulares en el vértice, si se especifican.
-   El color y la intensidad de la luz que producen las fuentes de luz de la escena o el nivel de luz ambiental de la escena.

Cuando se usa iluminación y materiales de Direct3D, se permite que Direct3D controle los detalles de iluminación. Los usuarios avanzados pueden realizar la iluminación por sí mismos, si lo desean.

La forma de trabajar con la iluminación y los materiales marca una gran diferencia en la apariencia de la escena representada. Los materiales definen cómo se refleja la luz fuera de una superficie. Los niveles de luz directa y luz ambiental definen la luz que se refleja. Debe usar materiales para representar una escena si la iluminación está habilitada. Las luces no son necesarias para representar una escena, pero los detalles de una escena representados sin luz no son visibles. En el mejor de los casos, la representación de una escena sin iluminación da como resultado una combinación de los objetos de la escena. Esto no es suficientemente detallado para la mayoría de los propósitos.

## <a name="direct-light-vs-ambient-light"></a>Luz directa frente a luz ambiente

Aunque la luz directa y ambiental enciende los objetos de una escena, son independientes entre sí, tienen efectos muy diferentes y requieren que trabaje con ellos de maneras completamente diferentes.

La luz directa es simplemente eso: directa. La luz directa siempre tiene dirección y color, y es un factor para los algoritmos de sombreado, como el sombreado de Gouraud. Los distintos tipos de luces emiten luz directa de maneras diferentes, lo que crea efectos de atenuación especiales. Para crear un conjunto de parámetros claros para la luz directa, llame al [**método IDirect3DDevice9::SetLight.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)

La luz ambiental está efectivamente en todas partes de una escena. Puede pensarlo como un nivel general de luz que llena toda una escena, independientemente de los objetos y sus ubicaciones en esa escena. La luz ambiental no tiene posición ni dirección, solo color e intensidad. Cada luz agrega a la luz ambiental general de una escena. Establezca el nivel de luz ambiente con una llamada al método [**IDirect3DDevice9::SetRenderState,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) especificando D3DRS AMBIENT como parámetro State y el color RGBA deseado como parámetro \_ Value. 

El color claro ambiente toma la forma de un valor RGBA, donde cada componente es un valor entero de 0 a 255. Esto es diferente de la mayoría de los valores de color de Direct3D.

Puede usar la macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) para generar valores RGBA. Los componentes rojo, verde y azul se combinan para crear el color final de la luz ambiente. El componente alfa controla la transparencia del color. Cuando se usa la aceleración de hardware o la emulación RGB, se omite el componente alfa.

## <a name="direct3d-light-model-vs-nature"></a>Direct3D Light Model frente a Nature

Por naturaleza, cuando se emite luz desde un origen, se refleja en cientos, si no miles o millones de objetos antes de llegar al ojo del usuario. Cada vez que se refleja, una superficie ve alguna luz, otra se dispersa en direcciones aleatorias y el resto pasa a otra superficie o al ojo del usuario. Este proceso continúa hasta que la luz se reduce a nada o un usuario la percibe.

Obviamente, los cálculos necesarios para simular perfectamente el comportamiento natural de la luz son demasiado lentos para usarlos en gráficos direct3D en tiempo real. Por lo tanto, con la velocidad en mente, el modelo de luz de Direct3D se aproxima a la forma en que funciona la luz en el mundo natural. Direct3D describe la luz en términos de componentes rojos, verdes y azules que se combinan para crear un color final.

En Direct3D, cuando la luz se refleja fuera de una superficie, el color claro interactúa matemáticamente con la propia superficie para crear el color que finalmente se muestra en la pantalla. Para obtener información específica sobre los algoritmos que usa Direct3D, vea Matemáticas de iluminación [(Direct3D 9).](mathematics-of-lighting.md)

El modelo de luz de Direct3D generaliza la luz en dos tipos: luz ambiente y luz directa. Cada uno tiene atributos diferentes y cada uno interactúa con el material de una superficie de maneras diferentes. La luz ambiental es una luz que se ha disperso tanto que su dirección y origen son indeterminados: mantiene un bajo nivel de intensidad en todas partes. La iluminación indirecta que usan los revendedores es un buen ejemplo de luz ambiental. La luz ambiental en Direct3D, como en la naturaleza, no tiene ninguna dirección ni origen reales, solo un color e intensidad. De hecho, el nivel de luz ambiental es completamente independiente de los objetos de una escena que generan luz. La luz ambiental no contribuye a la reflexión especular.

La luz directa es la luz generada por un origen dentro de una escena. siempre tiene color e intensidad, y viaja en una dirección especificada. La luz directa interactúa con el material de una superficie para crear resaltados especulares y su dirección se usa como factor en los algoritmos de sombreado, incluido el sombreado de Gouraud. Cuando se refleja la luz directa, no contribuye al nivel de luz ambiente de una escena. Los orígenes de una escena que generan luz directa tienen características diferentes que afectan a la forma en que encienden una escena.

Además, el material de un polígono tiene propiedades que afectan a la forma en que ese polígono refleja la luz que recibe. Se establece un único rasgo de reflectancia que describe cómo el material refleja la luz ambiente y se establecen rasgos individuales para determinar la reflectancia especular y difuso del material. Para obtener más información, [vea Materiales (Direct3D 9).](materials.md)

## <a name="color-values-for-lights-and-materials"></a>Valores de color para luces y materiales

Direct3D describe el color en términos de cuatro componentes(rojo, verde, azul y alfa) que se combinan para crear un color final. La [**estructura D3DCOLORVALUE**](d3dcolorvalue.md) de C++ se define para contener valores para cada componente. Cada miembro es un valor de punto flotante que normalmente oscila entre 0,0 y 1,0, ambos incluidos. Aunque tanto las luces como los materiales usan la misma estructura para describir el color, cada uno usa los valores de la estructura de forma un poco diferente.

Los valores de color de las fuentes de luz representan la cantidad de un componente de luz determinado que emite. Dado que las luces no usan un componente alfa, solo son pertinentes los componentes rojo, verde y azul del color. Puede visualizar los tres componentes como las lentes roja, verde y azul en una televisión de proyección. Cada lente podría estar desactivada (un valor de 0,0 en el miembro adecuado), podría ser lo más brillante posible (un valor de 1,0) o podría ser un nivel entre medio. Los colores que llegan a través de las lentes se combinan para crear el color final de la luz. Una combinación como R(1.0), G(1.0), B(1.0) crea una luz blanca, donde R(0.0), G(0.0), B(0.0) no emite ninguna luz. Puede crear una luz que emita solo un componente, lo que da como resultado una luz roja, verde o azul pura; o bien, la luz podría usar combinaciones para emitir colores como amarillo o púrpura. Incluso puede establecer valores de componente de color negativos para crear una "luz oscura" que realmente quite la luz de una escena. O bien, puede establecer los componentes en un valor superior a 1,0 para crear una luz extremadamente brillante.

Por otro lado, con los materiales, los valores de color representan la cantidad de un componente claro reflejado por una superficie que se representa con ese material. Un material cuyos componentes de color son R(1.0), G(1.0), B(1.0), A(1.0) refleja toda la luz que viene por su camino. Del mismo modo, un material con R(0.0), G(1.0), B(0.0), A(1.0) refleja toda la luz verde que se dirige a él. Los materiales tienen varios valores de reflectancia para crear varios tipos de efectos.

Encontrará información adicional en: [Tipos de luz (Direct3D 9)](light-types.md)y Propiedades de luz [(Direct3D 9).](light-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
