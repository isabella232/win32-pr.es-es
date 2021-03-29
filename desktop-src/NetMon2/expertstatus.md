---
description: Indica el estado actual de un experto en ejecución.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Estructura EXPERTSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540235"
---
# <a name="expertstatus-structure"></a>Estructura EXPERTSTATUS

La estructura **EXPERTSTATUS** indica el estado actual de un experto en ejecución.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Estado**
</dt> <dd>

Valor de estado de experto actual definido por la enumeración [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) .

</dd> <dt>

**Subestado**
</dt> <dd>

Valor de subestado.

</dd> <dt>

**PercentDone**
</dt> <dd>

Porcentaje de finalización del análisis experto de datos de red.

</dd> <dt>

**Frame**
</dt> <dd>

Número de marco.

</dd> <dt>

**Szstatustext del**
</dt> <dd>

Texto que describe el estado del experto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




