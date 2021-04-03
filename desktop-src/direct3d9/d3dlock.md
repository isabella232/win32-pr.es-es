---
description: Combinación de cero o más opciones de bloqueo que describen el tipo de bloqueo que se va a realizar.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3a60318aad8ae0fadcf02d5dea76f6aa62548
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807699"
---
# <a name="d3dlock"></a>D3DLOCK

Combinación de cero o más opciones de bloqueo que describen el tipo de bloqueo que se va a realizar.



|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| \_Descartar D3DLOCK           | La aplicación descarta toda la memoria dentro de la región bloqueada. En el caso de los búferes de vértices y de índices, se descartará todo el búfer. Esta opción solo es válida cuando el recurso se crea con uso dinámico (vea [D3DUSAGE](d3dusage.md)).                                                                                                                                                                                                                                                                                                                                                           |
| D3DLOCK \_ DONOTWAIT         | Permite que una aplicación recupere ciclos de CPU si el controlador no puede bloquear la superficie inmediatamente. Si se establece esta marca y el controlador no puede bloquear la superficie inmediatamente, la llamada de bloqueo devolverá D3DERR \_ WASSTILLDRAWING. Esta marca solo se puede usar cuando se bloquea una superficie creada con [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api)o [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface). Esta marca también se puede utilizar con un búfer de reserva.            |
| \_No se \_ pudo \_ Actualizar D3DLOCK | De forma predeterminada, un bloqueo en un recurso agrega una región desfasada a ese recurso. Esta opción evita cualquier cambio en el estado de modificación del recurso. Las aplicaciones deben usar esta opción cuando tengan información adicional sobre el conjunto de regiones que han cambiado durante la operación de bloqueo.                                                                                                                                                                                                                                                                                                                    |
| D3DLOCK \_ NOOVERWRITE       | Indica que la memoria a la que se hizo referencia en una llamada de dibujo desde el último bloqueo sin esta marca no se modificará durante el bloqueo. Esto puede habilitar las optimizaciones cuando la aplicación está anexando datos a un recurso. Si se especifica esta marca, el controlador se devolverá inmediatamente si el recurso está en uso; de lo contrario, el controlador debe terminar de usar el recurso antes de volver del bloqueo.                                                                                                                                                                                            |
| D3DLOCK \_ NOSYSLOCK         | El comportamiento predeterminado de un bloqueo de memoria de vídeo es reservar una sección crítica para todo el sistema, lo que garantiza que no se producirán cambios en el modo de presentación mientras dure el bloqueo. Esta opción hace que la sección crítica para todo el sistema no se mantenga mientras dure el bloqueo.<br/> La operación de bloqueo lleva mucho tiempo, pero puede permitir que el sistema realice otras tareas, como mover el cursor del mouse. Esta opción es útil para los bloqueos de larga duración, como el bloqueo del búfer de reserva para la representación de software que de otro modo afectaría negativamente a la capacidad de respuesta del sistema.<br/> |
| D3DLOCK \_ ReadOnly          | La aplicación no escribirá en el búfer. Esto permite que los recursos almacenados en formatos no nativos guarden el paso de recompresión al desbloquearse.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>Información constante



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3d9types. h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**Bloqueo**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**Bloqueo**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

**LockVertexBuffer**
</dt> <dt>

[**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
