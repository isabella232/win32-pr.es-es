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
ms.openlocfilehash: 9b8f291f055bfba159309b6c75a54d95514ed9c7614eb0456a4870e657f04209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555375"
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



## <a name="members"></a>Miembros

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

## <a name="remarks"></a>Comentarios

La aplicación que realiza la llamada debe asignar la memoria para esta estructura y la matriz [STATIONQUERY](stationquery.md) y liberarla después de que la información ya no sea necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

 




