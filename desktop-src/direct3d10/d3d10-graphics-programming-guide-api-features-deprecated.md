---
description: Aquí encontrará una lista de las características disponibles en Direct3D 10. En esta página se enumeran las características de Direct3D 9 que ya no se admiten en Direct3D 10.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Características en desuso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ce1750e6d8f98785bf87fb92169e56f0b4ca4e8a6dfdd34c6174a8c3087eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852775"
---
# <a name="deprecated-features-direct3d-10"></a>Características en desuso (Direct3D 10)

Aquí encontrará una lista de las características [](d3d10-graphics-programming-guide-api-features.md)disponibles en Direct3D 10. En esta página se enumeran las características de Direct3D 9 que ya no se admiten en Direct3D 10.

Los cambios más importantes en las características de Direct3D 10 son:

- Direct3D 10 ya no admite la canalización de iluminación y transformación de función fija.
- Direct3D 10 ya no admite la mezcla de textura de función fija (a veces denominada sombreador de píxeles de función fija).
- Direct3D 10 implementa nuevas reglas de rasterización, que son más sencillas y más claras que las reglas GDI heredadas que se implementan en Direct3D 9. Por ejemplo, ya no se admite el control de último píxel para las líneas.

Esta es una lista completa de las características de Direct3D 9 que han quedado en desuso en Direct3D 10.

- **Combinación alfa**. La mezcla alfa ahora está programada independientemente de la combinación de colores. Direct3D 10 agrega un botón de alternancia alfa-blend-enable que está habilitado de forma predeterminada. Vea [Objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obtener más información.
- **Prueba alfa**. La prueba alfa es un comportamiento de píxeles de función fija para Direct3D 9. La prueba alfa se mueve a sombreadores de píxeles programables para Direct3D 10 y superiores. Para obtener información sobre cómo emular la funcionalidad de prueba alfa de Direct3D 9 en Direct3D 10 y posteriores, consulte el ejemplo FixedFuncEMU en el SDK de DirectX para junio [de 2010.](https://www.microsoft.com/download/en/details.aspx?id=6812)
- **Opciones del modo blend**. BOTHSRCALPHA se ha quitado de BLEND D3D10, ya que es \_ redundante con BOTHINVSRCALPHA. Vea [**D3D10 \_ BLEND para**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) obtener más información.
- **Formatos de compresión de bloques**. No hay distinción entre alfa multiplicado previamente o alfa no multiplicado previamente en Direct3D 10. Estos formatos de Direct3D 9 se asignan a estos formatos de Direct3D 10: 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2,DXT3  | BC2\*       |
    | DXT4,DXT5  | BC3\*       |

    

     

    Consulte [Compresión de bloques (Direct3D 10)](d3d10-graphics-programming-guide-resources-block-compression.md) para obtener información adicional.

-   **Recortar planos**. En lugar de usar planos de recorte, Direct3D 10 implementa distancias de recorte y distancias cull, con hasta 8 componentes cada uno en hasta 2 elementos de atributos de vértice. Consulte [Semántica (HLSL de DirectX)](../direct3dhlsl/dx-graphics-hlsl-semantics.md) para obtener información adicional. [El ejemplo FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) proporciona un ejemplo de emulación de planos de clip en Direct3D 10.
-   **Dithering**. Direct3D 10 no admite la escritura de datos entreteados en un destino de representación.
-   **Transformación de función fija e canalización de iluminación en no disponible.** En su lugar, debe usar sombreadores. Vea [Shader Stages (Direct3D 10) (Fases del sombreador [Direct3D 10])](/previous-versions//bb205146(v=vs.85)) para obtener información adicional.
-   **Blender de textura de función fija (también denominado sombreador de píxeles de función fija).** En su lugar, debe usar sombreadores. Vea [Shader Stages (Direct3D 10) (Fases del sombreador [Direct3D 10])](/previous-versions//bb205146(v=vs.85)) para obtener información adicional.
-   **Los modos de** relleno han cambiado. Direct3D 10 implementa los modos de relleno sólido y de trama de conexión. Se ha quitado el punto D3DFILLMODE, use un sombreador de geometría para emular el modo de punto si es necesario. [El ejemplo FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) proporciona un ejemplo de emulación del punto D3DFILLMODE en Direct3D 10. Vea [**D3D10 \_ FILL MODE \_ y**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) [Shader Stages (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obtener información adicional.
-   **Da formato a**. El hardware puede usar formatos expuestos por la API. Los formatos de luminosidad ya no se implementan.
-   **Filtrado de mipmap**. Se ha quitado la opción para seleccionar el modo sin filtro. En su lugar, use una textura con un solo mapa mipmap o establezca el estado del muestreador MaxLOD en 0. Vea [Objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obtener información adicional.
-   **Paletas**. En su lugar, las aplicaciones deben usar una lectura de textura dependiente.
-   **Modelos de sombreador de píxeles y vértices:** 1 \_ x, 2 \_ x y 3 \_ 0. Direct3D 10 admite el modelo de sombreador 4. Vea [Shader Model 4 (Modelo de sombreador 4)](../direct3dhlsl/dx-graphics-hlsl-sm4.md) para obtener información adicional.
-   **Sprites de punto**. En su lugar, use un sombreador de geometría. Vea [Shader Stages (Direct3D 10) (Fases del sombreador [Direct3D 10])](/previous-versions//bb205146(v=vs.85)) para obtener información adicional.
-   **Reglas de rasterización**. Las reglas de rasterización de línea GDI heredadas se reemplazan por reglas más claras y sencillas. Ya no se admite el control de último píxel para las líneas. Consulte [Reglas de rasterización (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) para obtener información adicional.
-   **Modos de sombreado.** D3DSHADEMODE (que admite el sombreado flat/gouraud/phong) se ha quitado. Direct3D 10 implementa dos modificadores de interpolación para las salidas del sombreador de vértices en su lugar. Consulte [el ejemplo FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) para obtener un ejemplo de emulación de los modos de gouraud y sombreado plano de Direct3D 9 en Direct3D 10.
-   **Instrucción texldp.** Una aplicación debe implementar una carga de textura proyectada con instrucciones HLSL adicionales. Vea [Referencia de HLSL para](../direct3dhlsl/dx-graphics-hlsl-reference.md) obtener información adicional. [El ejemplo FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) proporciona un ejemplo de emulación de texldp en Direct3D 10.
-   **Ya no se admite el** estado de la fase de textura del índice de coordenadas de textura (TCI) (D3DTSS \_ TEXCOORDINDEX).
-   **Ventiladores de triángulo**. Una aplicación debe convertir los triángulos-ventiladores existentes en listas de triángulos o franjas de triángulo. Para emular algunos comportamientos mediante DrawPrimitive en API anteriores, pruebe a usar DrawIndexed en Direct3D 10. Vea [Primitive Topologies (Direct3D 10) (Topologías primitivas [Direct3D 10])](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) para obtener información adicional.
-   **W almacena en búfer**. No se garantiza la compatibilidad con hardware; Se recomienda que una aplicación use búferes de profundidad de alta precisión en su lugar. Consulte [Configuring Depth-Stencil Functionality (Direct3D 10) (Configuración](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) de la funcionalidad de Depth-Stencil (Direct3D 10) para obtener información adicional.
-   **Modos de ajuste** (ajuste de coordenadas de textura). El ajuste de direcciones de textura (como encapsulado, reflejo, fijación, etc.) todavía existe. Vea [**D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) y [**D3D10 \_ TEXTURE ADDRESS \_ \_ MODE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
