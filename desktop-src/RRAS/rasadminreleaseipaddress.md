---
title: Función de devolución de llamada RasAdminReleaseIpAddress
description: La función RasAdminReleaseIpAddress es una función definida por la aplicación que exporta un archivo DLL de administración de servidores RAS de terceros.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- RasAdminReleaseIpAddress función de devolución de llamada RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 102c9af7a8e38ccbbb4a7e67b2734588857ddca93da862be211fd1223133f80d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788867"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>Función de devolución de llamada RasAdminReleaseIpAddress

\[La **función RasAdminReleaseIpAddress** está disponible para su uso en Windows NT 4.0 y no está disponible en versiones posteriores. En su lugar, [**use MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]

La **función RasAdminReleaseIpAddress** es una función definida por la aplicación que exporta un archivo DLL de administración de servidores RAS de terceros. RAS llama a esta función para notificar al archivo DLL que el cliente remoto se ha desconectado y que se debe liberar la dirección IP.

## <a name="syntax"></a>Sintaxis


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszUserName* \[ En\]
</dt> <dd>

Especifica el puntero a una cadena Unicode terminada en NULL que especifica el nombre de un usuario remoto para el que se obtuvo previamente una dirección IP mediante la función [**RasAdminGetIpAddressForUser.**](rasadmingetipaddressforuser.md)

</dd> <dt>

*lpszPortName* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que especifica el nombre del puerto en el que está conectado el usuario especificado por *lpszUserName.*

</dd> <dt>

*pipAddress* \[ En\]
</dt> <dd>

Puntero a una variable **IPADDR** que especifica la dirección IP devuelta para este usuario en una llamada anterior a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No hay ninguna información de error extendida para esta función; no llame a [**GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentarios

El servidor RAS llama a la función **RasAdminReleaseIpAddress** solo si la aplicación devolvió **TRUE** en el *parámetro bNotifyRelease* durante la llamada anterior a [**RasAdminGetIpAddressForUser para**](rasadmingetipaddressforuser.md) el usuario especificado por el *parámetro lpszUserName.*

El programa de instalación de un archivo DLL de administración ras de terceros debe registrar el archivo DLL con RAS proporcionando información con la siguiente clave en el Registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Para registrar el archivo DLL, establezca los siguientes valores en esta clave.



| Nombre del valor    | Datos del valor                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Cadena **REG \_ SZ** que contiene el nombre para mostrar descriptivo del archivo DLL. |
| *DLLPath*     | Cadena **REG \_ SZ** que contiene la ruta de acceso completa del archivo DLL.                  |



 

Por ejemplo, la entrada del Registro para un archivo DLL de administración de RAS de una compañía ficticia denominada ProElectrón, Inc. podría ser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **REG \_ SZ** : Dll dll de administrador de RAS de ProElectrón *DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll

El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de eliminación o desinstalación. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del Registro del archivo DLL.

 

 