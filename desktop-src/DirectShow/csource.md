---
description: La clase CSource es una clase base para implementar filtros de origen. Un filtro derivado de CSource contiene uno o varios pins de salida derivados de la clase CSourceStream. Cada pin de salida crea un subproceso de trabajo que inserta muestras de medios de bajada.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: CSource (clase, Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6708ce38c826aae9ccb40d077972d267a20d5e22b4f67157000c4a62e92afa1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687524"
---
# <a name="csource-class"></a>CSource (clase)

![Jerarquía de clases de csource](images/source01.png)

La **clase CSource** es una clase base para implementar filtros de origen. Un filtro derivado de **CSource** contiene uno o varios pins de salida derivados de la [**clase CSourceStream.**](csourcestream.md) Cada pin de salida crea un subproceso de trabajo que inserta muestras de medios de bajada.

> [!Note]  
> La **clase CSource** está diseñada para admitir el modelo de inserción para el flujo de datos. Esta clase no se recomienda para crear filtros de lector de archivos. Los lectores de archivos deben admitir el modelo de extracción a través de [**la interfaz IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Para obtener más información, vea [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

 



| Variables de miembro protegido                     | Descripción                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**m \_ iPins**](csource-m-ipins.md)            | Número de pines en el filtro.                                |
| [**m \_ paStreams**](csource-m-pastreams.md)    | Matriz de pines.                                               |
| [**m \_ cStateLock**](csource-m-cstatelock.md)  | Objeto de sección crítica que protege el estado del filtro.      |
| Métodos públicos                                 | Descripción                                                  |
| [**CSource**](csource-csource.md)             | Método constructor.                                          |
| [**~CSource**](csource--csource.md)           | Método destructor.                                           |
| [**GetPinCount**](csource-getpincount.md)     | Recupera el número de pines del filtro.                  |
| [**GetPin**](csource-getpin.md)               | Recupera un pin.                                             |
| [**pStateLock**](csource--pstatelock.md)      | Recupera un puntero al objeto de sección crítica del filtro. |
| [**AddPin**](csource-addpin.md)               | Agrega un nuevo pin de salida al filtro.                         |
| [**RemovePin**](csource-removepin.md)         | Quita un pin especificado del filtro.                     |
| [**FindPinNumber**](csource-findpinnumber.md) | Recupera el número de un pin especificado en el filtro.       |
| Métodos IBaseFilter                            | Descripción                                                  |
| [**FindPin**](csource-findpin.md)             | Recupera el pin con el identificador especificado.             |



 

## <a name="remarks"></a>Comentarios

Para implementar un pin de salida, haga lo siguiente:

-   Derive una clase de [**CSourceStream**](csourcestream.md).
-   Invalide [**el método CSourceStream::GetMediaType**](csourcestream-getmediatype.md) y, posiblemente, el método [**CSourceStream::CheckMediaType,**](csourcestream-checkmediatype.md) que valida los tipos de medios para el pin.
-   Implemente [**el método CBaseOutputPin::D ecideBufferSize,**](cbaseoutputpin-decidebuffersize.md) que devuelve los requisitos de búfer del pin.
-   Implemente [**el método CSourceStream::FillBuffer,**](csourcestream-fillbuffer.md) que rellena un búfer de ejemplo multimedia con datos.

Para implementar el filtro, haga lo siguiente:

-   Derive una clase de **CSource**.
-   En el constructor, cree uno o varios pins de salida derivados de [**CSourceStream.**](csourcestream.md) Los pines se agregan automáticamente al filtro en sus métodos de constructor y se quitan ellos mismos en sus métodos destructores.

Para sincronizar el estado de filtro entre varios subprocesos, llame al [**método CSource::p StateLock.**](csource--pstatelock.md) Este método devuelve un puntero a la sección crítica de estado de filtro. Use la [**clase CAutoLock**](cautolock.md) para contener la sección crítica. Desde un pin, puede acceder **a pStateLock** desde la variable miembro [**CBasePin::m \_ pFilter**](cbasepin-m-pfilter.md) del pin, como se muestra a continuación:


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escribir filtros de origen](writing-source-filters.md)
</dt> </dl>

 

 




