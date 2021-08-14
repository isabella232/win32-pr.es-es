---
description: Cuando un dispositivo se restablece correctamente (IDirect3DDevice9::Reset) o se crea (IDirect3D9::CreateDevice) en operaciones de pantalla completa, el objeto direct3D que creó el dispositivo se marca como propietario de todos los adaptadores de ese sistema.
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4f175c136cd432223eeaaf32cf44bfbb08e724b54b8afe1dbb9717c2d79a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728215"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Multiple-Monitor (Direct3D 9)

Cuando un dispositivo se restablece correctamente ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) o se crea ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) en operaciones de pantalla completa, el objeto Direct3D que creó el dispositivo se marca como propietario de todos los adaptadores de ese sistema. Este estado se conoce como modo exclusivo y el objeto Direct3D posee el modo exclusivo. El modo exclusivo significa que los dispositivos creados por cualquier otro objeto de Direct3D no pueden asumir operaciones de pantalla completa ni asignar memoria de vídeo. Además, cuando un objeto de Direct3D asume el modo exclusivo, todos los dispositivos distintos del que se pasó a pantalla completa se colocan en estado perdido. Para más información, consulte [Dispositivos perdidos (Direct3D 9).](lost-devices.md)

Junto con el modo exclusivo, se informa al objeto Direct3D de la ventana de foco que usará el dispositivo. El modo exclusivo se libera cuando el dispositivo de pantalla completa final propiedad de ese objeto de Direct3D se restablece al modo de ventana o se destruye.

Los dispositivos se pueden dividir en dos categorías cuando un objeto de Direct3D posee el modo exclusivo. La primera categoría de dispositivos tiene las siguientes características.

-   Se crean mediante el mismo objeto de Direct3D que creó el dispositivo que es de pantalla completa.
-   Tienen la misma ventana de enfoque que el dispositivo que es de pantalla completa.
-   Representan un adaptador diferente de cualquier dispositivo de pantalla completa.

Los dispositivos de esta categoría no tienen ninguna restricción sobre su capacidad para restablecerse o crearse, y no se colocan en estado perdido. Los dispositivos de esta categoría incluso se pueden poner en modo de pantalla completa.

Los dispositivos que no están en la primera categoría (dispositivos creados por otro objeto de Direct3D, creados con una ventana de enfoque diferente y creados para un adaptador con un dispositivo que ya está en pantalla completa) no se pueden restablecer y permanecer en estado perdido hasta que se pierda el modo exclusivo. Como resultado, una aplicación de varios monitores puede colocar varios dispositivos en modo de pantalla completa, pero solo si todos estos dispositivos son para adaptadores diferentes, se crearon con el mismo objeto de Direct3D y comparten la misma ventana de foco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Presentación de una escena](presenting-a-scene.md)
</dt> </dl>

 

 



