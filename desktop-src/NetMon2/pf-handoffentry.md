---
description: La \_ estructura PF HANDOFFENTRY define un protocolo que monitor de red agrega al conjunto de entrega de un analizador.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Estructura de PF_HANDOFFENTRY (Netmon. h)
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
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678132"
---
# <a name="pf_handoffentry-structure"></a>\_Estructura PF HANDOFFENTRY

La estructura **PF \_ HANDOFFENTRY** define un protocolo que monitor de red agrega al conjunto de entrega de un analizador.

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

Nombre del archivo INI asociado al Protocolo.

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

Valor asociado al Protocolo.

</dd> <dt>

**ValueFormatBase**
</dt> <dd>

Base numérica del valor del protocolo que se especifica en **dwHandOffValue**. La función **ValueFormatBase** debe establecerse en uno de los siguientes elementos:



| Value                                                                                                                                                                                                                        | Significado                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**BASE de formato de valor de entrega \_ \_ \_ \_ desconocida**</dt> </dl> | Base desconocida<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**formato de valor de entrega \_ \_ \_ \_ decimal base**</dt> </dl> | Base decimal<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**formato de valor de entrega \_ \_ \_ \_ hexadecimal base**</dt> </dl>             | Base hexadecimal<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se usa una matriz de las estructuras **PF \_ HANDOFFENTRY** en la estructura [PF \_ HANDOFFSET](pf-handoffset.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> </dl>

 

 




