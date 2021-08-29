---
title: Función CleanupCredentialCache
description: Implementado por determinados proveedores de soporte técnico de seguridad (SSP) para vaciar la caché de credenciales de SSP.
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
ms.openlocfilehash: 62edb05f401c5ed69092c432f20a7ee96c98afd369e4a4cb0a1acde30e166013
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413025"
---
# <a name="cleanupcredentialcache-function"></a>Función CleanupCredentialCache

La **función CleanupCredentialCache** se implementa mediante determinados proveedores de soporte técnico de seguridad (SSP) para vaciar la caché de credenciales de SSP.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

**TRUE** si la función se realiza correctamente; de lo contrario, **FALSE**.

## <a name="remarks"></a>Comentarios

La **función CleanupCredentialCache** se implementa mediante los siguientes SSP:

-   MSNSSPC.dll
-   MSAPSSPC.dll

La implementación de **CleanupCredentialCache por** estos SSP siempre devuelve **TRUE**.

Antes de intentar obtener un identificador de módulo para exportar **CleanupCredentialCache,** la aplicación debe comprobar que el SSP que se ha cargado es uno de los SSP conocidos que implementan la **función CleanupCredentialCache.**

Para vaciar la caché de credenciales de SSP, la aplicación debe obtener un identificador de módulo para el SSP mediante una llamada a la [**función GetModuleHandle.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) Después de obtener el módulo, la aplicación debe exportar la función **CleanupCredentialCache** implementada por el SSP llamando a la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y pasando el módulo devuelto por **GetModuleHandle** y **CleanupCredentialCache** como parámetros de entrada.

Al igual que todos los demás aspectos de la API de WinINet, no se puede llamar a esta función de forma segura desde DllMain ni desde los constructores y destructores de objetos globales.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                                 |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt> </dl> |



 

