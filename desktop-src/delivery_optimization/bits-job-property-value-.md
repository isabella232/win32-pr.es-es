---
title: BITS_JOB_PROPERTY_VALUE estructura (Deliveryoptimization.h)
description: La BITS_JOB_PROPERTY_VALUE de datos proporciona el valor de propiedad del trabajo do en función del valor de la enumeración BITS_JOB_PROPERTY_ID datos.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- BITS_JOB_PROPERTY_VALUE estructura
- BITS_JOB_PROPERTY_VALUE estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567161"
---
# <a name="bits_job_property_value-structure"></a>BITS_JOB_PROPERTY_VALUE estructura

La **BITS_JOB_PROPERTY_VALUE** de datos proporciona el valor de propiedad del trabajo do en función del valor de la [**enumeración BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) datos.

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



## <a name="members"></a>Members

<dl> <dt>

**Dword**
</dt> <dd>

Este valor se devuelve cuando se usa el identificador de propiedad de enumeración BITS_JOB_PROPERTY_ID_COST_FLAGS **y** se aplica como directiva [de transferencia](https://www.bing.com/search?q=transfer+policy) en el trabajo do.

</dd> <dt>

**Clsid**
</dt> <dd>

Este valor se devuelve cuando se  usa el identificador de propiedad de enumeración BITS_JOB_PROPERTY_NOTIFICATION_CLSID y representa el CLSID del objeto de devolución de llamada que se va a registrar con el trabajo do.

</dd> <dt>

**Habilitar**
</dt> <dd>

No compatible.

</dd> <dt>

**Uint64**
</dt> <dd>

No compatible.

</dd> <dt>

**Target**
</dt> <dd>

No compatible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





