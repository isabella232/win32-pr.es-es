---
description: La administración de texturas es el proceso por el que se determinan las texturas que se necesitan para la representación en un momento dado y se garantiza que dichas texturas se cargan en la memoria de vídeo.
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: Administración automática de texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0eb14eede197661bc127a062229ebed31274ae8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907437"
---
# <a name="automatic-texture-management-direct3d-9"></a>Administración automática de texturas (Direct3D 9)

La administración de texturas es el proceso por el que se determinan las texturas que se necesitan para la representación en un momento dado y se garantiza que dichas texturas se cargan en la memoria de vídeo. Como con cualquier algoritmo, los esquemas de administración de texturas varían en complejidad, pero cualquier enfoque en la administración de texturas implica las siguientes tareas clave.

-   Seguimiento de la cantidad de memoria de textura disponible.
-   Calcular las texturas que se necesitan para la representación y cuáles no.
-   Determinar qué recursos de textura existentes se pueden volver a cargar con otra imagen de textura y qué superficies deben destruirse y reemplazarse con nuevos recursos de textura.

Direct3D implementa la administración de texturas compatible con el sistema para asegurarse de que las texturas se cargan para un rendimiento óptimo. Los recursos de textura que administra Direct3D se conocen como texturas administradas.

El administrador de textura realiza el seguimiento de las texturas con una marca de tiempo que identifica Cuándo se usó por última vez la textura. A continuación, usa un algoritmo usado menos recientemente para determinar qué texturas se deben quitar. Las prioridades de textura se usan como disyuntores cuando dos texturas se destinan a la eliminación de la memoria. Si dos texturas tienen el mismo valor de prioridad, se quita la textura usada menos recientemente. Sin embargo, si dos texturas tienen la misma marca de tiempo, primero se quita la textura que tiene una prioridad más baja.

Cuando se crean, se solicita la administración automática de texturas para las superficies de textura. Para recuperar una textura administrada en una aplicación de C++, cree un recurso de textura mediante una llamada a [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) y especifique el D3DPOOL \_ administrado para el parámetro Pool. No se le permite especificar dónde desea que se cree la textura. No puede usar las \_ marcas D3DPOOL default o D3DPOOL \_ SYSTEMMEM al crear una textura administrada. Después de crear la textura administrada, puede llamar al método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para establecerla en una fase de la textura en cascada del dispositivo de representación.

Puede asignar una prioridad a las texturas administradas llamando al método [**IDirect3DResource9:: SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) para la superficie de textura.

Direct3D descarga automáticamente las texturas en la memoria de vídeo según sea necesario. El sistema puede almacenar en caché las texturas administradas en la memoria de vídeo local o no local, en función de la disponibilidad de memoria de vídeo no local u otros factores. La ubicación de la memoria caché de las texturas administradas no se comunica con la aplicación, ni tampoco es necesaria para usar la administración de texturas automática. Si la aplicación usa más texturas de las que caben en la memoria de vídeo, Direct3D quita las texturas anteriores de la memoria de vídeo para dejar espacio a las nuevas texturas. Si vuelve a usar una textura quitada, el sistema utiliza la superficie de textura de memoria del sistema original para volver a cargar la textura en la memoria caché de la memoria de vídeo. Aunque es necesario volver a cargar la textura, también se reduce el rendimiento de la aplicación.

Puede modificar dinámicamente la copia de memoria del sistema original de la textura mediante la actualización o el bloqueo del recurso de textura. Cuando el sistema detecta una superficie sucia: una vez completada una actualización o cuando se desbloquea la superficie, el administrador de textura actualiza automáticamente la copia de la textura de la memoria de vídeo. El impacto en el rendimiento en el que se incurre es similar a la recarga de una textura quitada.

Al escribir un nuevo nivel en un juego, es posible que la aplicación tenga que vaciar todas las texturas administradas de la memoria de vídeo (llamando a [**IDirect3DDevice9:: EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)).

Para obtener más información sobre la administración de recursos, vea [administrar recursos (Direct3D 9)](managing-resources.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
