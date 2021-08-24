---
description: Lee las reglas de acceso para un tipo determinado.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: Método IPStore::ReadAccessRuleSet (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d22f56c14df4d11a8979065ede81ab8418909033ffd816a233a18c51af7f66c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749755"
---
# <a name="ipstorereadaccessruleset-method"></a>Método IPStore::ReadAccessRuleSet

\[La Storage protegida (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Este método no se implementa.\]

Lee las reglas de acceso para un tipo determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
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

*ppRules* \[ En\]
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
