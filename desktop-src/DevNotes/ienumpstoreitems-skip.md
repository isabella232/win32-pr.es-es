---
description: Omite el siguiente número especificado de elementos en la secuencia de enumeración especificada.
ms.assetid: 1459c18a-ccff-451f-8904-32858cc72b78
title: Método IEnumPStoreItems::Skip (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 8f40ac58b6801022d62d536e8f2ad5e2a27a6d5e71f05d5e0ced3656d5d3cf32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955974"
---
# <a name="ienumpstoreitemsskip-method"></a>IEnumPStoreItems::Skip (Método)

\[La Storage protegida (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Omite el siguiente número especificado de elementos en la secuencia de enumeración especificada.

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

Número de elementos de datos que se omitirán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> </dl>

 

 
