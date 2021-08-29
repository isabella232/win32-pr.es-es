---
description: Contiene un número de puerto utilizado para los protocolos IP o IPX.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: GENERIC_PORT union (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 353faa17a505742f9e5b31feeb1c0108add7895f8039f12905c399d515bb2bb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910875"
---
# <a name="generic_port-union"></a>Unión \_ DE PUERTO GENÉRICO

La **estructura \_ GENERIC PORT** contiene un número de puerto que se usa para los protocolos IP o IPX.

## <a name="syntax"></a>Sintaxis


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**IPPort**
</dt> <dd>

Número de puerto IP rellenado.

</dd> <dt>

**ByteSwappedIPXPort**
</dt> <dd>

Número de puerto IPX rellenado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




