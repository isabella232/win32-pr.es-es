---
description: Restablece al principio de la secuencia de enumeración dada.
ms.assetid: add91f5d-3f84-4069-93c0-9380a3935b85
title: Método IEnumPStoreItems::Reset (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ee49de07e59ecd0a16efab1e3cae0d9e52ffe5805857838508ea1ec39e999b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404578"
---
# <a name="ienumpstoreitemsreset-method"></a>IEnumPStoreItems::Reset (Método)

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Restablece al principio de la secuencia de enumeración dada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> </dl>

 

 
