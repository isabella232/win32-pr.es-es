---
description: La clase CBaseAllocator es una clase base abstracta que implementa un asignador. Los asignadores exponen la interfaz IMemAllocator.
ms.assetid: 3c9003d8-f15c-4e85-9712-9aaa87dffdf3
title: CBaseAllocator (clase, Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 068dd45ee3ffac5c3b915c3b0cdd8bc87756377e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072296"
---
# <a name="cbaseallocator-class"></a>CBaseAllocator (clase)

![Jerarquía de clases cbaseallocator](images/filter10.png)

La **clase CBaseAllocator** es una clase base abstracta que implementa un asignador. Los asignadores exponen la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Un *asignador* es un objeto que asigna búferes de memoria. El asignador mantiene una lista de búferes disponibles. Cuando un cliente (generalmente un filtro) solicita un búfer, el asignador recupera uno de la lista. El cliente rellena el búfer con datos y podría pasar el búfer a otro objeto. Finalmente, el búfer se libera y el asignador lo devuelve a la lista de búferes disponibles.

Cada búfer se encapsula mediante un objeto denominado ejemplo *multimedia*. Los ejemplos multimedia son una manera de empaquetar punteros a bloques de memoria dentro del marco del Modelo de objetos componentes (COM). Los ejemplos multimedia exponen [**la interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) y se implementan mediante la [**clase CMediaSample.**](cmediasample.md) Un ejemplo multimedia contiene un puntero al búfer asociado, al que se puede acceder mediante una llamada al [**método IMediaSample::GetPointer.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) Para obtener más información, [vea Ejemplos y asignadores.](samples-and-allocators.md)

Para usar esta clase, realice los pasos siguientes:

1.  Llame al [**método CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) para especificar los requisitos del búfer, incluido el número de búferes y el tamaño de cada búfer.
2.  Llame al [**método CBaseAllocator::Commit**](cbaseallocator-commit.md) para asignar los búferes.
3.  Llame al [**método CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) para recuperar ejemplos multimedia. Este método se bloquea hasta que el ejemplo siguiente esté disponible.
4.  Cuando haya terminado con cada ejemplo, llame al **método IUnknown::Release** en el ejemplo. El ejemplo no se elimina cuando su recuento de referencias alcanza cero. En su lugar, el ejemplo vuelve a la lista libre del asignador.
5.  Cuando haya terminado de usar el asignador, llame al método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) para liberar la memoria de los búferes.

El [**método Commit**](cbaseallocator-commit.md) llama al método virtual [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md), que asigna la memoria para los búferes. El [**método Decommit**](cbaseallocator-decommit.md) llama al método virtual [**puro CBaseAllocator::Free**](cbaseallocator-free.md), que libera la memoria. Las clases derivadas deben invalidar estos dos métodos.

La clase base [**CMemAllocator**](cmemallocator.md) se deriva de **CBaseAllocator**. Las clases base de filtro usan **la clase CMemAllocator.**



| Variables de miembro protegido                                                   | Descripción                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**m \_ lFree**](cbaseallocator-m-lfree.md)                                   | Puntero a una lista de ejemplos de medios disponibles (gratuitos).                                       |
| [**m \_ hSem**](cbaseallocator-m-hsem.md)                                     | Semáforo que se señala cuando una muestra está disponible.                                |
| [**m \_ lWaiting**](cbaseallocator-m-lwaiting.md)                             | Recuento de subprocesos que esperan ejemplos.                                                      |
| [**m \_ lCount**](cbaseallocator-m-lcount.md)                                 | Número de búferes que se proporcionarán.                                                              |
| [**m \_ lAllocated**](cbaseallocator-m-lallocated.md)                         | Número de búferes asignados actualmente.                                                     |
| [**m \_ lSize**](cbaseallocator-m-lsize.md)                                   | Tamaño de cada búfer.                                                                       |
| [**m \_ lAlignment**](cbaseallocator-m-lalignment.md)                         | Alineación de cada búfer.                                                                  |
| [**m \_ lPrefix**](cbaseallocator-m-lprefix.md)                               | Prefijo de cada búfer.                                                                     |
| [**m \_ bChanged**](cbaseallocator-m-bchanged.md)                             | Marca que indica si los requisitos del búfer han cambiado.                              |
| [**m \_ bCommitted**](cbaseallocator-m-bcommitted.md)                         | Marca que indica si se ha confirmado el asignador.                                  |
| [**m \_ bDecommitInProgress**](cbaseallocator-m-bdecommitinprogress.md)       | Marca que indica si hay una operación de desa confirmación en curso.                               |
| [**m \_ pNotify**](cbaseallocator-m-pnotify.md)                               | Puntero a una interfaz de devolución de llamada, a la que se llama cuando se liberan muestras.                |
| [**m \_ fEnableReleaseCallback**](cbaseallocator-m-fenablereleasecallback.md) | Marca que indica si la devolución de llamada de versión está habilitada.                                   |
| Métodos protegidos                                                            | Descripción                                                                                |
| [**Alloc**](cbaseallocator-alloc.md)                                        | Asigna memoria para los búferes. Virtual.                                                 |
| Métodos públicos                                                               | Descripción                                                                                |
| [**CBaseAllocator**](cbaseallocator-cbaseallocator.md)                      | Método constructor.                                                                        |
| [**~ CBaseAllocator**](cbaseallocator--cbaseallocator.md)                   | Método destructor.                                                                         |
| [**SetNotify**](cbaseallocator-setnotify.md)                                | Obsoleto.                                                                                  |
| [**GetFreeCount**](cbaseallocator-getfreecount.md)                          | Recupera el número de muestras de medios que no están en uso.                                 |
| [**NotifySample**](cbaseallocator-notifysample.md)                          | Libera todos los subprocesos que están esperando ejemplos.                                         |
| [**SetWaiting**](cbaseallocator-setwaiting.md)                              | Incrementa el número de subprocesos en espera.                                                   |
| Métodos virtuales puros                                                         | Descripción                                                                                |
| [**Gratuito**](cbaseallocator-free.md)                                          | Libera toda la memoria del búfer.                                                         |
| Métodos IMemAllocator                                                        | Descripción                                                                                |
| [**SetProperties**](cbaseallocator-setproperties.md)                        | Especifica el número de búferes que se asignarán y el tamaño de cada búfer.                   |
| [**GetProperties**](cbaseallocator-getproperties.md)                        | Recupera el número de búferes que creará el asignador y las propiedades del búfer. |
| [**Commit**](cbaseallocator-commit.md)                                      | Asigna la memoria para los búferes.                                                      |
| [**Desacomprimido**](cbaseallocator-decommit.md)                                  | Desacompone los búferes.                                                                     |
| [**GetBuffer**](cbaseallocator-getbuffer.md)                                | Recupera un ejemplo multimedia que contiene un búfer.                                           |
| [**ReleaseBuffer**](cbaseallocator-releasebuffer.md)                        | Devuelve un ejemplo multimedia a la lista de ejemplos multimedia gratuitos.                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Proporcionar un asignador personalizado](providing-a-custom-allocator.md)
</dt> </dl>

 

 




