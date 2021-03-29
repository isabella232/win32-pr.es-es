---
description: La \_ estructura de direcciones IPX proporciona una dirección en el nivel de protocolo IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Estructura de IPX_ADDRESS (Netmon. h)
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
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541182"
---
# <a name="ipx_address-structure"></a>\_Estructura de dirección IPX

La estructura de **\_ direcciones IPX** proporciona una dirección en el nivel de protocolo IPX.

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

Identificador de NIC de subred.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




