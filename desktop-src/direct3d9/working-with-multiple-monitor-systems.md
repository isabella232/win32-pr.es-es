---
description: El concepto de modo exclusivo de pantalla completa se conserva en Direct3D 9, pero se mantiene completamente implícito en las llamadas al método IDirect3D9::CreateDevice e IDirect3DDevice9::Reset.
ms.assetid: c3503d62-d9f9-4eec-8af3-ebcbfe7064d4
title: Trabajar con varios sistemas de supervisión (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cea4625038f701288676b95fc86c5ed7d56b292795c14b43031affa817bd8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025735"
---
# <a name="working-with-multiple-monitor-systems-direct3d-9"></a>Trabajar con varios sistemas de supervisión (Direct3D 9)

El concepto de modo exclusivo de pantalla completa se conserva en Direct3D 9, pero se mantiene completamente implícito en las llamadas al método [**IDirect3D9::CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9::Reset.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) Cada vez que un dispositivo se restablece correctamente o se crea en una operación de pantalla completa, el objeto de Direct3D que creó el dispositivo se marca como propietario de todos los adaptadores de ese sistema. Este estado se conoce como modo exclusivo y, en este momento, el objeto Direct3D posee el modo exclusivo. El modo exclusivo significa que los dispositivos creados por cualquier otro objeto de Direct3D9 no pueden asumir la operación de pantalla completa ni asignar memoria de vídeo. Además, cuando un objeto Direct3D9 asume el modo exclusivo, todos los dispositivos que no sean el dispositivo que pasó a pantalla completa se colocan en el estado perdido. Para obtener información sobre cómo controlar los dispositivos perdidos, [vea Dispositivos perdidos (Direct3D 9).](lost-devices.md)

Junto con el modo exclusivo, se informa al objeto Direct3D9 de la ventana de enfoque que va a usar el dispositivo. El modo exclusivo se libera cuando el último dispositivo de pantalla completa propiedad de ese objeto Direct3D9 se restablece al modo de ventana o se destruye.

Los dispositivos se pueden dividir en dos categorías cuando un objeto Direct3D9 posee el modo exclusivo. La primera categoría de dispositivos son las creadas por el mismo objeto de Direct3D9 que creó el dispositivo que ya está en pantalla completa, tienen la misma ventana de enfoque que el dispositivo que ya está en pantalla completa y representan un adaptador diferente de cualquier dispositivo de pantalla completa. Los dispositivos de esta categoría no tienen ninguna restricción sobre su capacidad para restablecerse o crearse y no se colocan en el estado perdido. Los dispositivos de esta categoría incluso se pueden colocar en modo de pantalla completa.

Los dispositivos que no están en esta categoría, que serían los creados por un objeto direct3D9 diferente o con una ventana de enfoque diferente, o para algún adaptador con un dispositivo que ya está en pantalla completa no se puede restablecer y permanecer en estado perdido hasta que se pierda el modo exclusivo.

La implicación práctica es que una aplicación de supervisión múltiple puede colocar varios dispositivos en modo de pantalla completa, pero solo si todos estos dispositivos son para adaptadores diferentes, se crearon con el mismo objeto Direct3D9 y todos comparten la misma ventana de enfoque.

Al crear un dispositivo con el mismo objeto [**IDirect3D9**](/windows/desktop/api) y la misma ventana de foco, el dispositivo original perderá sus superficies. Tendrá que llamar a [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) en el primer dispositivo para que la aplicación lo use. Por ejemplo, para crear dos dispositivos, haga lo siguiente:

1.  Creación del dispositivo 1
2.  Creación del dispositivo 2
3.  Restablecer dispositivo 1

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 
