---
title: Método GetCurrentVMMPlugin de la Win32_SessionDirectoryVMMPlugin clase
description: Obtiene el complemento de prioridad más alta que está habilitado.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Método GetCurrentVMMPlugin Servicios de Escritorio remoto
- Método GetCurrentVMMPlugin Servicios de Escritorio remoto , Win32_SessionDirectoryVMMPlugin clase
- Win32_SessionDirectoryVMMPlugin clase Servicios de Escritorio remoto método , GetCurrentVMMPlugin
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
ms.openlocfilehash: 4cc683275581aeb00c654a30e8c5aba7fd920f58248b480fc39caa96c885bb7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080115"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método GetCurrentVMMPlugin de la clase \_ SessionDirectoryVMMPlugin de Win32

Obtiene el complemento de prioridad más alta que está habilitado.

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

*sName* \[ out\]
</dt> <dd>

Nombre del complemento.

</dd> <dt>

*sProvider* \[ out\]
</dt> <dd>

Nombre del proveedor del complemento.

</dd> <dt>

*sServiceLocation* \[ out\]
</dt> <dd>

Ubicación del servicio con la que debe ponerse en contacto el complemento.

</dd> <dt>

*sClassID* \[ out\]
</dt> <dd>

Identificador de clase del complemento.

</dd> <dt>

*Prioridad* \[ out\]
</dt> <dd>

Prioridad del complemento. Cuanto mayor sea el valor, mayor será la prioridad del complemento.

</dd> <dt>

*Habilitado* \[ out\]
</dt> <dd>

Indica si el complemento está habilitado o deshabilitado. **True** si el complemento está habilitado o **false** de lo contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





