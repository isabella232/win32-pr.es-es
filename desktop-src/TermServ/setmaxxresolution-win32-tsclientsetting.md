---
title: Método SetMaxXResolution de la Win32_TSClientSetting clase
description: Establece la propiedad MaxXResolution.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Método SetMaxXResolution Servicios de Escritorio remoto
- Método SetMaxXResolution Servicios de Escritorio remoto , Win32_TSClientSetting clase
- Win32_TSClientSetting clase Servicios de Escritorio remoto , método SetMaxXResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759a674e2b283d18caf1cc4d1b2f3e3ecae786dc76f9acc222f47dd8daf385de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000515"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a>Método SetMaxXResolution de la clase \_ TSClientSetting de Win32

Establece la **propiedad MaxXResolution.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaxXResolution* \[ En\]
</dt> <dd>

Nueva resolución X máxima compatible con el servidor. El valor mínimo es 200 y el valor máximo es 4096.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





