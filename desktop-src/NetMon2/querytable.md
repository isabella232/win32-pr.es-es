---
description: La estructura QUERYTABLE proporciona una lista de los equipos que usan actualmente Monitor de red para capturar datos de red.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Estructura QUERYTABLE (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677685"
---
# <a name="querytable-structure"></a>Estructura QUERYTABLE

La estructura **QUERYTABLE** proporciona una lista de los equipos que usan actualmente monitor de red para capturar datos de red.

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

En la entrada, el número máximo de equipos que desea que Monitor de red devuelvan.

En la salida, el número de estructuras [STATIONQUERY](stationquery.md) devueltas por monitor de red. Cada estructura **STATIONQUERY** representa un equipo que está capturando datos actualmente.

</dd> <dt>

**StationQuery**
</dt> <dd>

En la entrada, una matriz de estructuras [STATIONQUERY](stationquery.md) vacías que contiene el número de elementos especificados en **nStationQueries**.

En la salida, una estructura [STATIONQUERY](stationquery.md) rellena para cada equipo que está capturando datos. El número de elementos rellenados es devuelto por **nStationQueries**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La aplicación que realiza la llamada debe asignar la memoria para esta estructura y la matriz [STATIONQUERY](stationquery.md) , y se puede liberar después de que ya no se necesite la información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[IESP::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC::QueryStations](irtc-querystations.md)
</dt> <dt>

[IStas:: QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




