---
description: Diseñado para establecer la información del parámetro especificado.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: Método IPStore::GetProvParam (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: de18c4452456ed98f7e5214a33445a0780189f7864d96cfb05e08123a3b42cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955914"
---
# <a name="ipstoregetprovparam-method"></a>Método IPStore::GetProvParam

\[La Storage protegida (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Este método no se implementa.\]

Diseñado para establecer la información del parámetro especificado. Sin embargo, tenga en cuenta que no se implementa y siempre producirá un error.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwParam* \[ En\]
</dt> <dd>

Reservado.

</dd> <dt>

*pwData* \[ out\]
</dt> <dd>

Reservado.

</dd> <dt>

*ppbData* \[ out\]
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

 

 
