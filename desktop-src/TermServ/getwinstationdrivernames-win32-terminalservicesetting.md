---
title: Método GetWinstationDriverNames de la Win32_TerminalServiceSetting clase
description: Recupera una lista de nombres de controladores de Winstation.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- Método GetWinstationDriverNames Servicios de Escritorio remoto
- Método GetWinstationDriverNames Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método GetWinstationDriverNames
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968459"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a>Método GetWinstationDriverNames de la clase \_ TerminalServiceSetting de Win32

Recupera una lista de nombres de controladores de Winstation.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*WinstaDriverNames* \[ out\]
</dt> <dd>

Lista de nombres de controladores de Winstation.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para conectarse al espacio \\ de nombres Raíz de \\ TerminalServices CIMV2, el nivel de \\ autenticación debe incluir privacidad de paquetes. Para las llamadas de C/C++, se trata de un nivel de autenticación de **RPC \_ C \_ AUTHN LEVEL \_ \_ PKT \_ PRIVACY**. Para Visual Basic y llamadas de scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6. En el ejemplo Visual Basic Scripting Edition (VBScript) siguiente se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contienen las definiciones de las clases Windows Management Instrumentation (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

