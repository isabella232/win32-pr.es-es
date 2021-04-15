---
title: Método ChangeMode de la clase Win32_TerminalServiceSetting
description: El método ChangeMode establece el tipo de licencia del servidor host de sesión de escritorio remoto (host de sesión de RD) Escritorio remoto actual.
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Método ChangeMode Servicios de Escritorio remoto
- Método ChangeMode Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422257"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>Método ChangeMode de la \_ clase TerminalServiceSetting de Win32

El método **ChangeMode** establece el tipo de licencia del servidor host de sesión de escritorio remoto (host de sesión de RD) escritorio remoto actual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LicensingType* \[ de\]
</dt> <dd>

Tipo de licencia que se va a establecer en función del modo de servidor host de sesión de escritorio remoto.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Servidor host de sesión de escritorio remoto personal.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Escritorio remoto para administración.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Por dispositivo/por puesto. Válido para los servidores de aplicaciones.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Por usuario. Válido para los servidores de aplicaciones.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

