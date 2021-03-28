---
title: Operaciones disponibles en grupos de iconos
description: En esta sección se enumeran las operaciones que se pueden realizar en grupos de mosaicos.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271268"
---
# <a name="operations-available-on-tile-pools"></a>Operaciones disponibles en grupos de iconos

En esta sección se enumeran las operaciones que se pueden realizar en grupos de mosaicos.

-   La duración de los grupos de mosaicos funciona como cualquier otro recurso de Direct3D, respaldado por el recuento de referencias, incluido en este caso el seguimiento de las asignaciones de los recursos en mosaico. Cuando la aplicación ya no hace referencia a un grupo de mosaicos y las asignaciones de icono a la memoria han desaparecido y los accesos a la unidad de procesamiento de gráficos (GPU) se han completado, el sistema operativo desasignará el grupo de mosaicos.
-   Las API relacionadas con el uso compartido de Surface y la sincronización funcionan para los grupos de mosaicos (pero no directamente en los recursos en mosaico). De forma similar al comportamiento de los grupos de mosaicos ofrecidos, los comandos de Direct3D que tienen acceso a los recursos en mosaico que apuntan a un grupo de mosaicos se quitan si el grupo de mosaicos se ha compartido y está adquirido actualmente por otro dispositivo y proceso.
-   [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) (operación)
-   Operaciones [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) y [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) : estas API para producir temporalmente la memoria para el sistema operan en todo el grupo de mosaicos (y no están disponibles para recursos individuales en mosaico). Si un recurso en mosaico apunta a un icono de un grupo de mosaicos ofrecido, el recurso en mosaico se comporta como si se hubiera ofrecido (por ejemplo, el tiempo de ejecución quita los comandos que hacen referencia a él).

Los datos no se pueden copiar directamente a y desde la memoria del grupo de mosaicos. Los accesos a la memoria siempre se realizan a través de recursos en mosaico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

 