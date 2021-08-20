---
description: La enumeración EXPERTSTATUSENUMERATION contiene valores de estado. Lo usa el miembro Status de la estructura EXPERTSTATUS y el parámetro Status de ExpertIndicateStatus.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Enumeración EXPERTSTATUSENUMERATION (Netmon.h)
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
ms.openlocfilehash: ee0729deab566717457f03af27a7e31de8cdf8f1b78f9a5f97b3c3ff406641fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795798"
---
# <a name="expertstatusenumeration-enumeration"></a>ENUMERACIÓN EXPERTSTATUSENUMERATION

La **enumeración EXPERTSTATUSENUMERATION** contiene valores de estado. Lo usa el miembro **Status de** la [estructura EXPERTSTATUS](expertstatus.md) y el *parámetro Status* [de ExpertIndicateStatus](expertindicatestatus.md).

## <a name="syntax"></a>Syntax


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

<span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ INACTIVE**
</dt> <dd>

El experto nunca empezó.

</dd> <dt>

<span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**INICIO \_ DE EXPERTSTATUS**
</dt> <dd>

El experto se está iniciando.

</dd> <dt>

<span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EJECUCIÓN \_ DE EXPERTSTATUS**
</dt> <dd>

El experto se ejecuta con normalidad.

</dd> <dt>

<span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**PROBLEMA \_ DE EXPERTSTATUS**
</dt> <dd>

Un problema especificado en *SubStatus detuvo* al experto.

</dd> <dt>

<span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ ABORTED**
</dt> <dd>

Monitor de red detuvo al experto.

</dd> <dt>

<span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ DONE**
</dt> <dd>

El experto finalizó correctamente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




