---
title: Método GetGracePeriodDays de la clase Win32_TerminalServiceSetting
description: Recupera el número de días que quedan en el Servicios de Escritorio remoto período de gracia de licencias de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Un valor cero indica que el período de gracia es superior.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Método GetGracePeriodDays Servicios de Escritorio remoto
- Método GetGracePeriodDays Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetGracePeriodDays
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
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359693"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a>Método GetGracePeriodDays de la \_ clase TerminalServiceSetting de Win32

Recupera el número de días que quedan en el Servicios de Escritorio remoto período de gracia de licencias de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Un valor cero indica que el período de gracia es superior.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DaysLeft* \[ enuncia\]
</dt> <dd>

Número de días que quedan en el período de gracia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

