---
title: Método Create de la clase Win32_Terminal
description: Crea un terminal con valores predeterminados que se pueden personalizar mediante las propiedades y los métodos de las \_ clases TerminalSetting de Win32.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create Method Servicios de Escritorio remoto, Win32_Terminal (clase)
- Win32_Terminal Servicios de Escritorio remoto de clase, Create (método)
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489533"
---
# <a name="create-method-of-the-win32_terminal-class"></a>Método Create de la \_ clase de terminal Win32

El método **Create** crea un terminal con valores predeterminados que se pueden personalizar mediante las propiedades y los métodos de las clases [**\_ TerminalSetting de Win32**](win32-terminalsetting.md) . La función devuelve cero si se ejecuta correctamente y un error en el error.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewTerminalName* \[ de\]
</dt> <dd>

Nombre del terminal.

</dd> <dt>

*Transporte* \[ de de\]
</dt> <dd>

Transporte para el terminal. Esta es una propiedad de la [**clase \_ TSGeneralSetting de Win32**](win32-tsgeneralsetting.md) .

</dd> <dt>

*TerminalProtocol* \[ de\]
</dt> <dd>

Protocolo para el terminal. Esta es una propiedad de la [**clase \_ TSGeneralSetting de Win32**](win32-tsgeneralsetting.md) .

</dd> </dl>

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

[**\_Terminal Win32**](win32-terminal.md)
</dt> </dl>

 

