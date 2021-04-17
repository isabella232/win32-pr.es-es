---
description: La clase CTransInPlaceInputPin implementa un PIN de entrada usado por la clase CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Clase CTransInPlaceInputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679250"
---
# <a name="ctransinplaceinputpin-class"></a>Clase CTransInPlaceInputPin

![jerarquía de clases ctransinplaceinputpin](images/tsip01.png)

La `CTransInPlaceInputPin` clase implementa un PIN de entrada usado por la clase [**CTransInPlaceFilter**](ctransinplacefilter.md) .

Normalmente, no es necesario derivar de esta clase. Si lo hace, debe invalidar el método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) del filtro para crear instancias de la clase derivada.



| Variables de miembro protegidas                                                          | Descripción                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md)                           | Marca que especifica si el flujo de entrada es de solo lectura. |
| [**m \_ pTIPFilter**](ctransinplaceinputpin-m-ptipfilter.md)                         | Puntero al filtro que creó este pin.               |
| Métodos públicos                                                                      | Descripción                                                |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Método de constructor.                                        |
| [**CheckMediaType**](ctransinplaceinputpin-checkmediatype.md)                      | Determina si el PIN acepta un tipo de medio específico.       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | Recupera un puntero al asignador del PIN.                |
| [**ReadOnly**](ctransinplaceinputpin-readonly.md)                                  | Indica si el flujo de entrada es de solo lectura.           |
| Métodos IPin                                                                        | Descripción                                                |
| [**EnumMediaTypes**](ctransinplaceinputpin-enummediatypes.md)                      | Enumera los tipos de medios preferidos del PIN.                |
| Métodos IMemInputPin                                                                | Descripción                                                |
| [**GetAllocator**](ctransinplaceinputpin-getallocator.md)                          | Recupera el asignador de memoria propuesto por este pin.       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | Especifica un asignador para la conexión.                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Recupera las propiedades de asignador solicitadas por el código PIN.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




