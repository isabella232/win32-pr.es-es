---
title: Método WSMan. CreateSession (WSManDisp. h)
description: Crea un objeto de sesión que se puede usar para las operaciones de red subsiguientes.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Método CreateSession Administración remota de Windows
- Administración remota de Windows método CreateSession, objeto WSMan
- Administración remota de Windows de objeto WSMan, método CreateSession
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
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534528"
---
# <a name="wsmancreatesession-method"></a>WSMan. CreateSession (método)

Crea un objeto de [**sesión**](session.md) que se puede usar para las operaciones de red subsiguientes.

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

*conexión* \[ de en, opcional\]
</dt> <dd>

Protocolo y servicio al que se va a conectar, incluido IPv4 o IPv6. El formato de la información de conexión es el siguiente: <sufijo de dirección de *transporte* ><  >< >. Para obtener ejemplos, vea la sección Comentarios. Si no se proporciona información de conexión, se utiliza el equipo local.

</dd> <dt>

*marcas* \[ de en, opcional\]
</dt> <dd>

Marcas de sesión que especifican el método de autenticación, como [*negociar autenticación*](windows-remote-management-glossary.md) o [*autenticación implícita*](windows-remote-management-glossary.md), para conectarse a un equipo remoto. Estas marcas también especifican otra información de conexión de la sesión, como la codificación o el cifrado. Este parámetro debe contener una o varias marcas en **\_ \_ WSManSessionFlags** para una conexión remota. Para obtener más información, vea [constantes de sesión](session-constants.md). No se requiere ninguna configuración de marca para una conexión a WinRM en el equipo local. El valor predeterminado es **WSManFlagUseNegotiate**.

Para obtener más información, consulte [autenticación para las conexiones remotas](authentication-for-remote-connections.md) y el parámetro *connectionOptions* .

</dd> <dt>

*connectionOptions* \[ en, opcional\]
</dt> <dd>

Un puntero a un objeto [**ConnectionOptions**](connectionoptions.md) que contiene un nombre de usuario y una contraseña. El valor predeterminado es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto de [**sesión**](session.md) que se puede usar para realizar operaciones WinRM locales o remotas.

## <a name="remarks"></a>Observaciones

El método **createSession** inicializa el objeto de [**sesión**](session.md) mediante la recopilación de parámetros, como marcas, credenciales y una cadena de conexión para el parámetro de *conexión* . **CreateSession** realmente no se conecta al equipo local o remoto. Si no se puede establecer la conexión, se produce un error en la primera operación de **sesión** , como [**Get**](session-get.md) o [**Enumerate**](session-enumerate.md), después de la llamada a **createSession**. Este comportamiento difiere de una conexión [*WMI*](windows-remote-management-glossary.md) a un [*espacio de nombres*](windows-remote-management-glossary.md) de un equipo remoto. Para obtener más información, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).

El siguiente ejemplo de código VBScript se usa para llamar a este método.


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



En los ejemplos siguientes se muestran los distintos formatos que se usan para especificar la información de conexión en el parámetro de *conexión* (al crear una sesión https, el campo de *Dirección* <> debe coincidir con el nombre del certificado de equipo del servidor; de lo contrario, se producirá un error):

-   "https://service"

    Usa HTTPS para conectarse a la ubicación del servicio Web predeterminada.

-   "https://service.corp.com/websvcs/wsman"

    Usa HTTPS para conectarse a la ubicación del servicio Web específica.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] "

    Usa HTTPS e IPv6 con el puerto predeterminado.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] : 9999/wsman"

    Usa HTTPS e IPv6 con el puerto especificado.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se crea una sesión en el equipo local.


```VB
 Set NewSession = Wsman.CreateSession   
   
```



En el siguiente ejemplo de código de VBScript se crea una sesión en un equipo remoto que se identifica mediante una dirección IP. El script proporciona un nombre de usuario y una contraseña para una cuenta. Las marcas **WSManFlagCredUserNamePassword** y **WSManFlagUseBasic** se combinan para indicar que la cuenta es una cuenta local en el equipo remoto. Si se produce un error en la creación de la sesión, el script finaliza. El script usa los métodos que devuelven la constante, como [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md).

Para ejecutar este script, tenga en cuenta que debe configurar las opciones de configuración predeterminadas para el cliente y el servidor para permitir el tráfico no cifrado y la autenticación básica (**AllowUnencrypted** establecido en **true** y Basic en **true**). Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



En el siguiente ejemplo de código de VBScript, la cuenta es una cuenta de dominio y se utiliza la autenticación Negotiate. Con Negotiate Authentication, debe especificar el nombre de usuario como `computername\username` o `ipaddress\username` .


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
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**De sesión**](session.md)
</dt> <dt>

[Autenticación para conexiones remotas](authentication-for-remote-connections.md)
</dt> <dt>

[Instalación y configuración de Administración remota de Windows](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





