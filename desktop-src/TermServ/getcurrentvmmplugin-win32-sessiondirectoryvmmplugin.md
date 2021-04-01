---
title: Método GetCurrentVMMPlugin de la clase Win32_SessionDirectoryVMMPlugin
description: Obtiene el complemento de prioridad máxima que está habilitado.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Método GetCurrentVMMPlugin Servicios de Escritorio remoto
- Método GetCurrentVMMPlugin Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de clase Servicios de Escritorio remoto, método GetCurrentVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905615"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método GetCurrentVMMPlugin de la \_ clase SessionDirectoryVMMPlugin de Win32

Obtiene el complemento de prioridad máxima que está habilitado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sName* \[ enuncia\]
</dt> <dd>

Nombre del complemento.

</dd> <dt>

*sProvider* \[ enuncia\]
</dt> <dd>

Nombre del proveedor del complemento.

</dd> <dt>

*sServiceLocation* \[ enuncia\]
</dt> <dd>

La ubicación del servicio en la que debe ponerse en contacto el complemento.

</dd> <dt>

*sClassID* \[ enuncia\]
</dt> <dd>

Identificador de clase del complemento.

</dd> <dt>

*Prioridad* \[ de enuncia\]
</dt> <dd>

Prioridad del complemento. Cuanto mayor sea el valor, mayor será la prioridad del complemento.

</dd> <dt>

*Habilitado* \[ enuncia\]
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

 

 





