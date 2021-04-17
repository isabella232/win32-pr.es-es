---
title: MPFASTPATH_DATA estructura (MpClient. h)
description: Notificación de actualización de FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPFASTPATH_DATA características de entorno heredado de Windows
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
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714564"
---
# <a name="mpfastpath_data-structure"></a>\_Estructura de datos MPFASTPATH

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

Tipo: **[ **\_ \_ tipo de firma de MP**](mp-signature-type.md)**

</dd> <dd>

Tipo de firma.

</dd> <dt>

**FastPathSignatureType**
</dt> <dd>

Tipo: **[ **MP \_ FASTPATH \_ Type**](mp-fastpath-type.md)**

</dd> <dd>

Tipo de firma FastPath.

</dd> <dt>

**FastPathSignatureVersion**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Versión de la firma FastPath (opcional).

</dd> <dt>

**CompilationTimestamp**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Marca de tiempo de compilación (UTC).

</dd> <dt>

**PersistenceType**
</dt> <dd>

Tipo: **[ **\_ tipo de \_ límite \_ de persistencia de MP**](mp-persistence-limit-type.md)**

</dd> <dd>

Tipo de persistencia (opcional).

</dd> <dt>

**PersistenceValue**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Valor de persistencia (opcional).

</dd> <dt>

**PersistencePath**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Ruta de acceso de persistencia (opcional).

</dd> <dt>

**Motivo**
</dt> <dd>

Tipo: **[ **\_ \_ motivo** de la eliminación del MP](mp-removal-reason.md)**

</dd> <dd>

Motivo de la eliminación de la firma.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo de FASTPATH de MP \_**](mp-fastpath-type.md)
</dt> <dt>

[**\_tipo de \_ límite de persistencia de MP \_**](mp-persistence-limit-type.md)
</dt> <dt>

[**\_tipo de firma MP \_**](mp-signature-type.md)
</dt> </dl>

 

 





