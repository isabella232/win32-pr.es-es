---
title: Método UpdateDirectConnectLicenseServer de la clase Win32_TerminalServiceSetting
description: UpdateDirectConnectLicenseServer ya no está disponible.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- Método UpdateDirectConnectLicenseServer Servicios de Escritorio remoto
- Método UpdateDirectConnectLicenseServer Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método UpdateDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676771"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método UpdateDirectConnectLicenseServer de la \_ clase TerminalServiceSetting de Win32

\[**UpdateDirectConnectLicenseServer** ya no está disponible para su uso a partir de Windows Server 2008 R2.\]

**Windows Server 2008:** Actualiza la lista de servidores de licencias de detección. La lista de servidores está delimitada por signos de punto y coma (";").

## <a name="syntax"></a>Sintaxis


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LicenseServerList* \[ de\]
</dt> <dd>

Lista de servidores de licencias.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

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

 

