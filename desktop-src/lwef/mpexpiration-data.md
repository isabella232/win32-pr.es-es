---
title: MPEXPIRATION_DATA estructura (MpClient.h)
description: Notificación de estado de expiración del producto.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA estructura heredada de Windows environment
- PMPEXPIRATION_DATA puntero de estructura heredado Windows environment features
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f270b7d433e6de7cd1eb3e7a3cfc88c9cb85c6087c20371ac804ec61d949d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976035"
---
# <a name="mpexpiration_data-structure"></a>Estructura DE DATOS \_ MPEXPIRATION

Notificación de estado de expiración del producto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Motivo**
</dt> <dd>

Tipo: **MP \_ EXPIRE \_ REASON**

</dd> <dd>

Motivo de expiración. Este es uno de los siguientes valores posibles:



| Value                                                                                                                                                                                                                                | Significado                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**MP \_ EXPIRADO \_ DESCONOCIDO**</dt> <dt>0</dt> </dl> | Desconocido.<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**MP \_ EVAL \_ EXPIRADA**</dt> <dt>1</dt> </dl>          | Evaluación.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**MP \_ EXPIR \_ EXPIR IN 2**</dt> <dt></dt> </dl>             | Wat.<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

Tipo: **MP EXPIRE STATE \_ \_ \_ REPORT**

</dd> <dd>

Estado de expiración. Este es uno de los siguientes valores posibles:



| Value                                                                                                                                                                                                                                                                      | Significado                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**MP \_ INFORME \_ DE ESTADO DE \_ \_ EXPIRACIÓN DESCONOCIDO**</dt> <dt>0</dt> </dl> | Estado desconocido.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**MP \_ INFORME \_ DE ESTADO DE \_ \_ EXPIRACIÓN VÁLIDO**</dt> <dt>1</dt> </dl>       | Sin expiración.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**MP \_ ADVERTENCIA \_ DE INFORME DE ESTADO DE \_ \_ EXPIRACIÓN**</dt> <dt>2</dt> </dl> | Casi ha expirado.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**MP \_ INFORME \_ DE ESTADO DE \_ \_ EXPIRACIÓN EXPIRADO**</dt> <dt>3</dt> </dl> | caducado.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





