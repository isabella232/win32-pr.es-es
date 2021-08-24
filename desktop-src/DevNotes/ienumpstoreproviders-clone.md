---
description: 'Método IEnumPStoreProviders::Clone: crea otro enumerador que contiene el mismo estado de enumeración que el actual.'
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: Método IEnumPStoreProviders::Clone (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a88a814d5052dea51bade8046392ecfe7530d43e368b10700c614d42baafe398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542185"
---
# <a name="ienumpstoreprovidersclone-method"></a>IEnumPStoreProviders::Clone (Método)

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Crea otro enumerador que contiene el mismo estado de enumeración que el actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mio* \[ out\]
</dt> <dd>

Puntero a un [**puntero IEnumPStoreProviders.**](ienumpstoreproviders.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
