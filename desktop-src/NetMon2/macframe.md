---
description: La estructura MACFRAME es una unión de los protocolos iniciales más comunes.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: Unión MACFRAME (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245361"
---
# <a name="macframe-union"></a>Unión de MACFRAME

La **estructura MACFRAME** es una unión de los protocolos iniciales más comunes.

## <a name="syntax"></a>Sintaxis


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a>Members

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

Puntero de anillo de token a un marco.

</dd> <dt>

**Fddi**
</dt> <dd>

Puntero FDDI a un marco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa con más frecuencia como superposición. Para que las propiedades del primer protocolo se puedan acceder, convierte el marco en el mismo tipo que el protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




