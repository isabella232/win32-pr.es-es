---
description: Aquí se muestra una lista de las características disponibles en Direct3D 10. En esta página se enumeran las características de Direct3D 9 que ya no se admiten en Direct3D 10.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Características desusadas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66b6fe5092427cd66876ab5f6e1d7aaf83f0880
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153062"
---
# <a name="deprecated-features-direct3d-10"></a>Características desusadas (Direct3D 10)

[Aquí](d3d10-graphics-programming-guide-api-features.md)se muestra una lista de las características disponibles en Direct3D 10. En esta página se enumeran las características de Direct3D 9 que ya no se admiten en Direct3D 10.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Los principales cambios en las características de Direct3D 10 son:<br/> Direct3D 10 ya no admite la canalización de transformación de función fija y de iluminación.<br/> Direct3D 10 ya no admite el mezclador de textura de función fija (a veces denominado sombreador de píxeles de función fija).<br/> Direct3D 10 implementa nuevas reglas de rasterización, que son más sencillas y limpias que las reglas de GDI heredadas que se implementan en Direct3D 9. Por ejemplo, ya no se admite el control de último píxel para las líneas.<br/> |



 

Esta es una lista completa de las características de Direct3D 9 que han quedado en desuso en Direct3D 10.

-   **Alpha Blend**. Alpha Blend se programa ahora de forma independiente de Blend de color. Direct3D 10 agrega un control de alternancia Alpha-Blend-enable que está habilitado de forma predeterminada. Vea [objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obtener más información.
-   **Prueba alfa**. La prueba alfa es un comportamiento de píxeles de función fija para Direct3D 9. La prueba alfa se mueve a los sombreadores de píxeles programables para Direct3D 10 y versiones posteriores. Para obtener información sobre la emulación de la funcionalidad de prueba alfa de Direct3D 9 en Direct3D 10 y versiones posteriores, consulte el ejemplo de FixedFuncEMU en el [SDK de DirectX de junio de 2010](https://www.microsoft.com/download/en/details.aspx?id=6812).
-   **Opciones de modo de mezcla**. BOTHSRCALPHA se ha quitado de D3D10 \_ Blend porque es redundante con BOTHINVSRCALPHA. Consulte [**D3D10 \_ Blend**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) para obtener más información.
-   **Formatos de compresión de bloque**. No hay distinción entre alfa premultiplicado o alfa no multiplicado previamente en Direct3D 10. Estos formatos de Direct3D 9 se asignan a estos formatos de Direct3D 10: 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2,DXT3  | BC2\*       |
    | DXT4, DXT5  | BC3\*       |

    

     

    Vea [compresión de bloques (Direct3D 10)](d3d10-graphics-programming-guide-resources-block-compression.md) para obtener información adicional.

-   **Planos de recortes**. En lugar de usar planos de clips, Direct3D 10 implementa distancias de recorte y distancias de selección, con un máximo de 8 componentes en un máximo de 2 elementos de atributos de vértice. Vea [semántica (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-semantics.md) para obtener información adicional. En el [ejemplo FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) se ofrece un ejemplo de emulación de planos de clips en Direct3D 10.
-   **Interpolación**. Direct3D 10 no admite la escritura de datos propuestos en un destino de representación.
-   **La canalización de transformación y de iluminación de funciones fijas no está disponible**. En su lugar, debe usar sombreadores. Consulte [fases del sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obtener información adicional.
-   **Mezclador de textura de función fija (también denominado sombreador de píxeles de función fija)**. En su lugar, debe usar sombreadores. Consulte [fases del sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obtener información adicional.
-   Los **modos de relleno** han cambiado. Direct3D 10 implementa modos de relleno sólido y reticular. Se ha quitado el punto D3DFILLMODE, use un sombreador de geometría para emular el modo de punto si es necesario. En el [ejemplo FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) se ofrece un ejemplo de emulación del punto D3DFILLMODE en Direct3D 10. Consulte fases del [**\_ \_ modo de relleno**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) y [sombreador de D3D10 (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obtener información adicional.
-   **Formatos**. El hardware puede usar formatos expuestos por la API. Los formatos de luminancia ya no se implementan.
-   **Filtrado de mipmap**. Se ha quitado la opción para seleccionar el modo sin filtro. En su lugar, use una textura con un solo mipmap o establezca el estado de la muestra de MaxLOD en 0. Vea [objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obtener información adicional.
-   **Paletas**. En su lugar, las aplicaciones deben usar una lectura de textura dependiente.
-   **Modelos de sombreador de píxeles y vértices**: 1 \_ x, 2 \_ x y 3 \_ 0. Direct3D 10 admite el modelo de sombreador 4. Consulte [modelo de sombreador 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md) para obtener información adicional.
-   Los **sprites de punto**. En su lugar, use un sombreador de geometría. Consulte [fases del sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obtener información adicional.
-   **Reglas de rasterización**. Las reglas de rasterización de líneas GDI heredadas se reemplazan por reglas más sencillas y más sencillas. Ya no se admite el control de último píxel para las líneas. Vea [reglas de rasterización (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) para obtener información adicional.
-   **Modos de sombreado**. Se ha quitado D3DSHADEMODE (que admiten el sombreado Flat/Gouraud/Phong). Direct3D 10 implementa dos modificadores de interpolación para las salidas del sombreador de vértices. Vea el [ejemplo de FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) para ver un ejemplo de emulación de los modos Gouraud y de sombra plana de Direct3D 9 en Direct3D 10.
-   instrucción **texldp** . Una aplicación debe implementar una carga de textura proyectada con instrucciones de HLSL adicionales. Consulte [referencia de HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) para obtener información adicional. En el [ejemplo FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) se ofrece un ejemplo de emulación de Texldp en Direct3D 10.
-   Ya no se admite el estado de la fase de textura de **Índice de textura** (TCI) (D3DTSS \_ TEXCOORDINDEX).
-   **Ventiladores de triángulo**. Una aplicación debe convertir los ventiladores de triángulo existentes en listas de triángulos o bandas de triángulos. Para emular algunos comportamientos mediante DrawPrimitive en API anteriores, pruebe a usar DrawIndexed en Direct3D 10. Vea [topologías primitivas (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) para obtener información adicional.
-   **W almacenamiento en búfer**. No se garantiza la compatibilidad de hardware; en su lugar, se recomienda que una aplicación use búferes de profundidad de alta precisión. Consulte [configuración de la funcionalidad de Depth-Stencil (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) para obtener información adicional.
-   **Modos de ajuste** (ajuste de coordenadas de textura). El ajuste de la dirección de textura (como Wrap, Mirror, Clamp, etc.) sigue existiendo. Consulte [**\_ \_ Descripción**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) de la muestra de D3D10 y [**modo de dirección de textura de D3D10 \_ \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de la API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
