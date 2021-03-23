---
title: Uso de descriptores directamente en la firma raíz
description: Las aplicaciones pueden poner descriptores directamente en la firma raíz para evitar tener que pasar por un montón de descriptores.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/15/2020
ms.locfileid: "104549174"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Uso de descriptores directamente en la firma raíz

Las aplicaciones pueden poner descriptores directamente en la firma raíz para evitar tener que pasar por un montón de descriptores. Estos descriptores ocupan mucho espacio en la firma raíz (consulte la sección límites de la firma raíz), por lo que las aplicaciones tienen que usarlos con moderación.

Un uso de ejemplo sería poner una vista de búfer de constantes (CBV) que cambie por dibujo en el diseño raíz para que no sea necesario que la aplicación asigne espacio en el montón de descriptores (y guarde el puntero a una tabla de descriptores en la nueva ubicación del montón de descriptores). Al colocar algo en la firma raíz, la aplicación simplemente está entregando la responsabilidad de control de versiones al controlador, pero se trata de una infraestructura que ya tiene.

En el caso de la representación que usa muy pocos recursos, es posible que no sea necesario usar el uso de la tabla de descriptores o del montón si todos los descriptores necesarios se pueden colocar directamente en la firma raíz.

Los únicos tipos de descriptores que se admiten en la firma raíz son:
- CBVs.
- Vistas de recursos del sombreador (SRVs)/Unordered vistas de acceso (UAVs) de recursos de búfer en los que el formato SRV/UAV contiene solo componentes FLOAT/UINT/SINT de 32 bits (no hay conversión de formato).
- SRVs de estructuras de aceleración de raytracing, en firmas de raíz locales o globales. 

UAVs en la raíz no puede tener contadores asociados. Los descriptores de la firma raíz aparecen cada uno como descriptores independientes individuales &mdash; que no se pueden indexar dinámicamente.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

En el ejemplo anterior, `mySceneData` no se puede declarar como una matriz, como en si se va `cbuffer mySceneData[2]` a asignar a un descriptor en la firma raíz, ya que la indización en los descriptores no se admite en la firma raíz. La aplicación puede definir búferes de constantes individuales independientes y definirlos como una entrada independiente en la firma raíz si se desea. Tenga en cuenta que, dentro de `mySceneData` lo anterior, hay una matriz `bar[2]` . La indexación dinámica dentro del búfer de constantes es válida: un descriptor de la signatura raíz se comporta igual que el mismo descriptor si se obtiene acceso a él a través de un montón de descriptores. Esto contrasta con las constantes de inserción directamente en la firma raíz, que también aparece como un búfer de constantes excepto con la restricción de que no se permite la indexación dinámica dentro de las constantes insertadas, por lo que `bar[2]` no se permitiría allí.

Las siguientes API (de la interfaz [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) son para establecer los descriptores directamente en la firma raíz:

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> No hay ningún concepto de "matriz de descriptores raíz" en Direct3D 12. Las matrices de descriptor solo se admiten en montones de descriptor.

## <a name="related-topics"></a>Temas relacionados

[Firmas raíz](root-signatures.md)
