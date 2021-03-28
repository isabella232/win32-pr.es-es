---
title: Operaciones disponibles en los recursos en mosaico
description: En esta sección se enumeran las operaciones que se pueden realizar en los recursos en mosaico.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076146"
---
# <a name="operations-available-on-tiled-resources"></a>Operaciones disponibles en los recursos en mosaico

En esta sección se enumeran las operaciones que se pueden realizar en los recursos en mosaico.

-   void [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) y [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations: estas ubicaciones de iconos de punto de operaciones en un recurso en mosaico en ubicaciones en grupos de mosaicos, o en null o en ambas. Estas operaciones pueden actualizar un subconjunto separado de los punteros en mosaico.
-   Operaciones de copia \* () y actualización \* (): todas las API que pueden copiar datos en una superficie de grupo predeterminada (por ejemplo, [**Id3d11devicecontext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) y [**id3d11devicecontext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) funcionan para los recursos en mosaico. La lectura desde mosaicos sin asignar produce 0 y las escrituras en mosaicos sin asignar se quitan.
-   [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) y [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) : estas operaciones existen para copiar mosaicos con una granularidad de 64 KB en cualquier recurso en mosaico y un recurso de búfer en un diseño de memoria canónico. El controlador de pantalla y el hardware realizan cualquier memoria "permutación" necesaria para el recurso en mosaico.
-   Los enlaces de canalización de Direct3D y la creación y los enlaces de la vista que funcionarían en recursos no en mosaico también funcionan en recursos en mosaico.

Los controles de mosaico están disponibles en contextos inmediatos o aplazados (al igual que las actualizaciones de los recursos típicos) y en el impacto de la ejecución en los accesos posteriores a los mosaicos (no las operaciones enviadas previamente).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

 




