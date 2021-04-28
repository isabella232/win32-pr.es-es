---
title: Método SetDisableForcibleLogoff de la Win32_TerminalServiceSetting clase
description: 'Método SetDisableForcibleLogoff de la Win32_TerminalServiceSetting clase : este método no se admite.'
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Método SetDisableForcibleLogoff Servicios de Escritorio remoto
- Método SetDisableForcibleLogoff Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetDisableForcibleLogoff
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103713"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a>Método SetDisableForcibleLogoff de la clase \_ TerminalServiceSetting de Win32

No se admite este método.

**Windows Vista y Windows Server 2008:** Habilita o deshabilita si un administrador que ha iniciado sesión en la consola se puede desactivar forzadamente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DisableForcibleLogoff* \[ En\]
</dt> <dd>

Marca la deshabilitación o habilitación de la propiedad **DisableForcibleLogoff,** que determina si un administrador que ha iniciado sesión en la consola se puede desactivar forzosamente.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Deshabilite la propiedad . El administrador conectado puede estar cerrado forzadamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilite la propiedad . El administrador conectado no se puede desactivar forzadamente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Fin de compatibilidad de cliente<br/>    | Windows Vista<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





