---
title: Método RegisterVMMPlugin de la Win32_SessionDirectoryVMMPlugin clase
description: Registra un nuevo complemento vmm.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Método RegisterVMMPlugin Servicios de Escritorio remoto
- Método RegisterVMMPlugin Servicios de Escritorio remoto , Win32_SessionDirectoryVMMPlugin clase
- Win32_SessionDirectoryVMMPlugin clase Servicios de Escritorio remoto , método RegisterVMMPlugin
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
ms.openlocfilehash: 163fc00b63fcc29a1c9d7b2a9388db547509d7b24eada2caccbdfbf70d9a3287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865995"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método RegisterVMMPlugin de la clase \_ SessionDirectoryVMMPlugin de Win32

Registra un nuevo complemento vmm.

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

*sName* \[ En\]
</dt> <dd>

Nombre del complemento.

</dd> <dt>

*sProvider* \[ En\]
</dt> <dd>

Nombre del proveedor del complemento.

</dd> <dt>

*sServiceLocation* \[ En\]
</dt> <dd>

Ubicación del servicio con la que debe ponerse en contacto el complemento.

</dd> <dt>

*sClassID* \[ En\]
</dt> <dd>

Identificador de clase del complemento.

</dd> <dt>

*Prioridad* \[ En\]
</dt> <dd>

Prioridad del complemento. Cuanto mayor sea el valor, mayor será la prioridad del complemento.

</dd> <dt>

*Habilitado* \[ En\]
</dt> <dd>

Indica si el complemento está habilitado o deshabilitado. **True** si el complemento está habilitado o **false** de lo contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





