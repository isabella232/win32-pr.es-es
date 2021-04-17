---
description: La clase CBaseMediaFilter implementa la interfaz IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Clase CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670669"
---
# <a name="cbasemediafilter-class"></a>Clase CBaseMediaFilter

![cbasemediafilter](images/filter05.png)

La `CBaseMediaFilter` clase implementa la interfaz [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) . Use esta clase para distribuidores de complementos u otros objetos que necesiten admitir **IMediaFilter** sin admitir la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . No utilice esta clase para los filtros. En su lugar, use la clase [**CBaseFilter**](cbasefilter.md) o una clase base derivada de **CBaseFilter**.



| Variables de miembro protegidas                                       | Descripción                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_Estado m**](cbasemediafilter-m-state.md)                     | Estado actual del objeto.                                 |
| [**m \_ pClock**](cbasemediafilter-m-pclock.md)                   | Puntero al reloj de referencia del objeto.                     |
| [**m \_ tStart**](cbasemediafilter-m-tstart.md)                   | Tiempo de referencia que corresponde al tiempo de secuencia 0.            |
| [**CLSID de m \_**](cbasemediafilter-m-clsid.md)                     | Identificador de clase (CLSID) del objeto.                      |
| [**m \_ Plock**](cbasemediafilter-m-plock.md)                     | Puntero a una sección crítica.                               |
| Métodos públicos                                                   | Descripción                                                  |
| [**CBaseMediaFilter**](cbasemediafilter-cbasemediafilter.md)    | Método de constructor.                                          |
| [**~ CBaseMediaFilter**](cbasemediafilter--cbasemediafilter.md) | Método de destructor. Virtualiza.                                  |
| [**StreamTime**](cbasemediafilter-streamtime.md)                | Recupera la hora de la secuencia actual. Virtualiza.                  |
| [**IsActive**](cbasemediafilter-isactive.md)                    | Determina si el objeto está activo (en ejecución o en pausa). |
| Métodos IPersist                                                 | Descripción                                                  |
| [**GetClassID**](cbasemediafilter-getclassid.md)                | Recupera el identificador de clase.                              |
| Métodos IMediaFilter                                             | Descripción                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | Recupera el estado del objeto (en ejecución, detenido o en pausa).  |
| [**SetSyncSource**](cbasemediafilter-setsyncsource.md)          | Establece un reloj de referencia para el objeto.                       |
| [**GetSyncSource**](cbasemediafilter-getsyncsource.md)          | Recupera el reloj de referencia que usa el objeto.      |
| [**Stop**](cbasemediafilter-stop.md)                            | Detiene el objeto.                                            |
| [**Pausar**](cbasemediafilter-pause.md)                          | Pausa el objeto.                                           |
| [**Ejecutar**](cbasemediafilter-run.md)                              | Ejecuta el objeto.                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




