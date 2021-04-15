---
title: Método SetMaxMonitors de la clase Win32_TSClientSetting
description: Establece la propiedad MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Método SetMaxMonitors Servicios de Escritorio remoto
- Método SetMaxMonitors Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetMaxMonitors
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676806"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a>Método SetMaxMonitors de la \_ clase TSClientSetting de Win32

Establece la propiedad **MaxMonitors** .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaxMonitors* \[ de\]
</dt> <dd>

Especifica el nuevo número máximo de monitores admitidos por el servidor. El valor mínimo es 1 y el valor máximo es 10.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si el servidor invalida la configuración de conexión del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





