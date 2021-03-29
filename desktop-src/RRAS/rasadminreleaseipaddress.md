---
title: Función de devolución de llamada RasAdminReleaseIpAddress
description: La función RasAdminReleaseIpAddress es una función definida por la aplicación que se exporta mediante un archivo DLL de administración de servidor RAS de terceros.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Función de devolución de llamada RasAdminReleaseIpAddress RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793510"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>Función de devolución de llamada RasAdminReleaseIpAddress

\[La función **RasAdminReleaseIpAddress** está disponible para su uso en Windows NT 4,0 y no está disponible en las versiones posteriores. En su lugar, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]

La función **RasAdminReleaseIpAddress** es una función definida por la aplicación que se exporta mediante un archivo dll de administración de servidor RAS de terceros. RAS llama a esta función para notificar a la DLL que el cliente remoto se desconectó y que se debe liberar la dirección IP.

## <a name="syntax"></a>Sintaxis


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszUserName* \[ de\]
</dt> <dd>

Especifica el puntero a una cadena Unicode terminada en null que especifica el nombre de un usuario remoto para el que se obtuvo previamente una dirección IP mediante la función [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) .

</dd> <dt>

*lpszPortName* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que especifica el nombre del puerto en el que está conectado el usuario especificado por *lpszUserName* .

</dd> <dt>

*pipAddress* \[ de\]
</dt> <dd>

Puntero a una variable **DirIP** que especifica la dirección IP devuelta para este usuario en una llamada anterior a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

El servidor RAS llama a la función **RasAdminReleaseIpAddress** solo si la aplicación devolvió **true** en el parámetro *bNotifyRelease* durante la llamada anterior a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) para el usuario especificado por el parámetro *lpszUserName* .

El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Para registrar el archivo DLL, establezca los siguientes valores bajo esta clave.



| Nombre del valor    | Datos del valor                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Una cadena **reg \_ SZ** que contiene el nombre descriptivo para mostrar del archivo dll. |
| *DLLPath*     | Una cadena **reg \_ SZ** que contiene la ruta de acceso completa del archivo dll.                  |



 

Por ejemplo, la entrada del registro para un archivo DLL de administración de RAS de una compañía ficticia denominada proelectrones, Inc. podría ser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **reg \_ SZ** : proelectrones ras admin dll *DLLPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll

El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de quitar o desinstalar. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del registro del archivo DLL.

 

 