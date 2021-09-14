---
description: La estructura PATTERNMATCH define los elementos de patrón utilizados para evaluar un marco.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Estructura PATTERNMATCH (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074101"
---
# <a name="patternmatch-structure"></a>PATTERNMATCH (estructura)

La **estructura PATTERNMATCH** define los elementos de patrón utilizados para evaluar un marco.

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



## <a name="members"></a>Members

<dl> <dt>

**Marcas**
</dt> <dd>

Marcas de coincidencia de patrones:



| Value                                                                                                                                                                                                                                                                                           | Significado                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <dt>**PATTERN \_ MARCAS \_ DE COINCIDENCIA NO \_ 0X00000001**</dt> <dt></dt> </dl>                                   | Cuando se establece, esta marca conserva los fotogramas que carecen del patrón especificado en el lugar adecuado.<br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <dt>**PATTERN \_ PUERTO \_ DE MARCAS DE COINCIDENCIA ESPECIFICADO \_ \_ 0X00000008**</dt> <dt></dt> </dl> | Busca un valor de número de puerto.<br/>                                                             |



 

</dd> <dt>

**OffsetBasis**
</dt> <dd>

Tipos de desplazamiento, que pueden ser uno de los siguientes:



| Value                                                                                                                                                                                                                                                       | Significado                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <dt>**BASE \_ DE DESPLAZAMIENTO RELATIVA AL \_ \_ \_ MARCO**</dt> </dl>                                         | Establece un desplazamiento, en bytes, relativo al inicio del marco.<br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <dt>**BASE \_ DE DESPLAZAMIENTO EN RELACIÓN CON EL PROTOCOLO \_ \_ \_ \_ EFECTIVO**</dt> </dl> | Establece un desplazamiento, en bytes, relativo al inicio del protocolo al que se hace referencia.<br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <dt>**BASE \_ DE DESPLAZAMIENTO RELATIVA A \_ \_ \_ IPX**</dt> </dl>                                               | Establece un desplazamiento, en bytes, solo relativo a IPX.<br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <dt>**BASE \_ DE DESPLAZAMIENTO RELATIVA A \_ \_ \_ IP**</dt> </dl>                                                  | Establece un desplazamiento, en bytes, solo relativo a IP.<br/>                              |



 

</dd> <dt>

**Puerto**
</dt> <dd>

Valor de puerto, si se especifica.

</dd> <dt>

**Offset**
</dt> <dd>

Desplazamiento, en bytes, relativo a **OffsetBasis.**

</dd> <dt>

**Duración**
</dt> <dd>

Longitud del patrón coincidente.

</dd> <dt>

**PatternToMatch**
</dt> <dd>

Patrón que se debe coincidir.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa para construir un filtro de captura. Para obtener más información sobre cómo implementar esta estructura, vea [Filtros de captura](capture-filters.md).

Un filtro de captura puede contener hasta cuatro **estructuras PATTERNMATCH.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




