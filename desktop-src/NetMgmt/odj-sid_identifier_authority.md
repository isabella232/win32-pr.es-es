---
title: SID_IDENTIFIER_AUTHORITY
description: SID_IDENTIFIER_AUTHORITY definición de IDL
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566885"
---
# <a name="sid_identifier_authority-structure"></a>SID_IDENTIFIER_AUTHORITY estructura

Contiene una entidad de identificador de SID.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a>Members

### <a name="value"></a>Value

Debe establecerse en los seis bytes de la entidad de identificador de SID.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)