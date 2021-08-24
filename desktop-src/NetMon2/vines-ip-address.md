---
description: La estructura DE \_ DIRECCIONES IP \_ de SARS es una dirección IP en una red de Dpis.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: VINES_IP_ADDRESS estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 23a590679fd2b4a147a8bc0f92a4d4c7b4afb8c746526de9fba7cfc388e4e1c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742205"
---
# <a name="vines_ip_address-structure"></a>ESTRUCTURA DE \_ DIRECCIONES IP \_ DE ASÍNS

La **estructura DE DIRECCIONES IP \_ \_ de SARS** es una dirección IP en una red de Dpis.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**NetID**
</dt> <dd>

Identificador de una máquina específica en una subred específica.

</dd> <dt>

**SubnetID**
</dt> <dd>

Identificador de una subred específica en toda la red.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




