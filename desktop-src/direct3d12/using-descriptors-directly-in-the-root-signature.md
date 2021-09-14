---
title: Uso de descriptores directamente en la firma raíz
description: Para evitar la necesidad de pasar por un montón de descriptores, puede colocar un descriptor directamente en la firma raíz.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f32b423b017477e66ea3ae32eee509ec455d85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072840"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Uso de descriptores directamente en la firma raíz

Para evitar la necesidad de pasar por un montón de descriptores, puede colocar un descriptor directamente en la firma raíz. Estos descriptores ocupa mucho espacio en la firma raíz (consulte Límites de firma [raíz),](./root-signature-limits.md)por lo que se recomienda usarlos con moderación.

Un ejemplo de uso sería colocar en el diseño raíz una vista de búfer constante (CBV) que cambia por dibujo. Esto es para que la aplicación no tenga que asignar espacio del montón de descriptores por dibujo (y guarda una tabla de descriptores en la nueva ubicación del montón de descriptores). Al colocar algo en la firma raíz, la aplicación simplemente entrega la responsabilidad de control de versiones al controlador. pero esa es la infraestructura que los controladores ya tienen.

Para la representación que usa muy pocos recursos, es posible que el uso de tablas o montones de descriptores no sea necesario en absoluto si todos los descriptores necesarios se pueden colocar directamente en la firma raíz.

Estos son los únicos tipos de descriptores admitidos en la firma raíz.

- Vista de búfer constante (CBV).
- Vistas de recursos de sombreador (SRV) / vistas de acceso desordenado (UAV) de recursos de búfer donde no se requiere la conversión de formato (búferes sin tipo). Algunos ejemplos de búferes sin tipo que se pueden enlazar con descriptores raíz incluyen `StructuredBuffer<type>` `RWStructuredBuffer<type>` , y `ByteAddressBuffer` `RWByteAddressBuffer` . Los búferes con tipo, `Buffer<uint>` como y `Buffer<float2>` , no.
- SRV de estructuras de aceleración de rayos, en firmas raíz locales o globales. 

Un UAV de la raíz no puede tener contadores asociados. Los descriptores de la firma raíz aparecen cada uno como descriptores independientes individuales &mdash; que no se pueden indexar dinámicamente.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

En el ejemplo anterior, no se puede declarar como una matriz, como en si se va a asignar a un descriptor en la `mySceneData` `cbuffer mySceneData[2]` firma raíz. Esto se debe a que no se admite la indexación entre descriptores en la firma raíz. Si lo desea, puede definir búferes de constantes individuales independientes y definirlos cada uno como una entrada independiente en la firma raíz. Tenga en cuenta `mySceneData` que, dentro de lo anterior, hay una matriz `bar[2]` . La indexación dinámica dentro del búfer constante es válida; un descriptor de la firma raíz se comporta igual que el mismo descriptor se comportaría si se accedía a él a través de &mdash; un montón de descriptores. Esto contrasta con la entrada de constantes directamente en la firma raíz, que también aparece como un búfer constante, excepto con la restricción de que no se permite la indexación dinámica dentro de las constantes en línea, por lo que no se permitirá `bar[2]` allí.

Estas API (desde la [**interfaz ID3D12GraphicsCommandList)**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) son para establecer descriptores directamente en la firma raíz.

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> No hay ningún concepto de una matriz *de descriptores raíz* en Direct3D 12. Las matrices de descriptores solo se admiten en montones de descriptores.

## <a name="related-topics"></a>Temas relacionados

* [Firmas raíz](root-signatures.md)