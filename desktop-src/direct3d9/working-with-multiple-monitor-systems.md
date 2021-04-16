---
description: 'El concepto de modo de pantalla completa exclusivo se conserva en Direct3D 9, pero se mantiene completamente implícito en las llamadas de método IDirect3D9:: CreateDevice y IDirect3DDevice9:: RESET.'
ms.assetid: c3503d62-d9f9-4eec-8af3-ebcbfe7064d4
title: Trabajar con varios sistemas de supervisión (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184a11f06d2296100a0b546e29770f44977b4de3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686326"
---
# <a name="working-with-multiple-monitor-systems-direct3d-9"></a>Trabajar con varios sistemas de supervisión (Direct3D 9)

El concepto de modo de pantalla completa exclusivo se conserva en Direct3D 9, pero se mantiene completamente implícito en las llamadas de método [**IDirect3D9:: CreateDevice**](/windows/desktop/api) y [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) . Cada vez que un dispositivo se restablece o se crea correctamente en una operación de pantalla completa, el objeto de Direct3D que creó el dispositivo se marca como propietario de todos los adaptadores del sistema. Este estado se conoce como modo exclusivo y, en este momento, el objeto de Direct3D posee el modo exclusivo. El modo exclusivo significa que los dispositivos creados por cualquier otro objeto de Direct3D9 no pueden asumir una operación de pantalla completa ni asignar memoria de vídeo. Además, cuando un objeto de Direct3D9 asume el modo exclusivo, todos los dispositivos que no sean el dispositivo que pasó a la pantalla completa se colocan en el estado perdido. Para obtener información sobre cómo controlar los dispositivos perdidos, vea [dispositivos perdidos (Direct3D 9)](lost-devices.md).

Junto con el modo exclusivo, el objeto Direct3D9 está informado de la ventana de enfoque que va a utilizar el dispositivo. El modo exclusivo se libera cuando el último dispositivo de pantalla completa que posee ese objeto Direct3D9 se restablece al modo de ventana o se destruye.

Los dispositivos se pueden dividir en dos categorías cuando un objeto de Direct3D9 posee el modo exclusivo. La primera categoría de dispositivos son las creadas por el mismo objeto de Direct3D9 que creó el dispositivo que ya está en pantalla completa, tienen la misma ventana de foco que el dispositivo que ya está en pantalla completa y representan un adaptador diferente de cualquier dispositivo de pantalla completa. Los dispositivos de esta categoría no tienen ninguna restricción en cuanto a su capacidad de restablecimiento o creación y no se colocan en el estado perdido. Los dispositivos de esta categoría se pueden incluir incluso en el modo de pantalla completa.

Los dispositivos que no se encuentren en esta categoría, que serían los creados por un objeto de Direct3D9 diferente, o con una ventana de enfoque diferente, o para algún adaptador con un dispositivo que ya está en pantalla completa no se pueden restablecer y permanecen en estado perdido hasta que se pierde el modo exclusivo.

La implicación práctica es que una aplicación de varios monitores puede poner varios dispositivos en modo de pantalla completa, pero solo si todos estos dispositivos son para adaptadores distintos, los creó el mismo objeto de Direct3D9 y todos comparten la misma ventana de enfoque.

Al crear un nuevo dispositivo con el mismo objeto [**IDirect3D9**](/windows/desktop/api) y la misma ventana de foco, el dispositivo original perderá sus superficies. Tendrá que llamar a [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) en el primer dispositivo para que la aplicación lo use. Por ejemplo, para crear dos dispositivos, haga lo siguiente:

1.  Crear dispositivo 1
2.  Crear dispositivo 2
3.  Restablecer dispositivo 1

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 
