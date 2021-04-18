---
description: Lee las reglas de acceso para un tipo determinado.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'IPStore:: ReadAccessRuleSet (método) (pstore. h)'
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
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649962"
---
# <a name="ipstorereadaccessruleset-method"></a>IPStore:: ReadAccessRuleSet (método)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

*Clave* \[ de de\]
</dt> <dd>

Reservado.

</dd> <dt>

*pType* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*pSubtype* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*Pinfo* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*ppRules* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre se producirá un error en las llamadas a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
