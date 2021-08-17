---
title: Método WSMan.CreateSession (WSManDisp.h)
description: Crea un objeto Session que, a continuación, se puede usar para las operaciones de red posteriores.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Método CreateSession Windows administración remota
- Método CreateSession Windows administración remota , objeto WSMan
- Objeto WSMan Windows administración remota, método CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330f8ea6456001c7e3b81dfbfeb07a125d30a5069596ef7d4f3e6ad561994ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742617"
---
# <a name="wsmancreatesession-method"></a>Método WSMan.CreateSession

Crea un [**objeto Session**](session.md) que, a continuación, se puede usar para las operaciones de red posteriores.

## <a name="syntax"></a>Sintaxis


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*conexión* \[ en, opcional\]
</dt> <dd>

Protocolo y servicio al que se conectará, incluidos IPv4 o IPv6. El formato de la información de conexión es el siguiente: <*sufijo de* >< *dirección de* transporte >< >. Para obtener ejemplos, vea Comentarios. Si no se proporciona información de conexión, se usa el equipo local.

</dd> <dt>

*flags* \[ en, opcional\]
</dt> <dd>

Marcas de sesión que especifican el método de autenticación, como la autenticación [*Negotiate*](windows-remote-management-glossary.md) o [*la autenticación implícita,*](windows-remote-management-glossary.md)para conectarse a un equipo remoto. Estas marcas también especifican otra información de conexión de sesión, como la codificación o el cifrado. Este parámetro debe contener una o varias de las marcas de **\_ \_ WSManSessionFlags** para una conexión remota. Para obtener más información, vea [Constantes de sesión](session-constants.md). No se requiere ninguna configuración de marca para una conexión a WinRM en el equipo local. El valor predeterminado **es WSManFlagUseNegotiate.**

Para obtener más información, vea [Autenticación para conexiones remotas](authentication-for-remote-connections.md) y el *parámetro connectionOptions.*

</dd> <dt>

*connectionOptions* \[ en, opcional\]
</dt> <dd>

Puntero a un [**objeto ConnectionOptions**](connectionoptions.md) que contiene un nombre de usuario y una contraseña. El valor predeterminado es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**Session**](session.md) que, a continuación, se puede usar para realizar operaciones winRM locales o remotas.

## <a name="remarks"></a>Comentarios

El **método CreateSession** inicializa el objeto [**Session**](session.md) mediante la recopilación de parámetros, como marcas, credenciales y una cadena de conexión para el *parámetro de* conexión. **CreateSession** no se conecta realmente al equipo local o remoto. Si no se puede establecer la conexión, se produce un error en la primera operación **session,** como [**Get**](session-get.md) o [**Enumerate**](session-enumerate.md), después de la llamada a **CreateSession**. Este comportamiento difiere de una conexión [*WMI*](windows-remote-management-glossary.md) a un espacio [*de nombres*](windows-remote-management-glossary.md) en un equipo remoto. Para obtener más información, [vea Windows Administración remota y WMI.](windows-remote-management-and-wmi.md)

El siguiente ejemplo de código VBScript se usa para llamar a este método.


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



En los ejemplos siguientes se muestran los  distintos formatos usados para especificar la información de conexión en el parámetro de conexión (al crear una sesión HTTPS, el campo> dirección *de* <debe coincidir con el nombre del certificado del equipo servidor; de lo contrario, se produce un error):

-   "https://service"

    Usa HTTPS para conectarse a la ubicación predeterminada del servicio web.

-   "https://service.corp.com/websvcs/wsman"

    Usa HTTPS para conectarse a la ubicación específica del servicio web.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420 \] "

    Usa HTTPS e IPv6 con el puerto predeterminado.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420 \] :9999/wsman"

    Usa HTTPS e IPv6 con el puerto dado.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se crea una sesión en el equipo local.


```VB
 Set NewSession = Wsman.CreateSession   
   
```



En el ejemplo de código de VBScript siguiente se crea una sesión en un equipo remoto identificado por una dirección IP. El script proporciona un nombre de usuario y una contraseña para una cuenta. Las marcas **WSManFlagCredUserNamePassword** y **WSManFlagUseBasic** se combinan para indicar que la cuenta es una cuenta local en el equipo remoto. Si se produce un error en la creación de la sesión, el script finaliza. El script usa los métodos que devuelven la constante, como [**WSMan.SessionFlagUseBasic.**](wsman-sessionflagusebasic.md)

Para ejecutar este script, tenga en cuenta que debe configurar las opciones de configuración predeterminadas para el cliente y el servidor para permitir el tráfico sin cifrar y la autenticación básica **(AllowUnencrypted** establecido en **True** y Basic establecido en **True).** Para obtener más información, [vea Instalación y configuración de Windows Administración remota.](installation-and-configuration-for-windows-remote-management.md)


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



En el siguiente ejemplo de código VBScript, la cuenta es una cuenta de dominio y se usa la autenticación Negotiate. Con la autenticación Negotiate, debe especificar el nombre de usuario como `computername\username` o `ipaddress\username` .


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Sesión**](session.md)
</dt> <dt>

[Autenticación para conexiones remotas](authentication-for-remote-connections.md)
</dt> <dt>

[Instalación y configuración de Windows administración remota](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





