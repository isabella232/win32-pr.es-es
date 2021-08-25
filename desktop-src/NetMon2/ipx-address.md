---
description: La estructura IPX \_ ADDRESS proporciona una dirección en el nivel de protocolo IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: IPX_ADDRESS estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0fc8298f2495029d63889fd5ebb24cdb284933897a9d9150b1dfcc2e14084f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743015"
---
# <a name="ipx_address-structure"></a>Estructura IPX \_ ADDRESS

La **estructura IPX \_ ADDRESS** proporciona una dirección en el nivel de protocolo IPX.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Subred**
</dt> <dd>

Identificador de subred de red.

</dd> <dt>

**Dirección**
</dt> <dd>

Identificador nic de subred.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




