---
title: Objeto ConnectionOptions (WSManDisp.h)
description: El objeto ConnectionOptions se pasa al método CreateSession para proporcionar el nombre de usuario y la contraseña asociados a la cuenta local en el equipo remoto.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Objeto ConnectionOptions Windows administración remota
- Objeto ConnectionOptions Windows Administración remota , descrito
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
ms.openlocfilehash: f8665dc3a5be91fddb4332be3512ec9eec5c483495a21b95b641ec26e4e9e111
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734095"
---
# <a name="connectionoptions-object"></a>Objeto ConnectionOptions

El **objeto ConnectionOptions** se pasa al [**método CreateSession**](wsman-createsession.md) para proporcionar el nombre de usuario y la contraseña asociados a la cuenta local en el equipo remoto. Si no se proporciona ningún parámetro, las credenciales de la cuenta que ejecuta el script se establecen en los valores predeterminados.

## <a name="members"></a>Miembros

El **objeto ConnectionOptions** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto ConnectionOptions** tiene estas propiedades.



| Propiedad                                                  | Tipo de acceso           | Descripción                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Contraseña**](connectionoptions-password.md)<br/> | Solo escritura<br/> | Establece la contraseña de una cuenta local o de dominio en el equipo remoto.<br/>           |
| [**nombre de usuario**](connectionoptions-username.md)<br/> | Lectura/escritura<br/> | Establece y obtiene el nombre de usuario de una cuenta local o de dominio en el equipo remoto.<br/> |



 

## <a name="remarks"></a>Comentarios

El **objeto ConnectionOptions** corresponde a la [**interfaz IWSManConnectionOptions.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)

Si una Windows cliente de administración remota se ejecuta en suplantación, se produce un error si establece la [**propiedad Password.**](connectionoptions-password.md) Una aplicación cliente es un script u otro programa que envía una solicitud a WinRM en el equipo local o remoto. Es posible que la aplicación cliente se esté ejecutando en suplantación porque llamó a una función como [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)). Un Active Server (ASP) o servicio no puede solicitar un nombre de usuario y una contraseña si el proceso asp se ejecuta en una cuenta que suplanta a un cliente.

La **marca WSManFlagCredUserNamePassword** debe establecerse en la llamada [**a WSman.CreateSession**](wsman-createsession.md) cuando se usan [**UserName**](connectionoptions-username.md) y [**Password**](connectionoptions-password.md) para la autenticación.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra cómo crear un objeto **ConnectionOptions,** establecer las propiedades de la cuenta en el equipo remoto y usarlo en la creación de un [**objeto Session.**](session.md)


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Autenticación para conexiones remotas](authentication-for-remote-connections.md)
</dt> <dt>

[WinRM Scripting API](winrm-scripting-api.md)
</dt> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Scripting en Windows administración remota](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtener datos del equipo local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtener datos de un equipo remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

