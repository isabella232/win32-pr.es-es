---
title: Operaciones disponibles en recursos en mosaico
description: En esta sección se enumeran las operaciones que puede realizar en recursos en mosaico.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcc002a0724b6f545d72f0c1a7a348ce71f44c612289e0e079c85c7768f8a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045603"
---
# <a name="operations-available-on-tiled-resources"></a>Operaciones disponibles en recursos en mosaico

En esta sección se enumeran las operaciones que puede realizar en recursos en mosaico.

-   void [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) operations: estas ubicaciones de mosaico de punto de operaciones en un recurso en mosaico a ubicaciones de grupos de mosaicos, a NULL o a ambas. Estas operaciones pueden actualizar un subconjunto desconexo de los punteros de icono.
-   Operaciones de copia () y actualización (): todas las API que pueden copiar datos hacia y desde una superficie de grupo predeterminada \* \* (por ejemplo, [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) e [**ID3D11DeviceContext1::UpdateSubresource1)**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)funcionan para los recursos en mosaico. La lectura de iconos no mapa genera 0 y se descartan las escrituras en iconos no mapa.
-   [**Operaciones ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2::UpdateTiles:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) estas operaciones existen para copiar iconos con una granularidad de 64 KB hacia y desde cualquier recurso en mosaico y un recurso de búfer en un diseño de memoria canónico. El controlador de pantalla y el hardware realizan cualquier "deslizar" memoria necesaria para el recurso en mosaico.
-   Los enlaces de canalización de Direct3D y las creaciones o enlaces de vistas que funcionarán en recursos sin mosaico también funcionan en recursos en mosaico.

Los controles de icono están disponibles en contextos inmediatos o diferidos (al igual que las actualizaciones de los recursos típicos) y en el impacto de la ejecución en los accesos posteriores a los iconos (no las operaciones enviadas previamente).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

 




