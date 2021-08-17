---
title: Operaciones disponibles en grupos de iconos
description: En esta sección se enumeran las operaciones que puede realizar en grupos de mosaicos.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c72e15ebe9a8fd2f6725451268d3d03fb7b181442907248d0db44860560aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098327"
---
# <a name="operations-available-on-tile-pools"></a>Operaciones disponibles en grupos de iconos

En esta sección se enumeran las operaciones que puede realizar en grupos de mosaicos.

-   La duración de los grupos de mosaicos funciona como cualquier otro recurso de Direct3D, con el respaldo del recuento de referencias, incluido en este caso el seguimiento de asignaciones de recursos en mosaico. Cuando la aplicación ya no hace referencia a un grupo de mosaicos y las asignaciones de mosaicos a la memoria desaparecen y se completa el acceso a la unidad de procesamiento de gráficos (GPU), el sistema operativo desasignará el grupo de mosaicos.
-   Las API relacionadas con el uso compartido de superficie y la sincronización funcionan para grupos de mosaicos (pero no directamente en recursos en mosaico). De forma similar al comportamiento de los grupos de mosaicos ofrecidos, los comandos de Direct3D que acceden a recursos en mosaico que apuntan a un grupo de mosaicos se descartan si el grupo de mosaicos se ha compartido y está adquirido actualmente por otro dispositivo y proceso.
-   [**Operación ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**Operaciones IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) y [**ReclaimResources:**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) estas API para producir memoria temporalmente en el sistema funcionan en todo el grupo de mosaicos (y no están disponibles para recursos en mosaico individuales). Si un recurso en mosaico apunta a un icono de un grupo de mosaicos ofrecido, el recurso en mosaico se comporta como si se hubiera ofrecido (por ejemplo, el tiempo de ejecución quita los comandos que hacen referencia a él).

Los datos no se pueden copiar directamente en la memoria del grupo de mosaicos ni desde esta. Los accesos a la memoria siempre se realizan a través de recursos en mosaico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

 