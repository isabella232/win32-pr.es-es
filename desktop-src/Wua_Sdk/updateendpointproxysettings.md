---
description: La estructura UpdateEndpointProxySettings define la configuración de proxy utilizada al solicitar un token.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Estructura UpdateEndpointProxySettings (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082171"
---
# <a name="updateendpointproxysettings-structure"></a>Estructura UpdateEndpointProxySettings

La estructura **UpdateEndpointProxySettings** define la configuración de proxy utilizada al solicitar un token.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a>Miembros

<dl> <dt>

**szProxyAddr**
</dt> <dd>

Nombre DNS o dirección IP del servidor proxy que se va a usar (por ejemplo, "proxy.somecorp.com" o "192.168.0.4") o una cadena vacía si no se debe utilizar ningún proxy.

</dd> <dt>

**szBypassList**
</dt> <dd>

Una lista de direcciones de host que deben omitir el servidor proxy o una cadena vacía si todas las direcciones de host deben usar el servidor proxy

WUA no utiliza estos datos si **szProxyAddr** está vacío.

</dd> <dt>

**szUserName**
</dt> <dd>

El nombre de usuario que se usa para autenticarse con el servidor proxy, o la cadena vacía si no se necesita autenticación.

WUA no utiliza estos datos si **szProxyAddr** está vacío.

</dd> <dt>

**szPassword**
</dt> <dd>

La contraseña que se usa para autenticarse con el servidor proxy, o la cadena vacía si no se necesita autenticación.

WUA no utiliza estos datos si **szProxyAddr** está vacío.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




