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
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071617"
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



## <a name="members"></a>Members

<dl> <dt>

**AuthAlgoId**
</dt> <dd>

Algoritmo de autenticación que usa un tipo enumerado [**DOT11 \_ AUTH \_ ALGORITHM.**](dot11-auth-algorithm.md)

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

Algoritmo de cifrado que usa un [**tipo enumerado \_ DOT11 CIPHER \_ ALGORITHM.**](dot11-cipher-algorithm.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura DOT11 AUTH CIPHER PAIR define un algoritmo de autenticación y cifrado que se puede habilitar conjuntamente para las conexiones de red del conjunto de servicios básicos \_ \_ \_ (BSS).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                        |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wlantypes.h (incluye Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ALGORITMO DE \_ AUTENTICACIÓN DE DOT11 \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**ALGORITMO DE CIFRADO DOT11 \_ \_**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




