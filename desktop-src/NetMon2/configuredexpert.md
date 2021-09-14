---
description: La estructura CONFIGUREDECIAL asocia un experto a sus datos de configuración.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Estructura CONFIGUREDEXPERT (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253857"
---
# <a name="configuredexpert-structure"></a>ESTRUCTURA CONFIGUREDEXPERT

La **estructura CONFIGUREDECIAL** asocia un experto a sus datos de configuración.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a>Members

<dl> <dt>

**hExpert**
</dt> <dd>

Controlar a un experto.

</dd> <dt>

**StartupFlags**
</dt> <dd>

Valores de marca de inicio del experto.

</dd> <dt>

**pConfig**
</dt> <dd>

Puntero a una [**estructura EXPERTCONFIG.**](expertconfig.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




