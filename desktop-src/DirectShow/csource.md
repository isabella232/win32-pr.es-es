---
description: La clase CSource es una clase base para la implementación de filtros de origen. Un filtro derivado de CSource contiene uno o varios PIN de salida derivados de la clase CSourceStream. Cada pin de salida crea un subproceso de trabajo que envía muestras de multimedia de bajada.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Clase CSource (Source. h)
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
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690532"
---
# <a name="csource-class"></a>Clase CSource

![jerarquía de clases csource](images/source01.png)

La clase **CSource** es una clase base para la implementación de filtros de origen. Un filtro derivado de **CSource** contiene uno o varios PIN de salida derivados de la clase [**CSourceStream**](csourcestream.md) . Cada pin de salida crea un subproceso de trabajo que envía muestras de multimedia de bajada.

> [!Note]  
> La clase **CSource** está diseñada para admitir el modelo de entrada para el flujo de datos. Esta clase no se recomienda para crear filtros de lector de archivos. Los lectores de archivos deben admitir el modelo de extracción a través de la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Para obtener más información, vea [flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md).

 



| Variables de miembro protegidas                     | Descripción                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**m \_ iPins**](csource-m-ipins.md)            | Número de clavijas en el filtro.                                |
| [**m en las \_ secuencias**](csource-m-pastreams.md)    | Matriz de clavijas.                                               |
| [**m \_ cStateLock**](csource-m-cstatelock.md)  | Objeto de sección crítica que protege el estado del filtro.      |
| Métodos públicos                                 | Descripción                                                  |
| [**CSource**](csource-csource.md)             | Método de constructor.                                          |
| [**~ CSource**](csource--csource.md)           | Método de destructor.                                           |
| [**GetPinCount**](csource-getpincount.md)     | Recupera el número de clavijas del filtro.                  |
| [**GetPin**](csource-getpin.md)               | Recupera un código PIN.                                             |
| [**pStateLock**](csource--pstatelock.md)      | Recupera un puntero al objeto de sección crítica del filtro. |
| [**AddPin**](csource-addpin.md)               | Agrega un nuevo PIN de salida al filtro.                         |
| [**RemovePin**](csource-removepin.md)         | Quita un punto de conexión especificado del filtro.                     |
| [**FindPinNumber**](csource-findpinnumber.md) | Recupera el número de un PIN especificado en el filtro.       |
| Métodos IBaseFilter                            | Descripción                                                  |
| [**FindPin**](csource-findpin.md)             | Recupera el pin con el identificador especificado.             |



 

## <a name="remarks"></a>Observaciones

Para implementar un PIN de salida, haga lo siguiente:

-   Derive una clase de [**CSourceStream**](csourcestream.md).
-   Invalide el método [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) y, posiblemente, el método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) , que valida los tipos de medios para el PIN.
-   Implemente el método [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , que devuelve los requisitos de búfer del PIN.
-   Implemente el método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , que rellena un búfer de ejemplo multimedia con datos.

Para implementar el filtro, haga lo siguiente:

-   Derive una clase de **CSource**.
-   En el constructor, cree uno o varios PIN de salida derivados de [**CSourceStream**](csourcestream.md). Los PIN se agregan automáticamente al filtro en sus métodos de constructor y se quitan a sí mismos en sus métodos de destructor.

Para sincronizar el estado del filtro entre varios subprocesos, llame al método [**CSource::P statelock**](csource--pstatelock.md) . Este método devuelve un puntero a la sección crítica de estado de filtro. Use la clase [**CAutoLock**](cautolock.md) para almacenar la sección crítica. Desde un PIN, puede acceder a **pStateLock** desde la variable miembro [**CBasePin:: m \_ pFilter**](cbasepin-m-pfilter.md) del PIN, como se indica a continuación:


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escribir filtros de origen](writing-source-filters.md)
</dt> </dl>

 

 




