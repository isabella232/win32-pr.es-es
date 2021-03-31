---
title: CleanupCredentialCache función)
description: Implementado por determinados proveedores de compatibilidad para seguridad (SSP) para vaciar la caché de credenciales de SSP.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Función CleanupCredentialCache WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149917"
---
# <a name="cleanupcredentialcache-function"></a>CleanupCredentialCache función)

Algunos proveedores de compatibilidad para seguridad (SSP) implementan la función **CleanupCredentialCache** para vaciar la caché de credenciales de SSP.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

**True** si la función se ejecuta correctamente; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

La función **CleanupCredentialCache** se implementa mediante el siguiente SSP:

-   MSNSSPC.dll
-   MSAPSSPC.dll

La implementación de **CleanupCredentialCache** por parte de estos SSP siempre devuelve **true**.

Antes de intentar obtener un identificador de módulo para exportar **CleanupCredentialCache**, la aplicación debe comprobar que el SSP que se ha cargado es uno de los SSP conocidos que implementan la función **CleanupCredentialCache** .

Para vaciar la memoria caché de credenciales de SSP, la aplicación debe obtener un identificador de módulo para el SSP mediante una llamada a la función [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) . Después de obtener el módulo, la aplicación debe exportar la función **CleanupCredentialCache** implementada por el SSP llamando a la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , pasando el módulo devuelto por **GetModuleHandle** y **CleanupCredentialCache** como parámetros de entrada.

Al igual que todos los demás aspectos de la API de WinINet, no se puede llamar a esta función de forma segura desde DllMain o los constructores y destructores de objetos globales.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                                 |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt> </dl> |



 

