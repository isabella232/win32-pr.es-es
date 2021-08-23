---
description: La estructura \_ PF HANDOFFENTRY define un protocolo que Monitor de red al conjunto de entrega de un analizador.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: PF_HANDOFFENTRY estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: faf98490424754d6ae2223ca063e0e3a4eec69c113b1a220e9657b7db5edbb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778675"
---
# <a name="pf_handoffentry-structure"></a>Estructura \_ PF HANDOFFENTRY

La **estructura \_ PF HANDOFFENTRY** define un protocolo que Monitor de red al conjunto de entrega de un analizador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**szIniFile**
</dt> <dd>

Nombre del archivo INI asociado al protocolo.

</dd> <dt>

**szIniSection**
</dt> <dd>

Etiqueta de sección dentro del archivo INI.

</dd> <dt>

**szProtocol**
</dt> <dd>

Nombre del protocolo.

</dd> <dt>

**dwHandOffValue**
</dt> <dd>

Valor asociado al protocolo.

</dd> <dt>

**ValueFormatBase**
</dt> <dd>

Base numérica del valor de protocolo especificado en **dwHandOffValue.** La **función ValueFormatBase** debe establecerse en una de las siguientes opciones:



| Valor                                                                                                                                                                                                                        | Significado                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**BASE DESCONOCIDA DEL \_ FORMATO DE VALOR DE \_ \_ ENTREGA \_**</dt> </dl> | Base desconocida<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**HANDOFF \_ VALUE \_ FORMAT \_ BASE \_ DECIMAL**</dt> </dl> | Base decimal<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**HANDOFF \_ VALUE \_ FORMAT \_ BASE \_ HEX**</dt> </dl>             | Base hexadecimal<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

En la estructura [PF \_ HANDOFFSET](pf-handoffset.md) se usa una matriz de las estructuras **\_ PF HANDOFFENTRY.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> </dl>

 

 




