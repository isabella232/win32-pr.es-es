---
title: MPTHREAT_INFOEX_BEHAVIOR estructura (MpClient. h)
description: Contiene información específica de la modificación del comportamiento.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_INFOEX_BEHAVIOR características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803530"
---
# <a name="mpthreat_infoex_behavior-structure"></a>MPTHREAT \_ estructura de comportamiento de INFOEX \_

Contiene información específica de la modificación del comportamiento.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**SignatureID**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

IDENTIFICADOR de la firma de modificación del comportamiento proporcionado por el motor en el momento de la detección.

</dd> <dt>

**EngineVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versión del módulo del motor.

</dd> <dt>

**ASDeltaSignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versión de la firma de AntiSpyware.

</dd> <dt>

**AVDeltaSignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versión de firma de antivirus

</dd> <dt>

**HashType**
</dt> <dd>

Tipo: **[ **\_ \_ tipo hash de MP**](mp-hash-type.md)**

</dd> <dd>

Tipo hash usado. Vea [**\_ \_ tipo de hash de MP**](mp-hash-type.md).

</dd> <dt>

**FidelityValue**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor de fidelidad.

</dd> <dt>

**HashValue**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Hash del archivo.

</dd> <dt>

**TargetFileName**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

La ruta de acceso y el nombre del archivo de destino.

</dd> <dt>

**TargetFileHash**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

El hash del archivo de destino.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo hash de MP \_**](mp-hash-type.md)
</dt> </dl>

 

 





