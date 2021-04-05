---
title: Método SetPriority de la clase Win32_SessionDirectoryVMMPlugin
description: Establece la prioridad del complemento.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- SetPriority (método) Servicios de Escritorio remoto
- Método SetPriority Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Clase Win32_SessionDirectoryVMMPlugin Servicios de Escritorio remoto, método SetPriority
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997075"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetPriority de la \_ clase Win32 SessionDirectoryVMMPlugin

Establece la prioridad del complemento.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Prioridad* \[ de de\]
</dt> <dd>

Prioridad del complemento. Cuanto mayor sea el valor, mayor será la prioridad del complemento. De forma predeterminada, la prioridad es cero.

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

 

 





