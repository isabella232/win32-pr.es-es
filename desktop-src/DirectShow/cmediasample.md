---
description: La clase CMediaSample define un ejemplo multimedia que admite la interfaz IMediaSample2. El ejemplo multimedia contiene un puntero a un búfer de memoria y varias propiedades almacenadas como variables de miembro protegidas.
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: Clase CMediaSample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72cfe0f86ff6b6643f2f7793822899136a5c6454
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670323"
---
# <a name="cmediasample-class"></a>Clase CMediaSample

![jerarquía de clases cmediasample](images/wutil03.png)

La `CMediaSample` clase define un ejemplo multimedia que admite la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) . El ejemplo multimedia contiene un puntero a un búfer de memoria y varias propiedades almacenadas como variables de miembro protegidas.

Los ejemplos de medios se crean mediante asignadores, que se derivan de la clase [**CBaseAllocator**](cbaseallocator.md) . El `CMediaSample` constructor recibe un puntero a un búfer asignado, junto con el tamaño del búfer. Normalmente, se establecen y recuperan otras propiedades a través de los métodos de la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .

El ciclo de vida de un ejemplo multimedia difiere del de la mayoría de los objetos COM:

-   El asignador contiene una lista de ejemplos gratuitos. Cuando un filtro necesita un nuevo ejemplo, llama al método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) del asignador. El asignador recupera un ejemplo de su lista libre, incrementa el recuento de referencias del ejemplo y devuelve un puntero al ejemplo.
-   Una vez que el filtro se realiza con el ejemplo, llama al método **IUnknown:: Release** en el ejemplo. A diferencia de la mayoría de los objetos, el ejemplo no se elimina a sí mismo cuando su recuento de referencias llega a cero. En su lugar, llama al método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) en el asignador y el asignador devuelve el ejemplo a su lista libre.
-   El asignador no destruye los ejemplos hasta que se llama al método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .



| Variables de miembro protegidas                                           | Descripción                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**m \_ dwFlags**](cmediasample-m-dwflags.md)                         | Marcas de propiedades de ejemplo.                                                                          |
| [**m \_ dwTypeSpecificFlags**](cmediasample-m-dwtypespecificflags.md) | Marcas específicas del tipo.                                                                            |
| [**m \_ pBuffer**](cmediasample-m-pbuffer.md)                         | Puntero al búfer de memoria que contiene los datos multimedia.                                      |
| [**m \_ lActual**](cmediasample-m-lactual.md)                         | Longitud de los datos válidos en el búfer, en bytes.                                               |
| [**m \_ cbBuffer**](cmediasample-m-cbbuffer.md)                       | Tamaño del búfer, en bytes.                                                                   |
| [**m \_ pAllocator**](cmediasample-m-pallocator.md)                   | Puntero al asignador que creó este ejemplo.                                              |
| [**m \_ pNext**](cmediasample-m-pnext.md)                             | Puntero al siguiente ejemplo de la lista de ejemplos del asignador.                                  |
| [**\_Inicio m**](cmediasample-m-start.md)                             | Hora de inicio de ejemplo.                                                                              |
| [**\_fin m**](cmediasample-m-end.md)                                 | Hora de finalización de ejemplo.                                                                                |
| [**m \_ MediaStart**](cmediasample-m-mediastart.md)                   | Hora de inicio del medio.                                                                               |
| [**m \_ MediaEnd**](cmediasample-m-mediaend.md)                       | Hora de detención del medio.                                                                                |
| [**m \_ pMediaType**](cmediasample-m-pmediatype.md)                   | Puntero al tipo de medio, si el tipo ha cambiado respecto al ejemplo anterior en el flujo de datos. |
| [**m \_ dwStreamId**](cmediasample-m-dwstreamid.md)                   | Identificador de flujo.                                                                              |
| Variables de miembro público                                              | Descripción                                                                                     |
| [**m \_ cRef**](cmediasample-m-cref.md)                               | Recuento de referencias.                                                                                |
| Métodos públicos                                                       | Descripción                                                                                     |
| [**CMediaSample**](cmediasample-cmediasample.md)                    | Método de constructor.                                                                             |
| [**~ CMediaSample**](cmediasample--cmediasample.md)                 | Método de destructor. Virtualiza.                                                                     |
| [**SetPointer**](cmediasample-setpointer.md)                        | Establece el puntero en el búfer de memoria.                                                          |
| Métodos IMediaSample                                                 | Descripción                                                                                     |
| [**GetPointer**](cmediasample-getpointer.md)                        | Recupera un puntero de lectura/escritura en el búfer.                                                   |
| [**GetSize (**](cmediasample-getsize.md)                              | Recupera el tamaño del búfer.                                                               |
| [**GetTime**](cmediasample-gettime.md)                              | Recupera los tiempos de flujo en los que este ejemplo debe comenzar y finalizar.                        |
| [**SetTime**](cmediasample-settime.md)                              | Establece los tiempos de flujo en los que este ejemplo debe comenzar y finalizar.                             |
| [**IsSyncPoint**](cmediasample-issyncpoint.md)                      | Determina si el principio del ejemplo es un punto de sincronización.                           |
| [**SetSyncPoint**](cmediasample-setsyncpoint.md)                    | Especifica si el principio de este ejemplo es un punto de sincronización.                      |
| [**IsPreroll**](cmediasample-ispreroll.md)                          | Determina si este ejemplo es un ejemplo de relanzamiento.                                                  |
| [**SetPreroll**](cmediasample-setpreroll.md)                        | Especifica si este ejemplo es un ejemplo de relanzamiento.                                              |
| [**GetActualDataLength**](cmediasample-getactualdatalength.md)      | Recupera la longitud de los datos válidos en el búfer.                                           |
| [**SetActualDataLength**](cmediasample-setactualdatalength.md)      | Establece la longitud de los datos válidos en el búfer.                                                |
| [**GetMediaType**](cmediasample-getmediatype.md)                    | Recupera el tipo de medio si el tipo de medio es distinto del ejemplo anterior.                   |
| [**SetMediaType**](cmediasample-setmediatype.md)                    | Establece el tipo de medio para el ejemplo.                                                             |
| [**IsDiscontinuity**](cmediasample-isdiscontinuity.md)              | Determina si este ejemplo representa una interrupción en el flujo de datos.                                |
| [**SetDiscontinuity**](cmediasample-setdiscontinuity.md)            | Especifica si este ejemplo representa una interrupción en el flujo de datos.                            |
| [**GetMediaTime**](cmediasample-getmediatime.md)                    | Recupera las horas de los medios de este ejemplo.                                                      |
| [**SetMediaTime**](cmediasample-setmediatime.md)                    | Establece las horas de los medios para este ejemplo.                                                           |
| Métodos IMediaSample2                                                | Descripción                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | Recupera las propiedades del ejemplo.                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | Establece las propiedades del ejemplo.                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




