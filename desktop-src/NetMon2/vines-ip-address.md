---
description: La estructura de \_ direcciones IP de Vines \_ es una dirección IP en una red de Vines.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Estructura de VINES_IP_ADDRESS (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360858"
---
# <a name="vines_ip_address-structure"></a>Estructura de \_ direcciones IP de Vines \_

La estructura de **\_ \_ direcciones IP de Vines** es una dirección IP en una red de Vines.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**NetId**
</dt> <dd>

El identificador de un equipo específico en una subred específica.

</dd> <dt>

**SubnetID**
</dt> <dd>

El identificador de una subred específica en toda la red.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




