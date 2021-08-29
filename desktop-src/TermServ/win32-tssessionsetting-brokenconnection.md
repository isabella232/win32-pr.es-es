---
title: Método BrokenConnection de la Win32_TSSessionSetting (Wtsprotocol.h)
description: Establece la propiedad BrokenConnectionAction, que es la acción que realiza el servidor si se alcanza el límite de tiempo de sesión o si se ha roto la conexión.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Método BrokenConnection Servicios de Escritorio remoto
- Método BrokenConnection Servicios de Escritorio remoto , Win32_TSSessionSetting clase
- Win32_TSSessionSetting clase Servicios de Escritorio remoto , método BrokenConnection
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba52de0d70c6f7e45b268fd879542ce64ed4a3b6fbe26dd994ad6723fb819857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137578"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a>Método BrokenConnection de la clase \_ TSSessionSetting de Win32

Establece la **propiedad BrokenConnectionAction,** que es la acción que realiza el servidor si se alcanza el límite de tiempo de sesión o si se ha roto la conexión.

## <a name="syntax"></a>Sintaxis


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BrokenConnectionAction* \[ En\]
</dt> <dd>

La acción que se va a realizar.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Desconectar** (0)


</dt> <dd>

El usuario está desconectado de la sesión.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)


</dt> <dd>

La sesión se elimina permanentemente del servidor.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo directiva de grupo control .

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| Header<br/>                   | <dl> <dt>Wtsprotocol.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> </dl>

 

