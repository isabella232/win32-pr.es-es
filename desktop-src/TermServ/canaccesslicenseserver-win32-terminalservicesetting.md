---
title: Método CanAccessLicenseServer de la clase Win32_TerminalServiceSetting
description: CanAccessLicenseServer ya no está disponible.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Método CanAccessLicenseServer Servicios de Escritorio remoto
- Método CanAccessLicenseServer Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método CanAccessLicenseServer
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
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150040"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método CanAccessLicenseServer de la \_ clase TerminalServiceSetting de Win32

\[**CanAccessLicenseServer** ya no está disponible para su uso a partir de Windows Server 2008 R2.\]

* * Windows Server 2008: * *

Determina si el servidor host Escritorio remoto de sesión de RD (host de sesión de escritorio remoto) puede solicitar Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) desde un servidor de licencias de Escritorio remoto basado en lo siguiente:

-   La configuración de directiva de grupo "grupo de seguridad del servidor de licencias" en el servidor de licencias de Escritorio remoto.
-   Pertenencia al grupo local de equipos Terminal Server en el servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NombreDeServidor* \[ de\]
</dt> <dd>

Nombre del servidor de licencias de Escritorio remoto.

</dd> <dt>

*AccessAllowed* \[ enuncia\]
</dt> <dd>

Si el servidor host de sesión de escritorio remoto puede solicitar cal de RDS del servidor de licencias.

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

Devuelve **S \_ correcto** si el servidor host de sesión de escritorio remoto tiene acceso al servidor de licencias. Devuelve **S \_ false** si el servidor host de sesión de escritorio remoto no tiene acceso al servidor de licencias.

## <a name="remarks"></a>Observaciones

La configuración de directiva "grupo de seguridad del servidor de licencias" le permite especificar los servidores host de sesión de escritorio remoto que pueden ponerse en contacto con el servidor de licencias para obtener Cal de RDS. Si la configuración de directiva está habilitada en el servidor de licencias, el servidor de licencias sólo responderá a las solicitudes CAL de RDS de los servidores host de sesión de escritorio remoto cuyas cuentas de equipo sean miembros del grupo local de Terminal Server equipos en el servidor de licencias.

Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes. En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C. En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6. En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

