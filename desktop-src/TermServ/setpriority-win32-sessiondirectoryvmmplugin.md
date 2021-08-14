---
title: Método SetPriority de la Win32_SessionDirectoryVMMPlugin clase
description: Establece la prioridad del complemento.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- Método SetPriority Servicios de Escritorio remoto
- Método SetPriority Servicios de Escritorio remoto , Win32_SessionDirectoryVMMPlugin clase
- Win32_SessionDirectoryVMMPlugin clase Servicios de Escritorio remoto , método SetPriority
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
ms.openlocfilehash: 3dfe18b5998a1b8576cbd1a8f3c793e355469cfeff44f585dcb167a3b154803a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987745"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetPriority de la clase \_ SessionDirectoryVMMPlugin de Win32

Establece la prioridad del complemento.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Prioridad* \[ En\]
</dt> <dd>

Prioridad del complemento. Cuanto mayor sea el valor, mayor será la prioridad del complemento. La prioridad es cero de forma predeterminada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





