---
title: MPTHREAT_INFOEX_BEHAVIOR estructura (MpClient.h)
description: Contiene información específica de modificación del comportamiento.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR estructura heredada de Windows environment
- PMPTHREAT_INFOEX_BEHAVIOR puntero de estructura heredado Windows environment Features
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
ms.openlocfilehash: 8d0043b371cf4a77523a3b78bc31c5e56a480f134e87a0ed3853939460fc6a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883198"
---
# <a name="mpthreat_infoex_behavior-structure"></a>Estructura MPTHREAT \_ INFOEX \_ BEHAVIOR

Contiene información específica de modificación del comportamiento.

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

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Identificador de firma de modificación del comportamiento que el motor ha dado en el momento de la detección.

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

Versión de firma antispyware.

</dd> <dt>

**AVDeltaSignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versión de firma antivirus

</dd> <dt>

**HashType**
</dt> <dd>

Tipo: **[ **MP \_ HASH \_ TYPE**](mp-hash-type.md)**

</dd> <dd>

Tipo hash utilizado. Vea [**MP HASH TYPE (TIPO DE HASH DE \_ \_ MP).**](mp-hash-type.md)

</dd> <dt>

**FidelityValue**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor de fidelidad.

</dd> <dt>

**HashValue**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Hash del archivo.

</dd> <dt>

**TargetFileName**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Ruta de acceso y nombre del archivo de destino.

</dd> <dt>

**TargetFileHash**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Hash del archivo de destino.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TIPO \_ HASH DE \_ MP**](mp-hash-type.md)
</dt> </dl>

 

 





