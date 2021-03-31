---
title: Método TimeLimit de la clase Win32_TSSessionSetting
description: Establece el tiempo máximo asignado al tipo de límite de sesión especificado.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Método TimeLimit Servicios de Escritorio remoto
- Método TimeLimit Servicios de Escritorio remoto, clase Win32_TSSessionSetting
- Win32_TSSessionSetting de clase Servicios de Escritorio remoto, método TimeLimit
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533783"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a>Método TimeLimit de la \_ clase TSSessionSetting de Win32

Establece el tiempo máximo asignado al tipo de límite de sesión especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SessionLimitType* \[ de\]
</dt> <dd>

Especifica el tipo de propiedad de límite de sesión que el método está estableciendo.

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**


</dt> <dd>

El método está estableciendo la propiedad **ActiveSessionLimit** .

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**


</dt> <dd>

El método está estableciendo la propiedad **DisconnectedSessionLimit** .

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**


</dt> <dd>

El método está estableciendo la propiedad **IdleSessionLimit** .

</dd> </dl> </dd> <dt>

*ValueLimit* \[ de\]
</dt> <dd>

Nuevo tiempo máximo, en milisegundos, para la propiedad especificada por el parámetro *SessionLimitType* . El valor cero indica que no hay límite de sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en control de directiva de grupo.

## <a name="remarks"></a>Observaciones

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

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> </dl>

 

