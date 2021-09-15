---
title: Método SetMaxYResolution de la Win32_TSClientSetting clase
description: Establece la propiedad MaxYResolution.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- Método SetMaxYResolution Servicios de Escritorio remoto
- Método SetMaxYResolution Servicios de Escritorio remoto , Win32_TSClientSetting clase
- Win32_TSClientSetting clase Servicios de Escritorio remoto , método SetMaxYResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258991"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a>Método SetMaxYResolution de la clase \_ TSClientSetting de Win32

Establece la **propiedad MaxYResolution.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaxYResolution* \[ En\]
</dt> <dd>

Nueva resolución Y máxima compatible con el servidor. El valor mínimo es 200 y el valor máximo es 2048.

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

 

 





