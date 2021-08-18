---
description: Recupera un puntero de interfaz a un proveedor de almacenamiento.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Función PStoreCreateInstance (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: 2e32319e9585f5d1a80d0473c6ce27167f0ec181b81b974c526371b29c018b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955694"
---
# <a name="pstorecreateinstance-function"></a>Función PStoreCreateInstance

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Esta función puede modificarse o no estar disponible en versiones futuras de Windows. Use las **funciones CryptProtectData** y **CryptUnprotectData** en lugar de esta función.\]

Recupera un puntero de interfaz a un proveedor de almacenamiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppProvider* \[ out\]
</dt> <dd>

Puntero al puntero de interfaz recuperado para el proveedor de almacenamiento. Cuando termine de usar la interfaz , decrete su recuento de referencias mediante una llamada a su [**método IUnknown::Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Este parámetro no puede ser **NULL.**

</dd> <dt>

*pProviderID* \[ En\]
</dt> <dd>

Puntero al **GUID que** identifica el proveedor de almacenamiento. Si este parámetro es **NULL,** se usa el proveedor de almacenamiento base.

</dd> <dt>

*pReserved* \[ En\]
</dt> <dd>

Reservado; debe ser **NULL.**

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT.** Un valor de **S \_ OK indica** que la función se ha realizado correctamente.

## <a name="remarks"></a>Comentarios

Esta función no tiene ninguna biblioteca de importación asociada; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
