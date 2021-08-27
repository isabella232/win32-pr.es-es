---
title: Método GetGracePeriodDays de la Win32_TerminalServiceSetting clase
description: Recupera el número de días restantes en el período de gracia Servicios de Escritorio remoto licencias para un servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto). Un valor cero indica que el período de gracia ha terminado.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Método GetGracePeriodDays Servicios de Escritorio remoto
- Método GetGracePeriodDays Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto método , GetGracePeriodDays
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbfe1a99fb0b4f12db19f018d8acb3aaee6ab15a3560cd9140c3a05f36986585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010125"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a>Método GetGracePeriodDays de la clase \_ TerminalServiceSetting de Win32

Recupera el número de días restantes en el período de gracia Servicios de Escritorio remoto licencias para un servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto). Un valor cero indica que el período de gracia ha terminado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DaysLeft* \[ out\]
</dt> <dd>

Número de días restantes en el período de gracia.

</dd> </dl>

## <a name="remarks"></a>Comentarios

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
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

