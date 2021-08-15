---
description: La estructura STATIONQUERY proporciona información sobre un equipo específico mediante Monitor de red.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Estructura STATIONQUERY (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a2e46f4c0d213091a3915b5310d7768a193d33e5ac3391fd3bc3c6781e32cb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363061"
---
# <a name="stationquery-structure"></a>STATIONQUERY (estructura)

La **estructura STATIONQUERY** proporciona información sobre un equipo específico mediante Monitor de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas**
</dt> <dd>

Marcas que identifican el estado actual de Monitor de red.



| Valor                                                                                                                                                                                                                | Significado                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <dt>**STATIONQUERY \_ FLAGS \_ LOADED**</dt> </dl>                   | El controlador se carga, pero el kernel no.<br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <dt>**MARCAS STATIONQUERY \_ EN \_ EJECUCIÓN**</dt> </dl>                | El controlador se carga pero no captura datos.<br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <dt>**CAPTURA DE \_ MARCAS STATIONQUERY \_**</dt> </dl>          | El controlador participa activamente en una captura.<br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <dt>**TRANSMISIÓN DE \_ MARCAS STATIONQUERY \_**</dt> </dl> | Este marcador está obsoleto.<br/>                       |



 

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Número de versión secundaria Monitor de red instalado en el equipo.

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Número de versión principal Monitor de red instalado en el equipo.

</dd> <dt>

**LicenseNumber**
</dt> <dd>

Número de licencia de software.

</dd> <dt>

**MachineName**
</dt> <dd>

Nombre del fabricante del equipo, si lo hubiera.

</dd> <dt>

**UserName**
</dt> <dd>

Nombre de usuario o identificador del sistema.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**AdapterAddress**
</dt> <dd>

Dirección NIC.

</dd> <dt>

**WMachineName**
</dt> <dd>

Nombre del equipo Unicode. Este miembro se aplica a Monitor de red 2.0 o posterior.

</dd> <dt>

**WUserName**
</dt> <dd>

Nombre de usuario Unicode. Este miembro se aplica a Monitor de red 2.0 o posterior.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La estructura [QUERYTABLE](querytable.md) usa una matriz de estas estructuras para proporcionar una lista de los equipos que actualmente usan Monitor de red para capturar datos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Querytable](querytable.md)
</dt> </dl>

 

 




