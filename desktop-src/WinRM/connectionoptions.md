---
title: Objeto ConnectionOptions (WSManDisp. h)
description: El objeto ConnectionOptions se pasa al método CreateSession para proporcionar el nombre de usuario y la contraseña asociados a la cuenta local en el equipo remoto.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Objeto ConnectionOptions Administración remota de Windows
- Administración remota de Windows de objeto ConnectionOptions, descrito
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705157"
---
# <a name="connectionoptions-object"></a>Objeto ConnectionOptions

El objeto **ConnectionOptions** se pasa al método [**createSession**](wsman-createsession.md) para proporcionar el nombre de usuario y la contraseña asociados a la cuenta local en el equipo remoto. Si no se proporciona ningún parámetro, las credenciales de la cuenta que ejecuta el script se establecen en los valores predeterminados.

## <a name="members"></a>Miembros

El objeto **ConnectionOptions** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **ConnectionOptions** tiene estas propiedades.



| Propiedad                                                  | Tipo de acceso           | Descripción                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Contraseña**](connectionoptions-password.md)<br/> | Solo escritura<br/> | Establece la contraseña de una cuenta local o de dominio en el equipo remoto.<br/>           |
| [**Nombre**](connectionoptions-username.md)<br/> | Lectura/escritura<br/> | Establece y obtiene el nombre de usuario de una cuenta local o de dominio en el equipo remoto.<br/> |



 

## <a name="remarks"></a>Observaciones

El objeto **ConnectionOptions** corresponde a la interfaz [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .

Si una aplicación cliente de Administración remota de Windows se ejecuta bajo suplantación, se produce un error si se establece la propiedad [**contraseña**](connectionoptions-password.md) . Una aplicación cliente es un script u otro programa que envía una solicitud a WinRM en el equipo local o remoto. Es posible que la aplicación cliente se esté ejecutando bajo suplantación porque llamó a una función como [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)). Una página Active Server (ASP) o un servicio no pueden solicitar un nombre de usuario y una contraseña si el proceso de ASP se ejecuta en una cuenta que suplanta a un cliente.

La marca **WSManFlagCredUserNamePassword** debe establecerse en la llamada [**WSman. createSession**](wsman-createsession.md) cuando se usa el [**nombre de usuario**](connectionoptions-username.md) y la [**contraseña**](connectionoptions-password.md) para la autenticación.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra cómo crear un objeto **ConnectionOptions** , cómo establecer las propiedades de la cuenta en el equipo remoto y cómo usarla para crear un objeto de [**sesión**](session.md) .


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
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

[Autenticación para conexiones remotas](authentication-for-remote-connections.md)
</dt> <dt>

[API de scripting de WinRM](winrm-scripting-api.md)
</dt> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Scripting en Administración remota de Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtención de datos del equipo local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtención de datos de un equipo remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

