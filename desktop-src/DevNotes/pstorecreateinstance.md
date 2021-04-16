---
description: Recupera un puntero de interfaz a un proveedor de almacenamiento.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Función PStoreCreateInstance (pstore. h)
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
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649889"
---
# <a name="pstorecreateinstance-function"></a>PStoreCreateInstance función)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Esta función puede modificarse o no estar disponible en versiones futuras de Windows. Use las funciones **CryptProtectData** y **CryptUnprotectData** en lugar de esta función.\]

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

*ppProvider* \[ enuncia\]
</dt> <dd>

Puntero al puntero de interfaz recuperado para el proveedor de almacenamiento. Cuando termine de usar la interfaz, disminuya su recuento de referencias mediante una llamada a su método [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Este parámetro no puede ser **null**.

</dd> <dt>

*pProviderID* \[ de\]
</dt> <dd>

Puntero al **GUID** que identifica el proveedor de almacenamiento. Si este parámetro es **null**, se usa el proveedor de almacenamiento base.

</dd> <dt>

*conservado* \[ de\]
</dt> <dd>

Sector debe ser **null**.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de **S \_ correcto** indica que la función se realizó correctamente.

## <a name="remarks"></a>Observaciones

Esta función no tiene biblioteca de importación asociada. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
