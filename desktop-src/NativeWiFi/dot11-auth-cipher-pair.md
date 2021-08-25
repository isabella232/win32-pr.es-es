---
description: Define un par de algoritmos de autenticación y cifrado 802.11 que se pueden habilitar al mismo tiempo en la estación 802.11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: DOT11_AUTH_CIPHER_PAIR estructura (Wlantypes.h)
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
ms.openlocfilehash: 84e4abde6192cf1be92b21df0c6a79125a198e0fde28e304cf583d76ea91689f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801485"
---
# <a name="dot11_auth_cipher_pair-structure"></a>Estructura DOT11 \_ AUTH \_ CIPHER \_ PAIR

La estructura **DOT11 \_ AUTH \_ CIPHER \_ PAIR** define un par de algoritmos de autenticación y cifrado 802.11 que se pueden habilitar al mismo tiempo en la estación 802.11.

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

Algoritmo de autenticación que usa un tipo enumerado [**DOT11 \_ AUTH \_ ALGORITHM.**](dot11-auth-algorithm.md)

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

Algoritmo de cifrado que usa un [**tipo enumerado \_ DOT11 CIPHER \_ ALGORITHM.**](dot11-cipher-algorithm.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La estructura DOT11 AUTH CIPHER PAIR define un algoritmo de autenticación y cifrado que se puede habilitar conjuntamente para las conexiones de red básicas del conjunto de servicios \_ \_ \_ (BSS).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                        |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wlantypes.h (incluya Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ALGORITMO DE \_ AUTENTICACIÓN DE DOT11 \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**ALGORITMO DE CIFRADO \_ DOT11 \_**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




