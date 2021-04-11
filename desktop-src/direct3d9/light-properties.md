---
description: Las propiedades de luz describen el tipo y el color de una fuente luminosa.
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: Propiedades de la luz (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63239024109327e483ff93c2ee29fe42fc22c922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152166"
---
# <a name="light-properties-direct3d-9"></a>Propiedades de la luz (Direct3D 9)

Las propiedades de luz describen el tipo y el color de una fuente luminosa. Dependiendo del tipo de luz que se esté usando, una luz puede tener propiedades de atenuación e intervalo, o de efectos destacados. Pero no todos los tipos de luces utilizan todas las propiedades. Direct3D usa la estructura [**D3DLIGHT9**](d3dlight9.md) para llevar información sobre las propiedades claras de todos los tipos de fuentes de luz. Esta sección contiene información de todas las propiedades de la luz. La información se divide en los siguientes grupos.

Las propiedades posición, rango y atenuación definen la ubicación de una luz en el espacio universal y cómo se comporta la luz con la distancia. Como con todas las propiedades de la luz que se usan en C++, se encuentran en la estructura [**D3DLIGHT9**](d3dlight9.md) de una luz.

-   [Atenuación de luz](#light-attenuation)
-   [Color claro](#light-color)
-   [Dirección de la luz](#light-direction)
-   [Posición de la luz](#light-position)
-   [Intervalo claro](#light-range)

## <a name="light-attenuation"></a>Atenuación de luz

La atenuación controla cómo se reduce la intensidad de una luz hacia la distancia máxima especificada por la propiedad de intervalo. Tres miembros de la estructura [**D3DLIGHT9**](d3dlight9.md) representan la atenuación de la luz: Attenuation0, Attenuation1 y Attenuation2. Estos miembros contienen valores de punto flotante que van de 0,0 a infinito y controlan la atenuación de una luz. Algunas aplicaciones establecen el miembro Attenuation1 en 1,0 y los demás en 0,0, lo que da lugar a una intensidad de luz que cambia como 1/D, donde D es la distancia desde la fuente de luz hasta el vértice. La intensidad de luz máxima está en el origen, decreciente en 1/(intervalo claro) en el intervalo de la luz. Normalmente, una aplicación establece Attenuation0 en 0,0, Attenuation1 en un valor constante y Attenuation2 en 0,0.

Puede combinar valores de atenuación para obtener efectos de atenuación más complejos. O bien, puede establecerlos en valores fuera del intervalo normal para crear incluso efectos de atenuación no extraño. Sin embargo, no se permiten valores de atenuación negativos. Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).

## <a name="light-color"></a>Color claro

Las luces de Direct3D emiten tres colores que se usan de forma independiente en los cálculos de iluminación del sistema: un color difuso, un color ambiente y un color especular. Cada uno de ellos lo incorpora el módulo de iluminación de Direct3D, que interactúa con un homólogo del material actual, para generar un color final usado en la representación. El color difuso interactúa con la propiedad de reflectancia difusa del material actual, el color especular con la propiedad de reflexión especular del material, etc. Para obtener información específica sobre cómo Direct3D aplica estos colores, vea [matemáticas de iluminación (Direct3D 9)](mathematics-of-lighting.md).

En una aplicación de C++, la estructura [**D3DLIGHT9**](d3dlight9.md) incluye tres miembros para estos colores: difuso, ambiente e especular; cada uno es una estructura [**D3DCOLORVALUE**](d3dcolorvalue.md) que define el color que se va a emitir.

El tipo de color que se aplica más a los cálculos del sistema es el color difuso. El color difuso más común es blanco (R:1.0 G:1.0 B:1.0), pero puede crear colores según sea necesario para lograr los efectos deseados. Por ejemplo, podría usar la luz roja para un Fireplace o podría usar la luz verde para una señal de tráfico establecida en "Go".

Por lo general, los componentes de color claro se establecen en valores entre 0,0 y 1,0, ambos incluidos, pero no es un requisito. Por ejemplo, puede establecer todos los componentes en 2,0, creando una luz que sea "más brillante que el blanco". Este tipo de configuración puede ser especialmente útil cuando se usa una configuración de atenuación distinta de Constant.

Tenga en cuenta que, aunque Direct3D usa valores RGBA para las luces, no se usa el componente de color alfa.

Normalmente, los colores de material se utilizan para la iluminación. Sin embargo, puede especificar que los colores de material (emisor, ambiente, difuso y especular) se invaliden con los colores de vértice difuso o especular. Esto se realiza mediante una llamada a [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y el establecimiento de las variables de estado de dispositivo que se muestran en la tabla siguiente.



| Variable de estado de dispositivo         | Significado                                       | Tipo                   | Valor predeterminado          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| D3DRS \_ AMBIENTMATERIALSOURCE  | Define dónde obtener el color del material ambiente.  | D3DMATERIALCOLORSOURCE | \_Material D3DMCS |
| D3DRS \_ DIFFUSEMATERIALSOURCE  | Define dónde obtener el color de material difuso.  | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR1   |
| D3DRS \_ SPECULARMATERIALSOURCE | Define dónde obtener el color del material especular. | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR2   |
| D3DRS \_ EMISSIVEMATERIALSOURCE | Define dónde obtener el color del material de emisor. | D3DMATERIALCOLORSOURCE | \_Material D3DMCS |
| D3DRS \_ COLORVERTEX            | Deshabilita o habilita el uso de colores de vértices.     | BOOL                   | TRUE             |



 

El valor de alfa/transparencia siempre viene únicamente del canal alfa del color difuso.

El valor de niebla siempre viene solo del canal alfa del color especular.

D3DMATERIALCOLORSOURCE puede tener los siguientes valores.

-   D3DMCS \_ material: el color del material se utiliza como origen.
-   D3DMCS \_ COLOR1: el color de vértice difuso se utiliza como origen.
-   D3DMCS \_ COLOR2: el color de vértice especular se utiliza como origen.

## <a name="light-direction"></a>Dirección de la luz

La propiedad direction de una luz determina la dirección en la que viaja la luz que emite el objeto, en el espacio universal. La dirección solo se usa en las luces direccionales y en los focos, y se describe con un vector.

Establezca la dirección de la luz en el miembro Direction de la estructura [**D3DLIGHT9**](d3dlight9.md) de la luz. El miembro Direction es de tipo [**D3DVECTOR**](d3dvector.md). Los vectores de dirección se describen como Distancias desde un origen lógico, independientemente de la posición de la luz en una escena. Por lo tanto, un foco que apunta directamente a una escena a lo largo del eje z positivo, tiene un vector de dirección de <0, 0, 1> sin importar dónde se define su posición. Del mismo modo, puede simular la luz solar directamente en una escena usando una luz direccional cuya dirección es <0,-1, 0>. Obviamente, no tiene que crear luces que destaquen a lo largo de los ejes de coordenadas. puede mezclar y hacer coincidir los valores para crear las luces que destacan en ángulos más interesantes.

> [!Note]  
> Aunque no es necesario normalizar el vector de dirección de una luz, asegúrese siempre de que tenga magnitud. En otras palabras, no utilice un vector de dirección <0, 0,0>.

 

## <a name="light-position"></a>Posición de la luz

La posición de la luz se describe mediante una estructura [**D3DVECTOR**](d3dvector.md) en el miembro Position de la estructura [**D3DLIGHT9**](d3dlight9.md) . Se supone que las coordenadas x, y y z están en el espacio universal. Las luces direccionales son el único tipo de luz que no usan la propiedad Position.

## <a name="light-range"></a>Intervalo claro

La propiedad de intervalo de una luz determina la distancia, en el espacio universal, a la que las mallas de una escena ya no reciben luz emitida por ese objeto. El miembro del intervalo contiene un valor de punto flotante que representa el intervalo máximo de la luz, en el espacio universal. Las luces direccionales no usan la propiedad Range.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Luces y materiales](lights-and-materials.md)
</dt> </dl>

 

 
