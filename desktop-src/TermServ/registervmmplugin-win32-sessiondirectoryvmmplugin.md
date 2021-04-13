---
title: Método RegisterVMMPlugin de la clase Win32_SessionDirectoryVMMPlugin
description: Registra un nuevo complemento de VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Método RegisterVMMPlugin Servicios de Escritorio remoto
- Método RegisterVMMPlugin Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de clase Servicios de Escritorio remoto, método RegisterVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422123"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método RegisterVMMPlugin de la \_ clase SessionDirectoryVMMPlugin de Win32

Registra un nuevo complemento de VMM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sName* \[ de\]
</dt> <dd>

Nombre del complemento.

</dd> <dt>

*sProvider* \[ de\]
</dt> <dd>

Nombre del proveedor del complemento.

</dd> <dt>

*sServiceLocation* \[ de\]
</dt> <dd>

La ubicación del servicio en la que debe ponerse en contacto el complemento.

</dd> <dt>

*sClassID* \[ de\]
</dt> <dd>

Identificador de clase del complemento.

</dd> <dt>

*Prioridad* \[ de de\]
</dt> <dd>

Prioridad del complemento. Cuanto mayor sea el valor, mayor será la prioridad del complemento.

</dd> <dt>

*Habilitado* \[ de\]
</dt> <dd>

Indica si el complemento está habilitado o deshabilitado. **True** si el complemento está habilitado o **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





