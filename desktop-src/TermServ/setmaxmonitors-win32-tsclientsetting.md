---
title: Método SetMaxMonitors de la Win32_TSClientSetting clase
description: Establece la propiedad MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Método SetMaxMonitors Servicios de Escritorio remoto
- Método SetMaxMonitors Servicios de Escritorio remoto , Win32_TSClientSetting clase
- Win32_TSClientSetting clase Servicios de Escritorio remoto , método SetMaxMonitors
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258996"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a>Método SetMaxMonitors de la clase \_ TSClientSetting de Win32

Establece la **propiedad MaxMonitors.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaxMonitors* \[ En\]
</dt> <dd>

Especifica el nuevo número máximo de monitores admitidos por el servidor. El valor mínimo es 1 y el valor máximo es 10.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si el servidor invalida la configuración de conexión del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





