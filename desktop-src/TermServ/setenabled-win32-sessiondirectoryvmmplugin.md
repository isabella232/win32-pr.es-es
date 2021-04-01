---
title: Método SetEnabled de la clase Win32_SessionDirectoryVMMPlugin
description: Habilita o deshabilita el complemento.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- Método SetEnabled Servicios de Escritorio remoto
- Método SetEnabled Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin Servicios de Escritorio remoto de clase, método SetEnabled
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803859"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetEnabled de la \_ clase SessionDirectoryVMMPlugin de Win32

Habilita o deshabilita el complemento.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

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

 

 





