---
description: Obtiene un objeto de enumerador que se puede utilizar a su vez para enumerar los proveedores de almacenamiento protegidos que están instalados actualmente en el sistema.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Función PStoreEnumProviders (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650000"
---
# <a name="pstoreenumproviders-function"></a>PStoreEnumProviders función)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Obtiene un objeto de enumerador que se puede utilizar a su vez para enumerar los proveedores de almacenamiento protegidos que están instalados actualmente en el sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*ppenum* 
</dt> <dd>

Un puntero a un puntero a una interfaz [**IEnumPStoreProviders**](ienumpstoreproviders.md) que se puede usar para enumerar los proveedores instalados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve un **valor HRESULT**.

## <a name="remarks"></a>Observaciones

El componente de almacenamiento protegido tiene una arquitectura basada en proveedor. Las aplicaciones que hacen uso de almacenamiento protegido pueden especificar los proveedores instalados que se van a usar al almacenar y recuperar sus datos.

La función **PStoreEnumProviders** se usa para enumerar los proveedores de almacenamiento protegido instalados. Cada proveedor se identifica mediante un identificador único global (GUID).

Hasta este momento, solo se ha escrito un proveedor de almacenamiento protegido. Dado que el servicio de almacenamiento protegido está en desuso actualmente, es muy poco probable que se produzcan todos los proveedores adicionales. Como resultado, esta función no se debe usar para ningún propósito.

Esta función no tiene biblioteca de importación asociada. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
