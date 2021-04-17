---
description: La clase CTransformOutputPin implementa un PIN de salida que se usa en la clase CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Clase CTransformOutputPin (Transfrm. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681107"
---
# <a name="ctransformoutputpin-class"></a>Clase CTransformOutputPin

![jerarquía de clases ctransformoutputpin](images/tfrm02.png)

La `CTransformOutputPin` clase implementa un PIN de salida que se usa en la clase [**CTransformFilter**](ctransformfilter.md) .

Normalmente, no es necesario derivar de esta clase. La mayoría de los métodos de esta clase llaman a los métodos correspondientes en la clase **CTransformFilter** , que puede invalidar. Si deriva de esta clase, debe invalidar el método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) del filtro para crear instancias de la clase derivada.

Esta clase expone las interfaces **IMediaSeeking** y **IMediaPosition** a través del objeto [**CPosPassThru**](cpospassthru.md) . Pasa todas las solicitudes de búsqueda al siguiente filtro ascendente.



| Variables de miembro protegidas                                               | Descripción                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransformoutputpin-m-ptransformfilter.md)    | Puntero al filtro propietario.                            |
| Variables de miembro público                                                  | Descripción                                              |
| [**m \_ pPosition**](ctransformoutputpin-m-pposition.md)                  | Objeto auxiliar para pasar comandos de búsqueda ascendentes.            |
| Métodos públicos                                                           | Descripción                                              |
| [**CTransformOutputPin**](ctransformoutputpin-ctransformoutputpin.md)   | Método de constructor.                                      |
| [**~ CTransformOutputPin**](ctransformoutputpin--ctransformoutputpin.md) | Método de destructor.                                       |
| [**CheckConnect**](ctransformoutputpin-checkconnect.md)                 | Determina si una conexión de PIN es adecuada.         |
| [**BreakConnect**](ctransformoutputpin-breakconnect.md)                 | Libera el PIN de una conexión.                      |
| [**CompleteConnect**](ctransformoutputpin-completeconnect.md)           | Completa una conexión a otro PIN.                   |
| [**CheckMediaType**](ctransformoutputpin-checkmediatype.md)             | Determina si el PIN acepta un tipo de medio específico.     |
| [**SetMediaType**](ctransformoutputpin-setmediatype.md)                 | Establece el tipo de medio para la conexión.                  |
| [**DecideBufferSize**](ctransformoutputpin-decidebuffersize.md)         | Establece los requisitos de búfer.                            |
| [**GetMediaType**](ctransformoutputpin-getmediatype.md)                 | Recupera un tipo de medio preferido, por valor de índice.        |
| [**CurrentMediaType**](ctransformoutputpin-currentmediatype.md)         | Recupera el tipo de medio para la conexión del PIN actual. |
| Métodos IPin                                                             | Descripción                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | Recupera un identificador para el código PIN.                     |
| Métodos IQualityControl                                                  | Descripción                                              |
| [**Notificar**](ctransformoutputpin-notify.md)                             | Notifica al pin que se ha solicitado un cambio de calidad.     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




