---
title: OP_JOINPROV2_PART
description: OP_JOINPROV2_PART definición de IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566909"
---
# <a name="op_joinprov2_part-structure"></a>OP_JOINPROV2_PART estructura

Contiene información adicional utilizada para configurar un cliente unido a un dominio.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a>Members

### <a name="dwflags"></a>dwFlags

Debe establecerse en cero o en uno de los valores siguientes:

|Value|Significado|
| --- | --- |
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|El sitio especificado en lpSiteName DEBE considerarse el sitio permanente para el cliente.|

### <a name="lpnetbiosname"></a>lpNetbiosName

Contiene el nombre Netbios de la cuenta de equipo en formato Unicode.

### <a name="lpsitename"></a>lpSiteName

Contiene el nombre del sitio Active Directory que debe usar el cliente.

### <a name="lpprimarydnsdomain"></a>lpPrimaryDNSDomain

Contiene el nombre de dominio DNS principal que debe usar el cliente.

### <a name="dwreserved"></a>dwReserved

Reservado para uso futuro y debe establecerse en 0.

### <a name="lpreserved"></a>lpReserved

Reservado para uso futuro y debe establecerse en NULL.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)
