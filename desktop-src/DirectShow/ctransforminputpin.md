---
description: La clase CTransformInputPin implementa un PIN de entrada usado por la clase CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Clase CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661315"
---
# <a name="ctransforminputpin-class"></a>Clase CTransformInputPin

![jerarquía de clases ctransforminputpin](images/tfrm01.png)

La `CTransformInputPin` clase implementa un PIN de entrada usado por la clase [**CTransformFilter**](ctransformfilter.md) .

Normalmente, no es necesario derivar de esta clase. La mayoría de los métodos de esta clase llaman a los métodos correspondientes en la clase **CTransformFilter** , que puede invalidar. Si deriva de esta clase, debe invalidar el método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) del filtro para crear instancias de la clase derivada.



| Variables de miembro protegidas                                           | Descripción                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransforminputpin-m-ptransformfilter.md) | Puntero al filtro propietario.                                                          |
| Métodos públicos                                                       | Descripción                                                                            |
| [**CTransformInputPin**](ctransforminputpin-ctransforminputpin.md)  | Método de constructor.                                                                    |
| [**CheckConnect**](ctransforminputpin-checkconnect.md)              | Determina si una conexión de PIN es adecuada.                                       |
| [**BreakConnect**](ctransforminputpin-breakconnect.md)              | Libera el PIN de una conexión.                                                    |
| [**CompleteConnect**](ctransforminputpin-completeconnect.md)        | Completa una conexión a otro PIN.                                                 |
| [**CheckMediaType**](ctransforminputpin-checkmediatype.md)          | Determina si el PIN acepta un tipo de medio específico.                                   |
| [**SetMediaType**](ctransforminputpin-setmediatype.md)              | Establece el tipo de medio para la conexión.                                                |
| [**CheckStreaming**](ctransforminputpin-checkstreaming.md)          | Determina si el pin puede aceptar ejemplos. Virtualiza.                                |
| [**CurrentMediaType**](ctransforminputpin-currentmediatype.md)      | Recupera el tipo de medio para la conexión del PIN actual.                               |
| Métodos IPin                                                         | Descripción                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | Recupera un identificador para el código PIN.                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | Notifica al pin que no se espera ningún dato adicional.                                  |
| [**BeginFlush**](ctransforminputpin-beginflush.md)                  | Comienza una operación de vaciado.                                                              |
| [**EndFlush**](ctransforminputpin-endflush.md)                      | Finaliza una operación de vaciado.                                                                |
| [**NewSegment**](ctransforminputpin-newsegment.md)                  | Notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento. |
| Métodos IMemInputPin                                                 | Descripción                                                                            |
| [**Aparecen**](ctransforminputpin-receive.md)                        | Recibe el siguiente ejemplo multimedia en la secuencia.                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




