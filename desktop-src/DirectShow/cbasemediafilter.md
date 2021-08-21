---
description: La clase CBaseMediaFilter implementa la interfaz IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: CBaseMediaFilter (clase, Amfilter.h)
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
ms.openlocfilehash: 16225ca289597bd8145e689912fd458a4f29d8aa4cc5ca68d6c3e0d0e3605ccc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586114"
---
# <a name="cbasemediafilter-class"></a>CBaseMediaFilter (clase)

![cbasemediafilter](images/filter05.png)

La `CBaseMediaFilter` clase implementa la interfaz [**IMediaFilter.**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) Use esta clase para distribuidores de complementos u otros objetos que necesiten admitir **IMediaFilter** sin admitir la [**interfaz IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) No use esta clase para los filtros. En su lugar, use [**la clase CBaseFilter**](cbasefilter.md) o una clase base derivada de **CBaseFilter.**



| Variables miembro protegidas                                       | Descripción                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**estado de m \_**](cbasemediafilter-m-state.md)                     | Estado actual del objeto.                                 |
| [**m \_ pClock**](cbasemediafilter-m-pclock.md)                   | Puntero al reloj de referencia del objeto.                     |
| [**m \_ tStart**](cbasemediafilter-m-tstart.md)                   | Hora de referencia que corresponde al tiempo de secuencia 0.            |
| [**m \_ clsid**](cbasemediafilter-m-clsid.md)                     | Identificador de clase (CLSID) del objeto .                      |
| [**m \_ pLock**](cbasemediafilter-m-plock.md)                     | Puntero a una sección crítica.                               |
| Métodos públicos                                                   | Descripción                                                  |
| [**CBaseMediaFilter**](cbasemediafilter-cbasemediafilter.md)    | Método constructor.                                          |
| [**~ CBaseMediaFilter**](cbasemediafilter--cbasemediafilter.md) | Método destructor. Virtual.                                  |
| [**StreamTime**](cbasemediafilter-streamtime.md)                | Recupera el tiempo de secuencia actual. Virtual.                  |
| [**IsActive**](cbasemediafilter-isactive.md)                    | Determina si el objeto está activo (en ejecución o en pausa). |
| Métodos IPersist                                                 | Descripción                                                  |
| [**GetClassID**](cbasemediafilter-getclassid.md)                | Recupera el identificador de clase.                              |
| Métodos IMediaFilter                                             | Descripción                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | Recupera el estado del objeto (en ejecución, detenido o en pausa).  |
| [**SetSyncSource**](cbasemediafilter-setsyncsource.md)          | Establece un reloj de referencia para el objeto .                       |
| [**GetSyncSource**](cbasemediafilter-getsyncsource.md)          | Recupera el reloj de referencia que usa el objeto .      |
| [**Stop**](cbasemediafilter-stop.md)                            | Detiene el objeto .                                            |
| [**Pausar**](cbasemediafilter-pause.md)                          | Pausa el objeto .                                           |
| [**Ejecutar**](cbasemediafilter-run.md)                              | Ejecuta el objeto .                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




