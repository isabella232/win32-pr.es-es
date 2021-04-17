---
title: MPEXPIRATION_DATA estructura (MpClient. h)
description: Notificación de estado de expiración del producto.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPEXPIRATION_DATA características de entorno heredado de Windows
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
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651386"
---
# <a name="mpexpiration_data-structure"></a>\_Estructura de datos MPEXPIRATION

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

Tipo: **el \_ \_ motivo de expiración del módulo de administración**

</dd> <dd>

Motivo de la expiración. Este es uno de los siguientes valores posibles:



| Value                                                                                                                                                                                                                                | Significado                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**Módulo de administración \_ EXPIRAdo \_ desconocido**</dt> <dt>0</dt> </dl> | Desconocido.<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**Módulo de administración \_ \_Evaluación expirada**</dt> <dt>1</dt> </dl>          | Evaluación.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**Módulo de administración \_ \_Wat expira**</dt> <dt>2</dt> </dl>             | Desconoce.<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

Tipo: **\_ \_ \_ Informe de estado de expiración de MP**

</dd> <dd>

Estado de expiración. Este es uno de los siguientes valores posibles:



| Value                                                                                                                                                                                                                                                                      | Significado                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**Módulo de administración \_ Informe de estado de EXPIRAción \_ \_ \_ desconocido**</dt> <dt>0</dt> </dl> | Estado desconocido.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**Módulo de administración \_ Informe de estado de EXPIRAción \_ \_ \_ válido**</dt> <dt>1</dt> </dl>       | Sin expiración.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**Módulo de administración \_ \_ \_ \_ Advertencia de informe de estado de expiración**</dt> <dt>2</dt> </dl> | Próximo expirado.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**Módulo de administración \_ El informe de estado de EXPIRAción \_ \_ \_ expiró**</dt> <dt>3</dt> </dl> | Expirado.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





