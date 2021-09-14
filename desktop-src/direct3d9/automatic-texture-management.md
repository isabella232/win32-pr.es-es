---
description: La administración de texturas es el proceso de determinar qué texturas son necesarias para representarse en un momento dado y asegurarse de que esas texturas se cargan en la memoria de vídeo.
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: Administración automática de texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0eb14eede197661bc127a062229ebed31274ae8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060754"
---
# <a name="automatic-texture-management-direct3d-9"></a>Administración automática de texturas (Direct3D 9)

La administración de texturas es el proceso de determinar qué texturas son necesarias para representarse en un momento dado y asegurarse de que esas texturas se cargan en la memoria de vídeo. Al igual que con cualquier algoritmo, los esquemas de administración de texturas varían en complejidad, pero cualquier enfoque para la administración de texturas implica las siguientes tareas clave.

-   Seguimiento de la cantidad de memoria de textura disponible.
-   Calcular qué texturas son necesarias para la representación y cuáles no.
-   Determinar qué recursos de textura existentes se pueden volver a cargar con otra imagen de textura y qué superficies se deben destruir y reemplazar por nuevos recursos de textura.

Direct3D implementa la administración de texturas compatible con el sistema para garantizar que las texturas se cargan para obtener un rendimiento óptimo. Los recursos de textura que administra Direct3D se conocen como texturas administradas.

El administrador de texturas realiza un seguimiento de las texturas con una marca de tiempo que identifica cuándo se usó por última vez la textura. A continuación, usa un algoritmo usado menos recientemente para determinar qué texturas se deben quitar. Las prioridades de textura se usan como separadores cuando dos texturas están destinadas a la eliminación de la memoria. Si dos texturas tienen el mismo valor de prioridad, se quita la textura usada menos recientemente. Sin embargo, si dos texturas tienen la misma marca de tiempo, la textura que tiene una prioridad inferior se quita primero.

Al crearlas, se solicita la administración automática de texturas para las superficies de textura. Para recuperar una textura administrada en una aplicación de C++, cree un recurso de textura llamando a [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) y especificando D3DPOOL MANAGED para el \_ parámetro Pool. No se permite especificar dónde desea que se cree la textura. No puede usar las marcas D3DPOOL \_ DEFAULT o D3DPOOL \_ SYSTEMMEM al crear una textura administrada. Después de crear la textura administrada, puede llamar al método [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para establecerla en una fase en la cascada de textura del dispositivo de representación.

Puede asignar una prioridad a las texturas administradas llamando al método [**IDirect3DResource9::SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) para la superficie de textura.

Direct3D descarga automáticamente texturas en la memoria de vídeo según sea necesario. El sistema podría almacenar en caché texturas administradas en memoria de vídeo local o no local, dependiendo de la disponibilidad de la memoria de vídeo no local u otros factores. La ubicación de caché de las texturas administradas no se comunica con la aplicación, ni esta información es necesaria para usar la administración automática de texturas. Si la aplicación usa más texturas de las que caben en la memoria de vídeo, Direct3D quita las texturas más antiguas de la memoria de vídeo para hacer espacio para las nuevas texturas. Si vuelve a usar una textura quitada, el sistema usa la superficie de textura de memoria del sistema original para volver a cargar la textura en la memoria caché de vídeo. Aunque es necesario volver a cargar la textura, también reduce el rendimiento de la aplicación.

Puede modificar dinámicamente la copia de memoria del sistema original de la textura actualizando o bloqueando el recurso de textura. Cuando el sistema detecta una superficie desnuciada (una vez completada una actualización o cuando se desbloquea la superficie), el administrador de texturas actualiza automáticamente la copia de memoria de vídeo de la textura. El rendimiento en el que se incurre es similar a volver a cargar una textura quitada.

Al escribir un nuevo nivel en un juego, es posible que la aplicación tenga que vaciar todas las texturas administradas de la memoria de vídeo (mediante una llamada a [**IDirect3DDevice9::EvictManagedResources).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)

Para obtener más información sobre la administración de recursos, vea [Administración de recursos (Direct3D 9).](managing-resources.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
