---
description: 'La clase CTransInPlaceFilter está diseñada para los filtros de transformación en contexto, que son filtros que modifican los datos de entrada en lugar de copiar los datos entre búferes. Para usar esta clase, derive una nueva clase de CTransInPlaceFilter e implemente los métodos siguientes:'
ms.assetid: 3d6d5436-f280-4e36-96e4-40161e8115c2
title: Clase CTransInPlaceFilter (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f59dd312adbb95797caf695aecea082f296df5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680742"
---
# <a name="ctransinplacefilter-class"></a>Clase CTransInPlaceFilter

![jerarquía de clases ctransinplacefilter](images/tsip03.png)

La `CTransInPlaceFilter` clase está diseñada para los filtros de transformación en contexto, que son filtros que modifican los datos de entrada en lugar de copiar los datos entre búferes. Para usar esta clase, derive una nueva clase de `CTransInPlaceFilter` e implemente los métodos siguientes:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransInPlaceFilter:: transform**](ctransinplacefilter-transform.md)

Esta clase usa la clase [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) para su PIN de entrada y la clase [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) para su PIN de salida. Normalmente, no es necesario invalidar estas clases de PIN. El filtro crea ambos PIN en el método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) . Si invalida las clases de PIN, debe invalidar **GetPin** para crear los pin personalizados.

Esta clase está diseñada para que el tipo de entrada coincida siempre con el tipo de salida. Siempre que sea posible, el filtro utiliza un único asignador para ambas conexiones de PIN.

## <a name="preferred-media-types"></a>Tipos de medios preferidos

Si el PIN de salida ya está conectado, el PIN de entrada ofrece los tipos preferidos del filtro de nivel inferior. (En realidad, simplemente devuelve el objeto de enumerador del filtro de nivel inferior). De lo contrario, no tiene tipos preferidos. El PIN de salida tiene el mismo comportamiento, pero en orden inverso: Si el PIN de entrada ya está conectado, el PIN de salida ofrece los tipos preferidos del filtro de nivel superior. De lo contrario, no tiene tipos preferidos

## <a name="pin-connections"></a>Anclar conexiones

Cuando se conecta un PIN, el filtro generalmente vuelve a conectar el otro, para asegurarse de que ambos PIN usan el mismo tipo de medio y el mismo asignador. (El mecanismo para volver a conectar los PIN se describe en [reconectar PIN](reconnecting-pins.md)). Existen dos escenarios posibles: el PIN de entrada se conecta primero, o bien el PIN de salida se conecta primero.

Supongamos que el PIN de entrada se conecta primero. Tienen lugar los pasos siguientes:

1.  El PIN de entrada llama al método [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de medio.
2.  El filtro de nivel superior selecciona un asignador. En este momento, el PIN de entrada no tiene ningún requisito de asignador y acepta cualquier asignador para la conexión. Si el filtro de nivel superior solicita un asignador, el PIN crea uno nuevo. Por motivos descritos en breve, este asignador no se utilizará en la conexión final. Solo se proporciona para ayudar a finalizar esta fase del proceso de conexión.

Más adelante, cuando se conecte el PIN de salida:

1.  El PIN de salida llama al método [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de medio. También llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el filtro de nivel superior. Esto garantiza que el PIN de entrada puede cambiar su tipo de medio para que coincida.
2.  El PIN de salida llama al método [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de medio. También llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el filtro de nivel superior. Esto garantiza que el PIN de entrada puede cambiar su tipo de medio para que coincida.
3.  El PIN de salida llama al método [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de medio. También llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el filtro de nivel superior. Esto garantiza que el PIN de entrada puede cambiar su tipo de medio para que coincida.
4.  Esta vez, el método [**GetAllocator**](ctransinplaceinputpin-getallocator.md) del PIN de entrada devuelve el asignador de bajada y [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) devuelve los requisitos del asignador del filtro de nivel inferior. El PIN de entrada acepta cualquier asignador que elija el filtro de nivel superior.
5.  Esta vez, el método [**GetAllocator**](ctransinplaceinputpin-getallocator.md) del PIN de entrada devuelve el asignador de bajada y [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) devuelve los requisitos del asignador del filtro de nivel inferior. El PIN de entrada acepta cualquier asignador que elija el filtro de nivel superior.

Ahora considere el escenario opuesto, donde el PIN de salida es el primer PIN que se va a conectar.

1.  El PIN de salida llama al método [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de medio.
2.  Selecciona un asignador y prefiere usar el asignador del filtro de nivel inferior.

Después, cuando se conecta el PIN de entrada:

1.  El PIN de entrada comprueba el tipo de medio llamando a [**CheckInputType**](ctransformfilter-checkinputtype.md) en el filtro y llamando a [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de salida del filtro de nivel inferior.
2.  Si el tipo de entrada no coincide con el tipo de salida, el filtro vuelve a conectar el terminal de salida.
3.  El filtro de nivel superior selecciona un asignador. El método [**GetAllocator**](ctransinplaceinputpin-getallocator.md) del PIN de entrada devuelve el asignador de bajada y el PIN de entrada acepta cualquier asignador que seleccione el filtro de nivel superior.
4.  El filtro usa el mismo asignador para la conexión de nivel inferior, posiblemente invalidando el asignador de bajada original.

Esta secuencia de eventos cambia ligeramente si alguno de los asignadores implicados es de solo lectura, porque el asignador de bajada debe ser grabable. En ese caso, el filtro podría usar dos asignadores independientes.

Para obtener más información sobre el uso de esta clase, vea [escribir filtros de transformación](writing-transform-filters.md).



| Variables de miembro protegidas                                                        | Descripción                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**m \_ bModifiesData**](ctransinplacefilter-m-bmodifiesdata.md)                   | Indica si el filtro modifica los datos de ejemplo.                           |
| Métodos protegidos                                                                 | Descripción                                                                      |
| [**Copiar**](ctransinplacefilter-copy.md)                                          | Copia un ejemplo multimedia.                                                           |
| [**InputPin**](ctransinplacefilter-inputpin.md)                                  | Recupera un puntero al pin de entrada del filtro.                                   |
| [**OutputPin**](ctransinplacefilter-outputpin.md)                                | Recupera un puntero a la clavija de salida del filtro.                                  |
| [**TypesMatch**](ctransinplacefilter-typesmatch.md)                              | Determina si el tipo de medio de entrada coincide con el tipo de medio de salida.           |
| [**UsingDifferentAllocators**](ctransinplacefilter--usingdifferentallocators.md) | Determina si los pin de entrada y salida están usando asignadores diferentes.     |
| Métodos públicos                                                                    | Descripción                                                                      |
| [**CTransInPlaceFilter**](ctransinplacefilter-ctransinplacefilter.md)            | Método de constructor.                                                              |
| [**GetPin**](ctransinplacefilter-getpin.md)                                      | Recupera un código PIN.                                                                 |
| [**GetMediaType**](ctransinplacefilter-getmediatype.md)                          | Recupera un tipo de medio preferido para el PIN de salida.                             |
| [**DecideBufferSize**](ctransinplacefilter-decidebuffersize.md)                  | Establece los requisitos de búfer del PIN de salida.                                       |
| [**CheckTransform**](ctransinplacefilter-checktransform.md)                      | Comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.      |
| [**CompleteConnect**](ctransinplacefilter-completeconnect.md)                    | Completa una conexión de PIN.                                                      |
| [**Aparecen**](ctransinplacefilter-receive.md)                                    | Recibe un ejemplo multimedia, lo procesa y lo entrega al filtro de nivel inferior. |
| Métodos virtuales puros                                                              | Descripción                                                                      |
| [**Transform**](ctransinplacefilter-transform.md)                                | Transforma un ejemplo en su lugar.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




