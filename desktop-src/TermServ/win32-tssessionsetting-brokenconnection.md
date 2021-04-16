---
title: Método BrokenConnection de la clase Win32_TSSessionSetting (Wtsprotocol. h)
description: Establece la propiedad BrokenConnectionAction, que es la acción que realiza el servidor si se alcanza el límite de tiempo de sesión o si se interrumpe la conexión.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Método BrokenConnection Servicios de Escritorio remoto
- Método BrokenConnection Servicios de Escritorio remoto, clase Win32_TSSessionSetting
- Win32_TSSessionSetting de clase Servicios de Escritorio remoto, método BrokenConnection
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
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685958"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a>Método BrokenConnection de la \_ clase TSSessionSetting de Win32

Establece la propiedad **BrokenConnectionAction** , que es la acción que realiza el servidor si se alcanza el límite de tiempo de sesión o si se interrumpe la conexión.

## <a name="syntax"></a>Sintaxis


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BrokenConnectionAction* \[ de\]
</dt> <dd>

La acción que se va a realizar.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Desconectar** (0)


</dt> <dd>

El usuario se desconecta de la sesión.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (1)


</dt> <dd>

La sesión se elimina permanentemente del servidor.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en directiva de grupo control.

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Wtsprotocol. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> </dl>

 

