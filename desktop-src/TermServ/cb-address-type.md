---
title: CB_ADDRESS_TYPE enumeración (Cbclient.h)
description: Especifica el tipo de dirección.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- CB_ADDRESS_TYPE enumeración Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecf17cea6ffc19743868b266236738839f9f917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249939"
---
# <a name="cb_address_type-enumeration"></a>Enumeración \_ CB ADDRESS \_ TYPE

Especifica el tipo de dirección.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB \_ ADDR \_ UNDEFINED**
</dt> <dd>

El tipo de dirección no está definido.

</dd> <dt>

<span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB \_ ADDR \_ IPv4**
</dt> <dd>

La dirección es una dirección IPv4.

</dd> <dt>

<span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB \_ ADDR \_ IPv6**
</dt> <dd>

La dirección es una dirección IPv6.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



 

 





