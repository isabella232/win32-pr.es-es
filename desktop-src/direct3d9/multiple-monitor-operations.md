---
description: 'Cuando un dispositivo se restablece correctamente (IDirect3DDevice9:: RESET) o se crea (IDirect3D9:: CreateDevice) en las operaciones de pantalla completa, el objeto de Direct3D que creó el dispositivo se marca como propietario de todos los adaptadores del sistema.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Operaciones de Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714722"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Operaciones de Multiple-Monitor (Direct3D 9)

Cuando un dispositivo se restablece correctamente ([**IDirect3DDevice9:: RESET**](/windows/desktop/api)) o se crea ([**IDirect3D9:: CreateDevice**](/windows/desktop/api)) en las operaciones de pantalla completa, el objeto de Direct3D que creó el dispositivo se marca como propietario de todos los adaptadores del sistema. Este estado se conoce como modo exclusivo y el objeto Direct3D posee el modo exclusivo. El modo exclusivo significa que los dispositivos creados por cualquier otro objeto de Direct3D no pueden asumir operaciones de pantalla completa ni asignar memoria de vídeo. Además, cuando un objeto Direct3D asume el modo exclusivo, todos los dispositivos que no sean el que se pusieron en pantalla completa se colocarán en estado perdido. Para obtener más información, vea [dispositivos perdidos (Direct3D 9)](lost-devices.md).

Junto con el modo exclusivo, el objeto de Direct3D se informa de la ventana de enfoque que el dispositivo usará. El modo exclusivo se libera cuando el dispositivo de pantalla completa final que posee ese objeto de Direct3D se restablece al modo de ventana o se destruye.

Los dispositivos se pueden dividir en dos categorías cuando un objeto de Direct3D posee el modo exclusivo. La primera categoría de dispositivos tiene las siguientes características.

-   Los crea el mismo objeto de Direct3D que creó el dispositivo que está en pantalla completa.
-   Tienen la misma ventana de foco que el dispositivo que está en pantalla completa.
-   Representan un adaptador diferente de cualquier dispositivo de pantalla completa.

Los dispositivos de esta categoría no tienen ninguna restricción en cuanto a su capacidad de restablecimiento o creación, y no se colocan en estado perdido. Los dispositivos de esta categoría incluso se pueden poner en modo de pantalla completa.

Los dispositivos que no están en la primera categoría: los dispositivos creados por otro objeto de Direct3D, creados con una ventana de foco diferente y creados para un adaptador con un dispositivo que ya está en pantalla completa, no se pueden restablecer y permanecen en estado perdido hasta que se pierde el modo exclusivo. Como resultado, una aplicación de varios monitores puede poner varios dispositivos en modo de pantalla completa, pero solo si todos estos dispositivos son para adaptadores distintos, se crearon con el mismo objeto de Direct3D y comparten la misma ventana de foco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Presentación de una escena](presenting-a-scene.md)
</dt> </dl>

 

 



