---
description: La clase CTransInPlaceOutputPin implementa un PIN de salida que se usa en la clase CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Clase CTransInPlaceOutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679238"
---
# <a name="ctransinplaceoutputpin-class"></a>Clase CTransInPlaceOutputPin

![jerarquía de clases ctransinplaceoutputpin](images/tsip02.png)

La `CTransInPlaceOutputPin` clase implementa un PIN de salida que se usa en la clase [**CTransInPlaceFilter**](ctransinplacefilter.md) .

Normalmente, no es necesario derivar de esta clase. Si lo hace, debe invalidar el método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) del filtro para crear instancias de la clase derivada.



| Variables de miembro protegidas                                                      | Descripción                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ pTIPFilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Puntero al filtro que creó este pin.         |
| Métodos públicos                                                                  | Descripción                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Método de constructor.                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | Determina si el PIN acepta un tipo de medio específico. |
| [**SetAllocator**](ctransinplaceoutputpin-setallocator.md)                     | Especifica un asignador para la conexión.           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Recupera un puntero al pin de entrada de nivel inferior.     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | Recupera un puntero al asignador del PIN.          |
| Métodos IPin                                                                    | Descripción                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Enumera los tipos de medios preferidos del PIN.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




