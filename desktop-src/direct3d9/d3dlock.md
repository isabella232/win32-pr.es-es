---
description: Combinación de cero o más opciones de bloqueo que describen el tipo de bloqueo que se debe realizar.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e4fcf8db9e60a30aee060dcc483b8d01e59b1c
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343200"
---
# <a name="d3dlock"></a>D3DLOCK

Combinación de cero o más opciones de bloqueo que describen el tipo de bloqueo que se debe realizar.



| \#Definir                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DLOCK \_ DISCARD           | La aplicación descarta toda la memoria dentro de la región bloqueada. En el caso de los búferes de vértices e índices, se descartará todo el búfer. Esta opción solo es válida cuando el recurso se crea con uso dinámico (consulte [D3DUSAGE).](d3dusage.md)                                                                                                                                                                                                                                                                                                                                                           |
| D3DLOCK \_ DONOTWAIT         | Permite a una aplicación recuperar ciclos de CPU si el controlador no puede bloquear la superficie inmediatamente. Si se establece esta marca y el controlador no puede bloquear la superficie inmediatamente, la llamada de bloqueo devolverá D3DERR \_ WASST ODBCDRAWING. Esta marca solo se puede usar al bloquear una superficie creada mediante [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateRenderTarget**](/windows/desktop/api)o [**CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) Esta marca también se puede usar con un búfer de reserva.            |
| D3DLOCK \_ NO \_ DIRTY \_ UPDATE | De forma predeterminada, un bloqueo en un recurso agrega una región desarroba a ese recurso. Esta opción evita cualquier cambio en el estado desasecionado del recurso. Las aplicaciones deben usar esta opción cuando tengan información adicional sobre el conjunto de regiones modificadas durante la operación de bloqueo.                                                                                                                                                                                                                                                                                                                    |
| D3DLOCK \_ NOOVERWRITE       | Indica que la memoria a la que se hizo referencia en una llamada de dibujo desde el último bloqueo sin esta marca no se modificará durante el bloqueo. Esto puede habilitar las optimizaciones cuando la aplicación anexa datos a un recurso. Al especificar esta marca, el controlador puede devolver inmediatamente si el recurso está en uso; de lo contrario, el controlador debe terminar de usar el recurso antes de volver del bloqueo.                                                                                                                                                                                            |
| D3DLOCK \_ NOSYSLOCK         | El comportamiento predeterminado de un bloqueo de memoria de vídeo es reservar una sección crítica para todo el sistema, lo que garantiza que no se producirá ningún cambio en el modo de presentación mientras dure el bloqueo. Esta opción hace que la sección crítica de todo el sistema no se mantiene mientras dure el bloqueo.<br/> La operación de bloqueo lleva mucho tiempo, pero puede permitir que el sistema realice otras tareas, como mover el cursor del mouse. Esta opción es útil para bloqueos de larga duración, como el bloqueo del búfer de reserva para la representación de software que, de lo contrario, afectaría negativamente a la capacidad de respuesta del sistema.<br/> |
| D3DLOCK \_ READONLY          | La aplicación no escribirá en el búfer. Esto permite que los recursos almacenados en formatos no nativos guarden el paso de recompresión al desbloquear.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>Información constante



|  Requisito                        | Value            |
|--------------------------|-------------|
| Encabezado                   | d3d9types.h |
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

[**Caja**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**Caja**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
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

 

 
