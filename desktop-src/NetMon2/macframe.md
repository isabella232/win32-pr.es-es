---
description: La estructura MACFRAME es una Unión de los protocolos iniciales más comunes.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: MACFRAME Union (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666544"
---
# <a name="macframe-union"></a>Unión MACFRAME

La estructura **MACFRAME** es una Unión de los protocolos iniciales más comunes.

## <a name="syntax"></a>Sintaxis


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a>Miembros

<dl> <dt>

**MacHeader**
</dt> <dd>

Puntero genérico a un marco.

</dd> <dt>

**Ethernet**
</dt> <dd>

Puntero Ethernet a un marco.

</dd> <dt>

**Tokenring**
</dt> <dd>

Puntero de token ring a un marco.

</dd> <dt>

**FDDI**
</dt> <dd>

Puntero FDDI a un marco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa con más frecuencia como una superposición. Para que se pueda tener acceso a las propiedades del primer Protocolo, convierta el marco en el mismo tipo que el protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




