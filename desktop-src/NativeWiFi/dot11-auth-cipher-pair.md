---
description: Define un par de algoritmos de cifrado y autenticación 802,11 que se pueden habilitar al mismo tiempo en la estación 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: DOT11_AUTH_CIPHER_PAIR estructura (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687763"
---
# <a name="dot11_auth_cipher_pair-structure"></a>\_Estructura del \_ par de cifrado de autenticación de DOT11 \_

La estructura de **\_ \_ \_ pares de cifrado de autenticación de DOT11** define un par de algoritmos de autenticación y cifrado 802,11 que se pueden habilitar al mismo tiempo en la estación 802,11.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**AuthAlgoId**
</dt> <dd>

Un algoritmo de autenticación que usa un tipo enumerado de [**\_ \_ algoritmo**](dot11-auth-algorithm.md) de autenticación de DOT11.

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

Algoritmo de cifrado que usa un tipo enumerado de [**\_ \_ algoritmo de cifrado de DOT11**](dot11-cipher-algorithm.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de pares de cifrado de autenticación de DOT11 \_ \_ \_ define un algoritmo de autenticación y cifrado que se puede habilitar conjuntamente para las conexiones de red de Basic Service Set (BSS).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                        |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wlantypes. h (incluye Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Algoritmo de autenticación de DOT11 \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**\_Algoritmo de cifrado de DOT11 \_**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




