---
description: La clase CTransformOutputPin implementa un pin de salida que usa la clase CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: CTransformOutputPin (clase, Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255326"
---
# <a name="ctransformoutputpin-class"></a>CTransformOutputPin (clase)

![Jerarquía de clases ctransformoutputpin](images/tfrm02.png)

La `CTransformOutputPin` clase implementa un pin de salida que usa la clase [**CTransformFilter.**](ctransformfilter.md)

Normalmente, no es necesario derivar de esta clase. La mayoría de los métodos de esta clase llaman a los métodos correspondientes en la **clase CTransformFilter,** que puede invalidar. Si deriva de esta clase, debe invalidar el método [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) del filtro para crear instancias de la clase derivada.

Esta clase expone las interfaces **IMediaSeeking** e **IMediaPosition** a través [**del objeto CPosPassThru.**](cpospassthru.md) Pasa todas las solicitudes de búsqueda al siguiente filtro ascendente.



| Variables miembro protegidas                                               | Descripción                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransformoutputpin-m-ptransformfilter.md)    | Puntero al filtro propietario.                            |
| Variables de miembro público                                                  | Descripción                                              |
| [**m \_ pPosition**](ctransformoutputpin-m-pposition.md)                  | Objeto auxiliar para pasar comandos seek ascendentes.            |
| Métodos públicos                                                           | Descripción                                              |
| [**CTransformOutputPin**](ctransformoutputpin-ctransformoutputpin.md)   | Método constructor.                                      |
| [**~CTransformOutputPin**](ctransformoutputpin--ctransformoutputpin.md) | Método destructor.                                       |
| [**CheckConnect**](ctransformoutputpin-checkconnect.md)                 | Determina si una conexión de pin es adecuada.         |
| [**BreakConnect**](ctransformoutputpin-breakconnect.md)                 | Libera el pin de una conexión.                      |
| [**CompleteConnect**](ctransformoutputpin-completeconnect.md)           | Completa una conexión a otro pin.                   |
| [**CheckMediaType**](ctransformoutputpin-checkmediatype.md)             | Determina si el pin acepta un tipo de medio específico.     |
| [**SetMediaType**](ctransformoutputpin-setmediatype.md)                 | Establece el tipo de medio para la conexión.                  |
| [**DecideBufferSize**](ctransformoutputpin-decidebuffersize.md)         | Establece los requisitos del búfer.                            |
| [**GetMediaType**](ctransformoutputpin-getmediatype.md)                 | Recupera un tipo de medio preferido, por valor de índice.        |
| [**CurrentMediaType**](ctransformoutputpin-currentmediatype.md)         | Recupera el tipo de medio para la conexión de pin actual. |
| Métodos de IPin                                                             | Descripción                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | Recupera un identificador para el pin.                     |
| Métodos IQualityControl                                                  | Descripción                                              |
| [**Notificar**](ctransformoutputpin-notify.md)                             | Notifica al pin que se solicita un cambio de calidad.     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




