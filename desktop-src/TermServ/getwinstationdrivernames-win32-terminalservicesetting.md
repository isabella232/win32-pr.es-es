---
title: Método GetWinstationDriverNames de la clase Win32_TerminalServiceSetting
description: Recupera una lista de los nombres de controlador de la estación de la.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- Método GetWinstationDriverNames Servicios de Escritorio remoto
- Método GetWinstationDriverNames Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetWinstationDriverNames
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bc0157f368edf129f578765c1b8d73f6f48a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685934"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a>Método GetWinstationDriverNames de la \_ clase TerminalServiceSetting de Win32

Recupera una lista de los nombres de controlador de la estación de la.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*WinstaDriverNames* \[ enuncia\]
</dt> <dd>

Lista de los nombres de controlador de la estación de la

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

 

