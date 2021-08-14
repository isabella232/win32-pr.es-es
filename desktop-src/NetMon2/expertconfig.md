---
description: La estructura EXPERTCONFIG contiene los datos de configuración del experto. El experto superpone el miembro RawConfigData con una estructura específica del experto.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Estructura EXPERTCONFIG (Netmon.h)
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
ms.openlocfilehash: 93b47054fd5b8103d5bbe0d762db87f285a5f01690d0b93f6da14d215e404a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366915"
---
# <a name="expertconfig-structure"></a>Estructura EXPERTCONFIG

La **estructura EXPERTCONFIG** contiene los datos de configuración del experto. El experto superpone el **miembro RawConfigData** con una estructura específica del experto.

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

Longitud total de la estructura, incluidos los cuatro bytes usados para el miembro. Monitor de red usa el valor cuando la estructura se guarda en una unidad de disco y se lee desde ella.

</dd> <dt>

**RawConfigData**
</dt> <dd>

Datos de configuración. El experto debe agregar los datos de configuración. Por ejemplo, suponga que tenía una estructura de datos similar a esta.

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

Tenga en **cuenta que RawConfigLength** garantiza que la superposición funciona correctamente. Al usar los datos, el código podría tener este aspecto:

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



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




