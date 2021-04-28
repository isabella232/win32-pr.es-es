---
description: 'Método IEnumPStoreProviders::Skip: omite el siguiente número especificado de elementos en la secuencia de enumeración.'
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: Método IEnumPStoreProviders::Skip (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2f74c44de172d9235d9768b8f484405b5e8fb7fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096753"
---
# <a name="ienumpstoreprovidersskip-method"></a>IEnumPStoreProviders::Skip (Método)

\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Omite el siguiente número especificado de elementos en la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Número de tipos de proveedor que se omitirán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
