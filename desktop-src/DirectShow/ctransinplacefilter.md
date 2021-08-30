---
description: 'La clase CTransInPlaceFilter está diseñada para filtros de transformación locales, que son filtros que modifican los datos de entrada en lugar de copiar los datos entre búferes. Para usar esta clase, derive una nueva clase de CTransInPlaceFilter e implemente los métodos siguientes:'
ms.assetid: 3d6d5436-f280-4e36-96e4-40161e8115c2
title: CTransInPlaceFilter (clase, Transip.h)
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
ms.openlocfilehash: 575a4433318a2c956f4585270b0ff329f40cdff37f6b9f6553b895b58c6a3e34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086984"
---
# <a name="ctransinplacefilter-class"></a>CTransInPlaceFilter (clase)

![Jerarquía de clases ctransinplacefilter](images/tsip03.png)

La clase está diseñada para filtros de transformación locales, que son filtros que modifican los datos de entrada en lugar de copiar los datos entre `CTransInPlaceFilter` búferes. Para usar esta clase, derive una nueva clase de `CTransInPlaceFilter` e implemente los métodos siguientes:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md)

Esta clase usa la [**clase CTransInPlaceInputPin**](ctransinplaceinputpin.md) para su pin de entrada y la clase [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) para su pin de salida. Normalmente, no es necesario invalidar estas clases de pin. El filtro crea ambos pines en el [**método CTransInPlaceFilter::GetPin.**](ctransinplacefilter-getpin.md) Si invalida las clases de pin, debe invalidar **GetPin** para crear los pines personalizados.

Esta clase está diseñada para que el tipo de entrada siempre coincida con el tipo de salida. Siempre que sea posible, el filtro usa un solo asignador para ambas conexiones de pin.

## <a name="preferred-media-types"></a>Tipos de medios preferidos

Si el pin de salida ya está conectado, el pin de entrada ofrece los tipos preferidos del filtro de bajada. (De hecho, simplemente devuelve el objeto enumerador del filtro de bajada). De lo contrario, no tiene tipos preferidos. El pin de salida tiene el mismo comportamiento, pero a la inversa: si el pin de entrada ya está conectado, el pin de salida ofrece los tipos preferidos del filtro ascendente. De lo contrario, no tiene tipos preferidos

## <a name="pin-connections"></a>Anclar conexiones

Cuando se conecta un pin, el filtro suele volver a conectar el otro pin para asegurarse de que ambos pin usan el mismo tipo de medio y el mismo asignador. (El mecanismo para volver a conectar los pines se describe en [Volver a conectar los pines).](reconnecting-pins.md) Son posibles dos escenarios: el pin de entrada se conecta primero o el pin de salida se conecta primero.

Supongamos que el pin de entrada se conecta primero. Tienen lugar los pasos siguientes:

1.  El pin de entrada llama al [**método CheckInputType del**](ctransformfilter-checkinputtype.md) filtro para comprobar el tipo de medio.
2.  El filtro ascendente selecciona un asignador. En este momento, el pin de entrada no tiene requisitos de asignador y acepta cualquier asignador para la conexión. Si el filtro ascendente solicita un asignador, el pin crea uno nuevo. Por los motivos descritos en breve, este asignador no se usará en la conexión final. Solo se proporciona para ayudar a finalizar esta fase del proceso de conexión.

Más adelante, cuando se conecte el pin de salida:

1.  El pin de salida llama al método [**CheckInputType del**](ctransformfilter-checkinputtype.md) filtro para comprobar el tipo de medio. También llama a [**IPin::QueryAccept en**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) el filtro ascendente. Esto garantiza que el pin de entrada puede cambiar su tipo de medio para que coincida.
2.  El pin de salida llama al método [**CheckInputType del**](ctransformfilter-checkinputtype.md) filtro para comprobar el tipo de medio. También llama a [**IPin::QueryAccept en**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) el filtro ascendente. Esto garantiza que el pin de entrada puede cambiar su tipo de medio para que coincida.
3.  El pin de salida llama al método [**CheckInputType del**](ctransformfilter-checkinputtype.md) filtro para comprobar el tipo de medio. También llama a [**IPin::QueryAccept en**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) el filtro ascendente. Esto garantiza que el pin de entrada puede cambiar su tipo de medio para que coincida.
4.  Esta vez, el método [**GetAllocator**](ctransinplaceinputpin-getallocator.md) del pin de entrada devuelve el asignador de nivel inferior y [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) devuelve los requisitos de asignador del filtro de bajada. El pin de entrada acepta el asignador que elija el filtro ascendente.
5.  Esta vez, el método [**GetAllocator**](ctransinplaceinputpin-getallocator.md) del pin de entrada devuelve el asignador de nivel inferior y [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) devuelve los requisitos de asignador del filtro de bajada. El pin de entrada acepta el asignador que elija el filtro ascendente.

Ahora considere el escenario opuesto, donde el pin de salida es el primer pin para conectarse.

1.  El pin de salida llama al método [**CheckInputType del**](ctransformfilter-checkinputtype.md) filtro para comprobar el tipo de medio.
2.  Selecciona un asignador y prefiere usar el asignador del filtro de nivel inferior.

A continuación, cuando se conecta el pin de entrada:

1.  El pin de entrada comprueba el tipo de medio llamando a [**CheckInputType**](ctransformfilter-checkinputtype.md) en el filtro y llamando a [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el pin de salida del filtro de bajada.
2.  Si el tipo de entrada no coincide con el tipo de salida, el filtro vuelve a conectar el pin de salida.
3.  El filtro ascendente selecciona un asignador. El método [**GetAllocator**](ctransinplaceinputpin-getallocator.md) del pin de entrada devuelve el asignador de nivel inferior y el pin de entrada acepta cualquier asignador que seleccione el filtro ascendente.
4.  El filtro usa el mismo asignador para la conexión de bajada, posiblemente invalidando el asignador de bajada original.

Esta secuencia de eventos cambia ligeramente si alguno de los asignadores implicados es de solo lectura, porque el asignador de nivel inferior debe poder escribirse. En ese caso, el filtro podría usar dos asignadores independientes.

Para obtener más información sobre el uso de esta clase, vea [Escribir filtros de transformación](writing-transform-filters.md).



| Variables de miembro protegido                                                        | Descripción                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**m \_ bModifiesData**](ctransinplacefilter-m-bmodifiesdata.md)                   | Indica si el filtro modifica los datos de ejemplo.                           |
| Métodos protegidos                                                                 | Descripción                                                                      |
| [**Copiar**](ctransinplacefilter-copy.md)                                          | Copia un ejemplo multimedia.                                                           |
| [**InputPin**](ctransinplacefilter-inputpin.md)                                  | Recupera un puntero al pin de entrada del filtro.                                   |
| [**OutputPin**](ctransinplacefilter-outputpin.md)                                | Recupera un puntero al pin de salida del filtro.                                  |
| [**TypesMatch**](ctransinplacefilter-typesmatch.md)                              | Determina si el tipo de medio de entrada coincide con el tipo de medio de salida.           |
| [**UsingDifferentAllocators**](ctransinplacefilter--usingdifferentallocators.md) | Determina si las clavijas de entrada y salida usan distintos asignadores.     |
| Métodos públicos                                                                    | Descripción                                                                      |
| [**CTransInPlaceFilter**](ctransinplacefilter-ctransinplacefilter.md)            | Método constructor.                                                              |
| [**GetPin**](ctransinplacefilter-getpin.md)                                      | Recupera un pin.                                                                 |
| [**GetMediaType**](ctransinplacefilter-getmediatype.md)                          | Recupera un tipo de medio preferido para el pin de salida.                             |
| [**DecideBufferSize**](ctransinplacefilter-decidebuffersize.md)                  | Establece los requisitos de búfer del pin de salida.                                       |
| [**CheckTransform**](ctransinplacefilter-checktransform.md)                      | Comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.      |
| [**CompleteConnect**](ctransinplacefilter-completeconnect.md)                    | Completa una conexión de pin.                                                      |
| [**Recibir**](ctransinplacefilter-receive.md)                                    | Recibe un ejemplo multimedia, lo procesa y lo entrega al filtro de nivel inferior. |
| Métodos virtuales puros                                                              | Descripción                                                                      |
| [**Transform**](ctransinplacefilter-transform.md)                                | Transforma un ejemplo en su lugar.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




