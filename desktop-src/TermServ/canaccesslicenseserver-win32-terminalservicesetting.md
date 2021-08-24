---
title: Método CanAccessLicenseServer de la Win32_TerminalServiceSetting clase
description: CanAccessLicenseServer ya no está disponible.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Método CanAccessLicenseServer Servicios de Escritorio remoto
- Método CanAccessLicenseServer Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto método , CanAccessLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0512f42d0d814793f4ecd62fda2dd84005a4183e8db736bd16919799b4570a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139148"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método CanAccessLicenseServer de la clase TerminalServiceSetting de Win32 \_

\[**CanAccessLicenseServer** ya no está disponible para su uso a partir Windows Server 2008 R2.\]

**Windows Server 2008: **

Determina si el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) puede solicitar licencias de acceso de cliente (CAL de RDS) Servicios de Escritorio remoto un servidor de licencias de Escritorio remoto en función de lo siguiente:

-   La configuración de directiva de grupo "grupo de seguridad del servidor de licencias" en Escritorio remoto servidor de licencias.
-   Pertenencia al grupo local Equipos de Terminal Server en el servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ServerName* \[ En\]
</dt> <dd>

Nombre del servidor de Escritorio remoto de licencias.

</dd> <dt>

*AccessAllowed* \[ out\]
</dt> <dd>

Si el servidor host de sesión de Escritorio remoto puede solicitar CAL de RDS desde el servidor de licencias.

<dt>

0
</dt> <dd>

Se permite la solicitud.

</dd> <dt>

1
</dt> <dd>

No se permite la solicitud.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** el servidor host de sesión de Escritorio remoto tiene acceso al servidor de licencias. Devuelve **S \_ FALSE si** el servidor host de sesión de Escritorio remoto no tiene acceso al servidor de licencias.

## <a name="remarks"></a>Comentarios

La configuración de directiva "grupo de seguridad del servidor de licencias" permite especificar los servidores host de sesión de Escritorio remoto que pueden ponerse en contacto con el servidor de licencias para obtener cal de RDS. Si la configuración de directiva está habilitada en el servidor de licencias, el servidor de licencias solo responderá a las solicitudes cal de RDS de los servidores host de sesión de Escritorio remoto cuyas cuentas de equipo son miembros del grupo local Equipos de Terminal Server en el servidor de licencias.

Para conectarse al espacio \\ de nombres raíz de \\ TerminalServices cimv2, el nivel de \\ autenticación debe incluir privacidad de paquetes. Para las llamadas de C/C++, se trata de un nivel de autenticación de **RPC \_ C \_ AUTHN LEVEL \_ \_ PKT \_ PRIVACY**. Para Visual Basic y llamadas de scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6. En el ejemplo Visual Basic Scripting Edition (VBScript) siguiente se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

