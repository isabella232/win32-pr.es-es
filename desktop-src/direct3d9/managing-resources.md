---
description: La administración de recursos es el proceso en el que los recursos se promueven del almacenamiento de memoria del sistema al almacenamiento accesible para dispositivos y se descartan del almacenamiento accesible desde el dispositivo.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Administrar recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ef7a8be0e71c652b6e3f2ed467e866fd922791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274686"
---
# <a name="managing-resources-direct3d-9"></a>Administrar recursos (Direct3D 9)

La administración de recursos es el proceso en el que los recursos se promueven del almacenamiento de memoria del sistema al almacenamiento accesible para dispositivos y se descartan del almacenamiento accesible desde el dispositivo. El tiempo de ejecución de Direct3D tiene su propio algoritmo de administración basado en una técnica de prioridad usada menos recientemente. Direct3D cambia a una técnica de prioridad usada más recientemente cuando detecta que se usan más recursos de los que pueden coexistir en la memoria accesible para dispositivos en un solo fotograma: entre las llamadas a [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) y [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .

Use la [**marca \_ predeterminada de D3DPOOL**](./d3dpool.md) en el momento de la creación para especificar que un recurso se coloca en el bloque de memoria más adecuado para el conjunto de usos solicitado para el recurso especificado. Suele ser la memoria de vídeo, incluida la memoria de vídeo local y la memoria de puerto de gráficos acelerado (AGP). Los recursos del grupo predeterminado no se conservan a través de las transiciones entre los Estados de pérdida y de funcionamiento del dispositivo. Estos recursos deben liberarse antes de llamar a RESET y se deben volver a crear.

Use la [**marca \_ administrada D3DPOOL**](./d3dpool.md) en el momento de la creación para especificar un recurso administrado. Los recursos administrados se conservan a través de las transiciones entre los Estados de pérdida y de funcionamiento del dispositivo. Estos recursos existen tanto en el vídeo como en la memoria del sistema. Un recurso administrado se copiará en la memoria de vídeo cuando sea necesario durante la representación. El dispositivo se puede restaurar con una llamada a [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)y estos recursos continúan funcionando normalmente sin tener que volver a cargarlos con los datos. Sin embargo, si el dispositivo se debe destruir y volver a crear, se deben volver a crear todos los recursos.

No se recomienda la administración de recursos para los recursos que cambian con una frecuencia alta. Por ejemplo, los búferes de vértices y de índices que se usan para recorrer un gráfico de escena cada fotograma que representa solo la geometría visible para el usuario cambia cada fotograma. Dado que los recursos administrados están respaldados por la memoria del sistema, los cambios constantes deben actualizarse en la memoria del sistema, lo que puede provocar una degradación grave del rendimiento. En este escenario concreto, se debe usar [**D3DPOOL \_ default**](./d3dpool.md) junto con [**D3DUSAGE \_ Dynamic**](d3dusage.md) .

Otro ejemplo para el que no se recomienda la administración de recursos (y que el runtime no permite explícitamente) es la administración de una textura creada con [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Si el tiempo de ejecución administraba la memoria usada por los destinos de representación, su contenido tendría que copiarse constantemente en la memoria del sistema durante la representación, lo que provocaría grandes penalizaciones de rendimiento. Por esta razón, los destinos de representación deben crearse en el grupo predeterminado. Si es necesario el acceso a la CPU de los datos contenidos en un destino de representación, los datos se deben copiar en un recurso creado en [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) mediante [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api)o [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

Para obtener más información sobre el estado de pérdida de un dispositivo, vea [dispositivos perdidos (Direct3D 9)](lost-devices.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
