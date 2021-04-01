---
description: Restablece el estado de mantenimiento de todas las aplicaciones de una máquina virtual.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'IVmApplicationHealthMonitor:: ResetAllApplicationState (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908449"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>IVmApplicationHealthMonitor:: ResetAllApplicationState (método)

Restablece el estado de mantenimiento de todas las aplicaciones de una máquina virtual. Si se realiza correctamente, el estado de mantenimiento de todas las aplicaciones supervisadas se establecerá en **ApplicationStateHealthy**.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Para usar este elemento de programación, los componentes de integración de Windows 8 deben estar instalados en la máquina virtual en la que se ejecuta la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                      |
| Versión<br/>                  | Componentes de integración para Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




