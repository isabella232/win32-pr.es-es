---
description: La estructura CONFIGUREDEXPERT asocia un experto con sus datos de configuración.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Estructura CONFIGUREDEXPERT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277025"
---
# <a name="configuredexpert-structure"></a>Estructura CONFIGUREDEXPERT

La estructura **CONFIGUREDEXPERT** asocia un experto con sus datos de configuración.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**hExpert**
</dt> <dd>

Identificador de un experto.

</dd> <dt>

**StartupFlags**
</dt> <dd>

Valores de marca de inicio del experto.

</dd> <dt>

**pConfig**
</dt> <dd>

Puntero a una estructura [**EXPERTCONFIG**](expertconfig.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




