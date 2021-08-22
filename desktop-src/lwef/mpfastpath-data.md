---
title: MPFASTPATH_DATA estructura (MpClient.h)
description: Notificación de actualización de FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA estructura heredada de Windows environment
- PMPFASTPATH_DATA puntero de estructura heredado de Windows environment
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e138e9c45657cfc4ebeba1d1dbeed38070b6e07d09c512ec96835a04702d0c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556155"
---
# <a name="mpfastpath_data-structure"></a>Estructura DE DATOS \_ MPFASTPATH

Notificación de actualización de FastPath.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**SignatureType**
</dt> <dd>

Tipo: **[ **TIPO DE \_ FIRMA DE \_ MP**](mp-signature-type.md)**

</dd> <dd>

Tipo de firma.

</dd> <dt>

**FastPathSignatureType**
</dt> <dd>

Tipo: **[ **MP \_ FASTPATH \_ TYPE**](mp-fastpath-type.md)**

</dd> <dd>

Tipo de firma FastPath.

</dd> <dt>

**FastPathSignatureVersion**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Versión de firma de FastPath (opcional).

</dd> <dt>

**CompilationTimestamp**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Marca de tiempo de compilación (UTC).

</dd> <dt>

**PersistenceType**
</dt> <dd>

Tipo: **[ **TIPO DE \_ LÍMITE DE PERSISTENCIA \_ DE \_ MP**](mp-persistence-limit-type.md)**

</dd> <dd>

Tipo de persistencia (opcional).

</dd> <dt>

**PersistenceValue**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Valor de persistencia (opcional).

</dd> <dt>

**PersistencePath**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Ruta de acceso de persistencia (opcional).

</dd> <dt>

**Motivo**
</dt> <dd>

Tipo: **[ **MP \_ REMOVAL \_ REASON**](mp-removal-reason.md)**

</dd> <dd>

Motivo de la eliminación de la firma.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TIPO \_ DE MP FASTPATH \_**](mp-fastpath-type.md)
</dt> <dt>

[**TIPO DE \_ LÍMITE DE PERSISTENCIA DE \_ \_ MP**](mp-persistence-limit-type.md)
</dt> <dt>

[**TIPO \_ DE FIRMA DE \_ MP**](mp-signature-type.md)
</dt> </dl>

 

 





