---
description: Escribe las reglas de acceso para el tipo especificado.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: Método IPStore::WriteAccessRuleset (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a21fac6df5ab4d87e55d71e45f5698251ca4f82b6c93de1072c2ae5bcd7236aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955904"
---
# <a name="ipstorewriteaccessruleset-method"></a>Método IPStore::WriteAccessRuleset

\[El Storage protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Este método no se implementa.\]

Escribe las reglas de acceso para el tipo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Reservado.

</dd> <dt>

*pType* \[ En\]
</dt> <dd>

Reservado.

</dd> <dt>

*pSubtype* \[ En\]
</dt> <dd>

Reservado.

</dd> <dt>

*pInfo* \[ En\]
</dt> <dd>

Reservado.

</dd> <dt>

*pRules* \[ En\]
</dt> <dd>

Reservado.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Las llamadas a este método siempre producirán un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
