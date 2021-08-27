---
title: Propiedad ConnectionOptions.UserName (WSManDisp.h)
description: Establece y obtiene el nombre de usuario de una cuenta de dominio o local en el equipo remoto. Esta propiedad determina el nombre de usuario para la autenticación.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Propiedad UserName Windows Administración remota
- Propiedad UserName Windows de administración remota, objeto ConnectionOptions
- Objeto ConnectionOptions Windows administración remota, propiedad UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fa4cd5e1d4fd733431adab80241744c0b197960506cfe2908bc99315ecfdea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121785"
---
# <a name="connectionoptionsusername-property"></a>Propiedad ConnectionOptions.UserName

Establece y obtiene el nombre de usuario de una cuenta de dominio o local en el equipo remoto. Esta propiedad determina el nombre de usuario para la autenticación. Para obtener más información, vea [Autenticación para conexiones remotas.](authentication-for-remote-connections.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el nombre de usuario de una cuenta local o de dominio en el equipo remoto.

Si no se proporciona ningún valor y no se establece la marca **WSManFlagCredUsernamePassword,** se usa el nombre de usuario de la cuenta que ejecuta el script.

Si no se proporciona ningún valor y se establece la marca **WSManFlagCredUsernamePassword,** el script solicita al usuario que escriba el nombre de usuario y la contraseña. Si no se introducen un nombre de usuario y una contraseña válidos, se devuelve un error de acceso denegado.

## <a name="remarks"></a>Comentarios

La sintaxis siguiente se usa para especificar esta propiedad.


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



Puede proporcionar **UserName y** [**Password**](connectionoptions-password.md) para una cuenta de dominio al usar la autenticación [*negotiate*](windows-remote-management-glossary.md) o *Kerberos,* o para una cuenta local con [*autenticación*](windows-remote-management-glossary.md) básica. Para conectarse a una cuenta local, las marcas [**WSMan.CreateSession**](wsman-createsession.md) deben contener la combinación de la marca **WSManFlagUseBasic** y la marca **WsmanFlagCredUserNamePassword.** Para conectarse a una cuenta de dominio, las marcas **WSMan.CreateSession** deben contener la combinación de la marca **WSManFlagUseNegotiate** y la marca **WsmanFlagCredUserNamePassword,** o la combinación de la marca **WSManFlagUseKerberos** y la marca **WsmanFlagCredUserNamePassword.** Para una cuenta de dominio, **UserName** debe especificarse con el formato "nombre de usuario del equipo", donde la parte "equipo" de la cadena puede ser el nombre o la \\ dirección IP. Para obtener más información, vea [Autenticación para conexiones remotas.](authentication-for-remote-connections.md)


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



Para conectarse a una cuenta de dominio, las marcas [**WSMan.CreateSession**](wsman-createsession.md) deben contener la combinación de la marca **WSManFlagUseNegotiate** y la marca **WsmanFlagCredUserNamePassword** para conectarse a una cuenta de dominio, lo que requiere la autenticación Negotiate.


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
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

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





