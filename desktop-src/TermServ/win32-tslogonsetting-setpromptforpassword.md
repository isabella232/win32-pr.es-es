---
title: Método SetPromptForPassword de la Win32_TSLogonSetting clase
description: El método SetPromptForPassword establece la propiedad PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Método SetPromptForPassword Servicios de Escritorio remoto
- Método SetPromptForPassword Servicios de Escritorio remoto , Win32_TSLogonSetting clase
- Win32_TSLogonSetting clase Servicios de Escritorio remoto , método SetPromptForPassword
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90ea5202b0cfdfb624a05240deb042a88a8c73c8ea994cd810e1d9680ac0ddc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769525"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>Método SetPromptForPassword de la clase \_ TSLogonSetting de Win32

El **método SetPromptForPassword** establece la **propiedad PromptForPassword.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PromptForPassword* \[ En\]
</dt> <dd>

Marca que deshabilita o habilita la **propiedad PromptForPassword.**

<dt>

0
</dt> <dd>

Deshabilita la solicitud de contraseña.

</dd> <dt>

1
</dt> <dd>

Habilita la solicitud de contraseña.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

<dl> <dt>

**FALSE** (0)
</dt> <dt>

**TRUE** (1)
</dt> </dl>

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

