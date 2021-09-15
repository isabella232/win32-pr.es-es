---
title: Uso de constantes directamente en la firma raíz
description: Las aplicaciones pueden definir constantes raíz en la firma raíz, cada una como un conjunto de valores de 32 bits. Aparecen en lenguaje de sombreado de alto nivel (HLSL) como búfer constante. Tenga en cuenta que los búferes constantes por motivos históricos se ven como conjuntos de valores de 4x32 bits.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567969"
---
# <a name="using-constants-directly-in-the-root-signature"></a>Uso de constantes directamente en la firma raíz

Las aplicaciones pueden definir constantes raíz en la firma raíz, cada una como un conjunto de valores de 32 bits. Aparecen en lenguaje de sombreado de alto nivel (HLSL) como búfer constante. Tenga en cuenta que los búferes constantes por motivos históricos se ven como conjuntos de valores de 4x32 bits.

Cada conjunto de constantes de usuario se trata como una matriz escalar de valores de 32 bits, indexable dinámicamente y de solo lectura desde el sombreador. La indexación fuera de límites de un conjunto determinado de constantes raíz genera resultados indefinidos. En HLSL, se pueden proporcionar definiciones de estructura de datos para que las constantes de usuario les den tipos. Por ejemplo, si la firma raíz define un conjunto de 4 constantes raíz, HLSL puede superponer la siguiente estructura en ellas.

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

No se permiten matrices en búferes constantes que se asignan a constantes raíz, ya que no se admite la indexación dinámica en el espacio de firma raíz. Por ejemplo, no es válido tener una entrada en el búfer constante como `float myArray[2];` . Un búfer constante asignado a constantes raíz no puede ser una matriz; por lo tanto, no es válido asignar `cbuffer myCBArray[2]` a constantes raíz.

Las constantes se pueden establecer parcialmente. Por ejemplo, si la firma raíz define cuatro valores de 32 bits en *RootTableBindSlot* 2, se puede establecer cualquier subconjunto de las cuatro constantes a la vez (las demás permanecen sin cambios). Esto puede ser útil en agrupaciones que heredan el estado de firma raíz y pueden cambiarlo parcialmente.

Al establecer constantes, tenga cuidado con el diseño de búfer constante esperado por el sombreador. Es posible que las constantes se agregó a `vec4` los límites, por ejemplo. Para comprobar el diseño esperado, compruebe la información de reflexión del sombreador HLSL.

Las siguientes API (desde la [**interfaz ID3D12GraphicsCommandList)**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) son para establecer constantes directamente en la firma raíz:

-   [**SetGraphicsRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [**SetComputeRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

Además, consulte la estructura [**D3D12 \_ ROOT \_ CONSTANTS.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 




