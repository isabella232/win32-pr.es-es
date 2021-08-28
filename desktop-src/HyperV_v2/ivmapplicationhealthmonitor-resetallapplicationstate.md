---
description: Restablece el estado de mantenimiento de todas las aplicaciones de una máquina virtual.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: IVmApplicationHealthMonitor::ResetAllApplicationState (método)
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
ms.openlocfilehash: 4e97d5d16200501d77acf8b0b02cc5562d51706fcc46298421ad7f7e8fc0dfac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694355"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>IVmApplicationHealthMonitor::ResetAllApplicationState (método)

Restablece el estado de mantenimiento de todas las aplicaciones de una máquina virtual. Si se realiza correctamente, el estado de mantenimiento de todas las aplicaciones supervisadas se establecerá **en ApplicationStateHealthy.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Para usar este elemento de programación, Windows 8 componentes de integración deben instalarse en la máquina virtual en la que se ejecuta la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                                |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                      |
| Versión<br/>                  | Componentes de integración para Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




