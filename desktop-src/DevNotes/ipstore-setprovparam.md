---
description: Establece la información del parámetro especificado.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: Método IPStore::SetProvParam (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9ec106cd4558ddab7fd8bc430088f1bd7d721d7122f77166dfe0da7de35f1787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749725"
---
# <a name="ipstoresetprovparam-method"></a>Método IPStore::SetProvParam

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Establece la información del parámetro especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwParam* \[ En\]
</dt> <dd>

Contiene **PST PP FLUSH PW CACHE \_ \_ \_ \_ para** vaciar la caché de contraseñas de usuario.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

Longitud de la contraseña en el búfer.

</dd> <dt>

*pbData* 
</dt> <dd>

Puntero a un búfer que contiene la contraseña del usuario. Debe establecerse en **NULL.**

</dd> <dt>

*dwFlags* 
</dt> <dd>

Reservado: debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un **valor HRESULT.** Un valor de **PST \_ E OK \_ indica** que la función se ha realizado correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
