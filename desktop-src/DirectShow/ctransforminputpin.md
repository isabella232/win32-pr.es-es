---
description: La clase CTransformInputPin implementa un pin de entrada que usa la clase CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: CTransformInputPin (clase, Transfrm.h)
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
ms.openlocfilehash: 3df5da0ee6e80dd1da147563ef698a520222531de5cee9656ec52cb14301f66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087024"
---
# <a name="ctransforminputpin-class"></a>CTransformInputPin (clase)

![Jerarquía de clases ctransforminputpin](images/tfrm01.png)

La `CTransformInputPin` clase implementa un pin de entrada que usa la clase [**CTransformFilter.**](ctransformfilter.md)

Normalmente, no es necesario derivar de esta clase. La mayoría de los métodos de esta clase llaman a los métodos correspondientes en la **clase CTransformFilter,** que puede invalidar. Si deriva de esta clase, debe invalidar el método [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) del filtro para crear instancias de la clase derivada.



| Variables miembro protegidas                                           | Descripción                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransforminputpin-m-ptransformfilter.md) | Puntero al filtro propietario.                                                          |
| Métodos públicos                                                       | Descripción                                                                            |
| [**CTransformInputPin**](ctransforminputpin-ctransforminputpin.md)  | Método constructor.                                                                    |
| [**CheckConnect**](ctransforminputpin-checkconnect.md)              | Determina si una conexión de pin es adecuada.                                       |
| [**BreakConnect**](ctransforminputpin-breakconnect.md)              | Libera el pin de una conexión.                                                    |
| [**CompleteConnect**](ctransforminputpin-completeconnect.md)        | Completa una conexión a otro pin.                                                 |
| [**CheckMediaType**](ctransforminputpin-checkmediatype.md)          | Determina si el pin acepta un tipo de medio específico.                                   |
| [**SetMediaType**](ctransforminputpin-setmediatype.md)              | Establece el tipo de medio para la conexión.                                                |
| [**CheckStreaming**](ctransforminputpin-checkstreaming.md)          | Determina si el pin puede aceptar ejemplos. Virtual.                                |
| [**CurrentMediaType**](ctransforminputpin-currentmediatype.md)      | Recupera el tipo de medio para la conexión de pin actual.                               |
| Métodos de IPin                                                         | Descripción                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | Recupera un identificador para el pin.                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | Notifica al pin que no se espera ningún dato adicional.                                  |
| [**BeginFlush**](ctransforminputpin-beginflush.md)                  | Comienza una operación de vaciado.                                                              |
| [**EndFlush**](ctransforminputpin-endflush.md)                      | Finaliza una operación de vaciado.                                                                |
| [**NewSegment**](ctransforminputpin-newsegment.md)                  | Notifica al pin que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento. |
| Métodos IMemInputPin                                                 | Descripción                                                                            |
| [**Recibir**](ctransforminputpin-receive.md)                        | Recibe el siguiente ejemplo multimedia en la secuencia.                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




