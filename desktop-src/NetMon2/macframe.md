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
ms.openlocfilehash: dcff7294d2800e797b43b3a05bd25c35418c6fb466c95130b97be73f25040d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364713"
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

Puntero de anillo de token a un marco.

</dd> <dt>

**Fddi**
</dt> <dd>

Puntero FDDI a un marco.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa con más frecuencia como superposición. Para que las propiedades del primer protocolo puedan ser accesibles, convierte el marco en el mismo tipo que el protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




