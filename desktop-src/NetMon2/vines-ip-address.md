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
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245103"
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



## <a name="members"></a>Members

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



 

 




