---
title: Método DumpVmInfo de la Win32_TSVm clase
description: Este miembro tiene fines de prueba interna y no debe usarse en el código.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Método DumpVmInfo Servicios de Escritorio remoto
- Método DumpVmInfo Servicios de Escritorio remoto , Win32_TSVm clase
- Win32_TSVm clase Servicios de Escritorio remoto método , DumpVmInfo
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c74602e09f7aab4909e78bcd4696a450419e929b89769b35e16f21cbcafc080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354026"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a>Método DumpVmInfo de la clase TSVm win32 \_

Este miembro tiene fines de prueba interna y no debe usarse en el código.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSVm**](win32-tsvm.md)
</dt> </dl>

 

 





