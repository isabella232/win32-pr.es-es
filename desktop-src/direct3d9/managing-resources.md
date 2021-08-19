---
description: La administración de recursos es el proceso en el que los recursos se promueven desde el almacenamiento de memoria del sistema al almacenamiento accesible desde el dispositivo y se descartan del almacenamiento accesible desde el dispositivo.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Administración de recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b860f1c394de932f167de94a3552315b1b70396e9900fccc079ab09142c9e31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728468"
---
# <a name="managing-resources-direct3d-9"></a>Administración de recursos (Direct3D 9)

La administración de recursos es el proceso en el que los recursos se promueven desde el almacenamiento de memoria del sistema al almacenamiento accesible desde el dispositivo y se descartan del almacenamiento accesible desde el dispositivo. El tiempo de ejecución de Direct3D tiene su propio algoritmo de administración basado en una técnica de prioridad usada menos recientemente. Direct3D cambia a una técnica de prioridad usada más recientemente cuando detecta que se usan más recursos de los que pueden coexistir en la memoria accesible desde el dispositivo en un solo fotograma, entre las llamadas [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) [**e IDirect3DDevice9::EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)

Use la [**marca D3DPOOL \_ DEFAULT**](./d3dpool.md) en el momento de la creación para especificar que un recurso se coloca en el grupo de memoria más adecuado para el conjunto de usos solicitado para el recurso especificado. Normalmente se trata de memoria de vídeo, incluida la memoria de vídeo local y la memoria de puerto de gráficos acelerados (AGP). Los recursos del grupo predeterminado no se conservan a través de transiciones entre los estados perdido y operativo del dispositivo. Estos recursos deben liberarse antes de llamar al restablecimiento y, a continuación, se deben volver a crear.

Use la [**marca D3DPOOL \_ MANAGED**](./d3dpool.md) en el momento de la creación para especificar un recurso administrado. Los recursos administrados se conservan a través de transiciones entre los estados perdidos y operativos del dispositivo. Estos recursos existen tanto en el vídeo como en la memoria del sistema. Un recurso administrado se copiará en la memoria de vídeo cuando sea necesario durante la representación. El dispositivo se puede restaurar con una llamada a [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)y estos recursos siguen funcionando con normalidad sin volver a cargarse con datos. Sin embargo, si el dispositivo se debe destruir y volver a crear, se deben volver a crear todos los recursos.

No se recomienda la administración de recursos para los recursos que cambian con alta frecuencia. Por ejemplo, los búferes de vértices e índices que se usan para recorrer un gráfico de escena cada fotograma que representa solo la geometría visible para el usuario cambia cada fotograma. Puesto que los recursos administrados están avalados por la memoria del sistema, los cambios constantes deben actualizarse en la memoria del sistema, lo que puede provocar una degradación grave del rendimiento. Para este escenario concreto, [**se debe usar D3DPOOL \_ DEFAULT**](./d3dpool.md) junto con [**D3DUSAGE \_ DYNAMIC.**](d3dusage.md)

Otro ejemplo para el que no se recomienda la administración de recursos (y no se permite explícitamente por el tiempo de ejecución) es la administración de una textura creada con [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Si el tiempo de ejecución administra la memoria utilizada por los destinos de representación, su contenido tendría que copiarse constantemente en la memoria del sistema durante la representación, lo que provocaría grandes penalizaciones de rendimiento. Por este motivo, los destinos de representación deben crearse en el grupo predeterminado. Si se necesita acceso a la CPU de los datos contenidos en un destino de representación, los datos se deben copiar en un recurso creado en [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) mediante [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api)o [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

Para obtener más información sobre el estado perdido de un dispositivo, vea [Dispositivos perdidos (Direct3D 9).](lost-devices.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
