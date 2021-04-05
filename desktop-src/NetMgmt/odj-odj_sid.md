---
title: ODJ_SID
description: Definición de ODJ_SID IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104078559"
---
# <a name="odj_sid-structure"></a>Estructura de ODJ_SID

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

## <a name="members"></a>Miembros

### <a name="revision"></a>Revisión

Debe establecerse en la revisión del SID.

### <a name="subauthoritycount"></a>SubAuthorityCount

Debe establecerse en el número de elementos de la subautoridad.

### <a name="identifierauthority"></a>IdentifierAuthority

Debe establecerse en el identificador de la entidad de SID.

### <a name="subauthority"></a>Subautoridad

Debe contener una matriz de subentidades de SID.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**ODJ \_ \_ entidad de identificación \_ SID**](odj-sid_identifier_authority.md)
