---
description: La clase CTransInPlaceOutputPin implementa un pin de salida que usa la clase CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: CTransInPlaceOutputPin (clase, Transip.h)
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
ms.openlocfilehash: 2462843f9ad42793a9e0666dd96aaf7387a1f5f0f1749f97cc4e2ca4d3ed051a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076164"
---
# <a name="ctransinplaceoutputpin-class"></a>CTransInPlaceOutputPin (clase)

![ctransinplaceoutputpin (jerarquía de clases)](images/tsip02.png)

La `CTransInPlaceOutputPin` clase implementa un pin de salida que usa la clase [**CTransInPlaceFilter.**](ctransinplacefilter.md)

Normalmente, no es necesario derivar de esta clase. Si lo hace, debe invalidar el método [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) del filtro para crear instancias de la clase derivada.



| Variables miembro protegidas                                                      | Descripción                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ pTIPFilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Puntero al filtro que creó este pin.         |
| Métodos públicos                                                                  | Descripción                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Método constructor.                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | Determina si el pin acepta un tipo de medio específico. |
| [**SetAllocator**](ctransinplaceoutputpin-setallocator.md)                     | Especifica un asignador para la conexión.           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Recupera un puntero a la patilla de entrada de bajada.     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | Recupera un puntero al asignador del pin.          |
| Métodos de IPin                                                                    | Descripción                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Enumera los tipos de medios preferidos del pin.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




