---
description: La clase CTransInPlaceInputPin implementa un pin de entrada que usa la clase CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: CTransInPlaceInputPin (clase, Transip.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973820"
---
# <a name="ctransinplaceinputpin-class"></a>CTransInPlaceInputPin (clase)

![Jerarquía de clases ctransinplaceinputpin](images/tsip01.png)

La `CTransInPlaceInputPin` clase implementa un pin de entrada que usa la clase [**CTransInPlaceFilter.**](ctransinplacefilter.md)

Normalmente, no es necesario derivar de esta clase. Si lo hace, debe invalidar el método [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) del filtro para crear instancias de la clase derivada.



| Variables de miembro protegido                                                          | Descripción                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md)                           | Marca que especifica si el flujo de entrada es de solo lectura. |
| [**m \_ pTIPFilter**](ctransinplaceinputpin-m-ptipfilter.md)                         | Puntero al filtro que creó este pin.               |
| Métodos públicos                                                                      | Descripción                                                |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Método constructor.                                        |
| [**CheckMediaType**](ctransinplaceinputpin-checkmediatype.md)                      | Determina si el pin acepta un tipo de medio específico.       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | Recupera un puntero al asignador del pin.                |
| [**Readonly**](ctransinplaceinputpin-readonly.md)                                  | Indica si el flujo de entrada es de solo lectura.           |
| Métodos de IPin                                                                        | Descripción                                                |
| [**EnumMediaTypes**](ctransinplaceinputpin-enummediatypes.md)                      | Enumera los tipos de medios preferidos del pin.                |
| Métodos IMemInputPin                                                                | Descripción                                                |
| [**GetAllocator**](ctransinplaceinputpin-getallocator.md)                          | Recupera el asignador de memoria propuesto por este pin.       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | Especifica un asignador para la conexión.                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Recupera las propiedades del asignador solicitadas por el pin.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




