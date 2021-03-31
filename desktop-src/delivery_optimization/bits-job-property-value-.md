---
title: BITS_JOB_PROPERTY_VALUE estructura (Deliveryoptimization. h)
description: La Unión BITS_JOB_PROPERTY_VALUE proporciona el valor de propiedad del trabajo DO basándose en el valor de la enumeración BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Estructura de BITS_JOB_PROPERTY_VALUE
- Estructura de BITS_JOB_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150280"
---
# <a name="bits_job_property_value-structure"></a>Estructura de BITS_JOB_PROPERTY_VALUE

La Unión **BITS_JOB_PROPERTY_VALUE** proporciona el valor de propiedad del trabajo do basándose en el valor de la enumeración [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**DWORD**
</dt> <dd>

Este valor se devuelve al utilizar el identificador de la propiedad de enumeración **BITS_JOB_PROPERTY_ID_COST_FLAGS** y se aplica como la [Directiva de transferencia](https://www.bing.com/search?q=transfer+policy) en el trabajo do.

</dd> <dt>

**ClsID**
</dt> <dd>

Este valor se devuelve cuando se usa el identificador de la propiedad de enumeración **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** y representa el CLSID del objeto de devolución de llamada que se va a registrar con el trabajo.

</dd> <dt>

**Habilitar**
</dt> <dd>

No se admite.

</dd> <dt>

**Uint64**
</dt> <dd>

No se admite.

</dd> <dt>

**Target**
</dt> <dd>

No se admite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





