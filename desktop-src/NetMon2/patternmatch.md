---
description: La estructura PATTERNMATCH define los elementos de patrón que se usan para evaluar un marco.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Estructura PATTERNMATCH (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002236"
---
# <a name="patternmatch-structure"></a>Estructura PATTERNMATCH

La estructura **PATTERNMATCH** define los elementos de patrón que se usan para evaluar un marco.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas**
</dt> <dd>

Marcas de coincidencia de patrones:



| Value                                                                                                                                                                                                                                                                                           | Significado                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <dt>**Patrón \_ de Marcas de coincidencia \_ \_ no**</dt> <dt>0x00000001</dt> </dl>                                   | Cuando se establece, esta marca conserva los fotogramas que no tienen el patrón especificado en el lugar adecuado.<br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <dt>**Patrón \_ de Marcas de coincidencia \_ \_ Puerto \_ especificado**</dt> <dt>0x00000008</dt> </dl> | Busca un valor de número de puerto.<br/>                                                             |



 

</dd> <dt>

**OffsetBasis**
</dt> <dd>

Tipos de desplazamiento, que pueden ser uno de los siguientes:



| Value                                                                                                                                                                                                                                                       | Significado                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <dt>**DESPLAZAMIENTO \_ \_ en relación \_ con el \_ marco**</dt> </dl>                                         | Establece un desplazamiento, en bytes, con respecto al inicio del marco.<br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <dt>**DESPLAZAMIENTO \_ \_ en relación \_ con \_ el \_ Protocolo efectivo**</dt> </dl> | Establece un desplazamiento, en bytes, con respecto al inicio del Protocolo al que se hace referencia.<br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <dt>**DESPLAZAMIENTO \_ \_ de base con respecto \_ a \_ IPX**</dt> </dl>                                               | Establece un desplazamiento, en bytes, solo con respecto a IPX.<br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <dt>**\_base \_ de desplazamiento relativa \_ a \_ IP**</dt> </dl>                                                  | Establece un desplazamiento, en bytes, solo con respecto a IP.<br/>                              |



 

</dd> <dt>

**Puerto**
</dt> <dd>

Valor de puerto, si se especifica.

</dd> <dt>

**Offset**
</dt> <dd>

Desplazamiento, en bytes, con respecto al **OffsetBasis**.

</dd> <dt>

**Duración**
</dt> <dd>

Longitud del patrón coincidente.

</dd> <dt>

**PatternToMatch**
</dt> <dd>

Patrón que debe coincidir.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa para construir un filtro de captura. Para obtener más información sobre la implementación de esta estructura, vea [Capture filters](capture-filters.md).

Un filtro de captura puede contener hasta cuatro estructuras **PATTERNMATCH** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




