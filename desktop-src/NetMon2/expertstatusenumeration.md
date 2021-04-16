---
description: La enumeración EXPERTSTATUSENUMERATION contiene valores de estado. Lo usa el miembro status de la estructura EXPERTSTATUS y el parámetro status en ExpertIndicateStatus.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Enumeración EXPERTSTATUSENUMERATION (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666294"
---
# <a name="expertstatusenumeration-enumeration"></a>Enumeración EXPERTSTATUSENUMERATION

La enumeración **EXPERTSTATUSENUMERATION** contiene valores de estado. Lo usa el miembro **status** de la estructura [EXPERTSTATUS](expertstatus.md) y el parámetro *status* en [ExpertIndicateStatus](expertindicatestatus.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ INactivo**
</dt> <dd>

El experto nunca comenzó.

</dd> <dt>

<span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**Inicio de EXPERTSTATUS \_**
</dt> <dd>

Se está iniciando el experto.

</dd> <dt>

<span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS en \_ ejecución**
</dt> <dd>

El experto se ejecuta con normalidad.

</dd> <dt>

<span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**problema de EXPERTSTATUS \_**
</dt> <dd>

Un problema especificado en el *subestado* detuvo el experto.

</dd> <dt>

<span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ anulado**
</dt> <dd>

Monitor de red detuvo el experto.

</dd> <dt>

<span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ completado**
</dt> <dd>

El experto ha finalizado correctamente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




