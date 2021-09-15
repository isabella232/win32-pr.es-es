---
title: ODJ_SID
description: ODJ_SID definición de IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566941"
---
# <a name="odj_sid-structure"></a>ODJ_SID estructura

Contiene un identificador de seguridad (SID).

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a>Members

### <a name="revision"></a>Revisión

Debe establecerse en la revisión de SID.

### <a name="subauthoritycount"></a>SubAuthorityCount

Debe establecerse en el número de elementos de SubAuthority.

### <a name="identifierauthority"></a>IdentifierAuthority

Debe establecerse en el identificador de entidad de SID.

### <a name="subauthority"></a>Subautoridad

Debe contener una matriz de subatenciones de SID.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**ODJ \_ SID \_ IDENTIFIER \_ AUTHORITY**](odj-sid_identifier_authority.md)
