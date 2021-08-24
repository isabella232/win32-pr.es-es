---
description: Las propiedades de luz describen el tipo y el color de una fuente de luz.
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: Propiedades ligeras (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14c3e815401fe0b35c7409dec783515de5c3422ac92d6aed6fd4adebf09f8c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747005"
---
# <a name="light-properties-direct3d-9"></a>Propiedades ligeras (Direct3D 9)

Las propiedades de luz describen el tipo y el color de una fuente de luz. Dependiendo del tipo de luz que se usa, una luz puede tener propiedades para atenuación e intervalo, o para efectos destacados. Pero no todos los tipos de luces usan todas las propiedades. Direct3D usa la [**estructura D3DLIGHT9**](d3dlight9.md) para llevar información sobre las propiedades de luz de todos los tipos de fuentes de luz. Esta sección contiene información para todas las propiedades ligeras. La información se divide en los siguientes grupos.

Las propiedades de posición, rango y atenuación definen la ubicación de una luz en el espacio mundial y cómo se comporta la luz que emite a lo largo de la distancia. Al igual que con todas las propiedades ligeras que se usan en C++, estas se encuentran en la estructura [**D3DLIGHT9**](d3dlight9.md) de una luz.

-   [Atenuación de luz](#light-attenuation)
-   [Color claro](#light-color)
-   [Dirección de la luz](#light-direction)
-   [Posición ligera](#light-position)
-   [Intervalo de luz](#light-range)

## <a name="light-attenuation"></a>Atenuación de luz

La atenuación controla cómo disminuye la intensidad de una luz hacia la distancia máxima especificada por la propiedad range. Tres [**miembros de la estructura D3DLIGHT9**](d3dlight9.md) representan la atenuación de luz: Atenuación0, Atenuación1 y Atenuación2. Estos miembros contienen valores de punto flotante que van desde 0,0 hasta el infinito, controlando la atenuación de una luz. Algunas aplicaciones establecen el miembro Atenuación1 en 1.0 y las otras en 0.0, lo que da lugar a una intensidad de luz que cambia como 1/D, donde D es la distancia desde la fuente de luz al vértice. La intensidad de la luz máxima está en el origen, disminuyendo a 1/ (intervalo de luz) en el intervalo de la luz. Normalmente, una aplicación establece Atenuación0 en 0,0, Atenuación1 en un valor constante y Atenuación2 en 0,0.

Puede combinar valores de atenuación para obtener efectos de atenuación más complejos. O bien, puede establecerlos en valores fuera del intervalo normal para crear incluso efectos de atenuación de atenuación. Sin embargo, no se permiten valores de atenuación negativos. Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)

## <a name="light-color"></a>Color claro

Las luces de Direct3D emiten tres colores que se usan de forma independiente en los cálculos de iluminación del sistema: un color difuso, un color ambiente y un color especular. Cada uno se incorpora mediante el módulo de iluminación de Direct3D, que interactúa con un homólogo del material actual, para generar un color final utilizado en la representación. El color difuso interactúa con la propiedad de reflectancia difusa del material actual, el color especular con la propiedad de reflectancia especular del material, y así sucesivamente. Para obtener información específica sobre cómo Aplica Direct3D estos colores, vea Matemáticas de iluminación [(Direct3D 9).](mathematics-of-lighting.md)

En una aplicación de C++, la estructura [**D3DLIGHT9**](d3dlight9.md) incluye tres miembros para estos colores :Difuso, Ambiente y Especular; cada uno es una estructura [**D3DCOLORVALUE**](d3dcolorvalue.md) que define el color que se emite.

El tipo de color que se aplica en mayor medida a los cálculos del sistema es el color difuso. El color difuso más común es el blanco (R:1.0 G:1.0 B:1.0), pero puede crear colores según sea necesario para lograr los efectos deseados. Por ejemplo, podría usar una luz roja para una iluminación, o bien podría usar una luz verde para una señal de tráfico establecida en "Go".

Por lo general, los componentes de color claro se establecen en valores entre 0,0 y 1,0, ambos incluidos, pero esto no es un requisito. Por ejemplo, podría establecer todos los componentes en 2.0, creando una luz que sea "más brillante que blanca". Este tipo de configuración puede ser especialmente útil cuando se usa una configuración de atenuación que no sea constante.

Tenga en cuenta que aunque Direct3D usa valores RGBA para las luces, no se usa el componente de color alfa.

Normalmente, los colores de material se usan para la iluminación. Sin embargo, puede especificar que los colores de material (emissive, ambient, difuso y specular) se invaliden por colores de vértice difusos o especulares. Para ello, llame a [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y establezca las variables de estado del dispositivo enumeradas en la tabla siguiente.



| Variable de estado del dispositivo         | Significado                                       | Tipo                   | Valor predeterminado          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| D3DRS \_ AMBIENTMATERIALSOURCE  | Define dónde obtener el color del material ambiente.  | D3DMATERIALCOLORSOURCE | MATERIAL de D3DMCS \_ |
| D3DRS \_ DIFFUSEMATERIALSOURCE  | Define dónde obtener el color del material difuso.  | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR1   |
| D3DRS \_ SPECULARMATERIALSOURCE | Define dónde obtener el color del material especular. | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR2   |
| D3DRS \_ EMISSIVEMATERIALSOURCE | Define dónde obtener el color del material emisivo. | D3DMATERIALCOLORSOURCE | MATERIAL de D3DMCS \_ |
| D3DRS \_ COLORVERTEX            | Deshabilita o habilita el uso de colores de vértice.     | BOOL                   | TRUE             |



 

El valor alfa/transparencia siempre procede únicamente del canal alfa del color difuso.

El valor de la paleta siempre procede únicamente del canal alfa del color especular.

D3DMATERIALCOLORSOURCE puede tener los siguientes valores.

-   MATERIAL de D3DMCS: \_ el color del material se usa como origen.
-   D3DMCS \_ COLOR1: el color de vértice difuso se usa como origen.
-   D3DMCS \_ COLOR2: el color del vértice especular se usa como origen.

## <a name="light-direction"></a>Dirección de la luz

La propiedad de dirección de una luz determina la dirección en la que viaja la luz emitida por el objeto, en el espacio mundial. La dirección solo la usan las luces direccionales y los focos, y se describe con un vector.

Establezca la dirección de la luz en el miembro Direction de la estructura [**D3DLIGHT9 de la**](d3dlight9.md) luz. El miembro Direction es de [**tipo D3DVECTOR.**](d3dvector.md) Los vectores de dirección se describen como distancias desde un origen lógico, independientemente de la posición de la luz en una escena. Por lo tanto, un foco que apunta directamente a una escena (a lo largo del eje Z positivo) tiene un vector de dirección de <0,0,1> independientemente de dónde esté definida su posición. De forma similar, puede simular el contraluz de la escena directamente mediante una luz direccional cuya dirección es <0,-1,0>. Obviamente, no tiene que crear luces que se deslucen a lo largo de los ejes de coordenadas. puede mezclar y combinar valores para crear luces que se deslucen en ángulos más interesantes.

> [!Note]  
> Aunque no es necesario normalizar el vector de dirección de una luz, asegúrese siempre de que tiene magnitud. En otras palabras, no use un vector <0,0,0> dirección.

 

## <a name="light-position"></a>Posición ligera

La posición ligera se describe mediante una [**estructura D3DVECTOR**](d3dvector.md) en el miembro Position de la [**estructura D3DLIGHT9.**](d3dlight9.md) Se supone que las coordenadas x, y y z están en el espacio mundial. Las luces direccionales son el único tipo de luz que no usa la propiedad position.

## <a name="light-range"></a>Intervalo de luz

La propiedad range de una luz determina la distancia, en el espacio mundial, en la que las mallas de una escena ya no reciben la luz emitida por ese objeto. El miembro Range contiene un valor de punto flotante que representa el intervalo máximo de la luz, en el espacio mundial. Las luces direccionales no usan la propiedad range.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Luces y materiales](lights-and-materials.md)
</dt> </dl>

 

 
