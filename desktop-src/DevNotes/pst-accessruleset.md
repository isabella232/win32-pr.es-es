---
description: Identifica el conjunto de reglas de acceso para los datos de almacenamiento protegidos.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: PST_ACCESSRULESET estructura (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 9695af01c6f0ffb33fe20a112659444011ad9c18812b8d2fd885641635c6b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666986"
---
# <a name="pst_accessruleset-structure"></a>Estructura \_ ACCESSRULESET de PST

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Identifica el conjunto de reglas de acceso para los datos de almacenamiento protegidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de esta estructura.

</dd> <dt>

**cRules**
</dt> <dd>

Número de reglas de la **matriz rgRules.**

</dd> <dt>

**rgRules**
</dt> <dd>

Puntero a una matriz de [**estructuras \_ ACCESSRULE de PST.**](pst-accessrule.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PST \_ ACCESSRULE**](pst-accessrule.md)
</dt> <dt>

[**CreateSubtype**](ipstore-createsubtype.md)
</dt> </dl>

 

 
