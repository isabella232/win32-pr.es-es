---
description: La estructura EXPERTCONFIG contiene los datos de configuración del experto. El experto superpone el miembro RawConfigData con una estructura específica del experto.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Estructura EXPERTCONFIG (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666301"
---
# <a name="expertconfig-structure"></a>Estructura EXPERTCONFIG

La estructura **EXPERTCONFIG** contiene los datos de configuración del experto. El experto superpone el miembro **RawConfigData** con una estructura específica del experto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a>Miembros

<dl> <dt>

**RawConfigLength**
</dt> <dd>

Longitud total de la estructura, incluidos los cuatro bytes usados para el miembro. Monitor de red usa el valor cuando la estructura se guarda en una unidad de disco y se lee de ella.

</dd> <dt>

**RawConfigData**
</dt> <dd>

Datos de configuración. El experto debe agregar los datos de configuración. Por ejemplo, supongamos que tiene una estructura de datos que tenía el aspecto siguiente.

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

Tenga en cuenta que **RawConfigLength** garantiza que la superposición funciona correctamente. Al usar los datos, el código podría tener el aspecto siguiente:

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




