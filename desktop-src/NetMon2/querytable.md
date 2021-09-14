---
description: La estructura QUERYTABLE proporciona una lista de los equipos que actualmente usan Monitor de red para capturar datos de red.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Estructura QUERYTABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362126"
---
# <a name="querytable-structure"></a>QUERYTABLE (estructura)

La **estructura QUERYTABLE** proporciona una lista de los equipos que actualmente usan Monitor de red para capturar datos de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**nStationQueries**
</dt> <dd>

En la entrada, el número máximo de equipos que Monitor de red devolver.

En la salida, el número de estructuras [STATIONQUERY](stationquery.md) devueltas por Monitor de red. Cada **estructura STATIONQUERY** representa un equipo que captura datos actualmente.

</dd> <dt>

**StationQuery**
</dt> <dd>

En la entrada, una matriz de estructuras [STATIONQUERY vacías](stationquery.md) que contiene el número de elementos especificados en **nStationQueries**.

En la salida, una estructura [STATIONQUERY rellena](stationquery.md) para cada equipo que captura datos. nStationQueries devuelve el número de elementos **rellenos.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La aplicación que realiza la llamada debe asignar la memoria para esta estructura y la matriz [STATIONQUERY](stationquery.md) y liberarla después de que la información ya no sea necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[IESP::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC::QueryStations](irtc-querystations.md)
</dt> <dt>

[IStats::QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




