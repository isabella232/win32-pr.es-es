---
description: Proporciona una línea en el panel superior de la Visor de eventos que actúa como contenedor para todos los datos posibles insertados en una columna.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Estructura NMCOLUMNVARIANT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669833"
---
# <a name="nmcolumnvariant-structure"></a>Estructura NMCOLUMNVARIANT

La estructura **NMCOLUMNVARIANT** proporciona una línea en el panel superior de la visor de eventos que actúa como contenedor para todos los datos posibles insertados en una columna.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Un valor del tipo de enumeración [**NMCOLUMNTYPE**](nmcolumntype.md) .

</dd> <dt>

**Valor**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

valor entero de 8 bits sin signo.

</dd> <dt>

**Sint8Val**
</dt> <dd>

valor entero de 8 bits con signo.

</dd> <dt>

**Uint16Val**
</dt> <dd>

valor entero sin signo de 16 bits.

</dd> <dt>

**Sint16Val**
</dt> <dd>

valor entero de 16 bits con signo.

</dd> <dt>

**Uint32Val**
</dt> <dd>

valor entero de 32 bits sin signo.

</dd> <dt>

**Sint32Val**
</dt> <dd>

valor entero de 32 bits con signo.

</dd> <dt>

**Float64Val**
</dt> <dd>

valor Float de 64 bits.

</dd> <dt>

**FrameVal**
</dt> <dd>

Número de marco.

</dd> <dt>

**YesNoVal**
</dt> <dd>

Muestra sí o no.

</dd> <dt>

**OnOffVal**
</dt> <dd>

Muestra activado o desactivado.

</dd> <dt>

**TrueFalseVal**
</dt> <dd>

Muestra true o false.

</dd> <dt>

**MACAddrVal**
</dt> <dd>

Dirección MAC.

</dd> <dt>

**IPXAddrVal**
</dt> <dd>

Dirección IPX.

</dd> <dt>

**IPAddrVal**
</dt> <dd>

Dirección IP.

</dd> <dt>

**VarTimeVal**
</dt> <dd>

Hora de la variante. Use **VariantTimetoSystemTime** para convertir a la hora del sistema.

</dd> <dt>

**pStringVal**
</dt> <dd>

Puntero a una cadena.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NMCOLUMNTYPE**](nmcolumntype.md)
</dt> </dl>

 

 




