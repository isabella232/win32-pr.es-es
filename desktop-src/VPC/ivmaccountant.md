---
title: Interfaz IVMAccountant (VPCCOMInterfaces.h)
description: Proporciona acceso a la información relacionada con la contabilidad de una máquina virtual.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- IVMAccountant interface Virtual PC
- IVMAccountant interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae791ce6cd1cd401beba4ff200ffbb54213b89d642c478eca7eb3b3057b4acb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473715"
---
# <a name="ivmaccountant-interface"></a>Interfaz IVMAccountant

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Proporciona acceso a la información relacionada con la contabilidad de una máquina virtual. Para recuperar **el IVMAccountant** de una máquina virtual, use la [**propiedad IVMVirtualMachine::Accountant.**](ivmvirtualmachine-accountant.md)

## <a name="members"></a>Miembros

La **interfaz IVMAccountant** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMAccountant** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMAccountant** tiene estas propiedades.



| Propiedad                                                                        | Tipo de acceso          | Descripción                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**CPUUtilization**](ivmaccountant-cpuutilization.md)<br/>               | Solo lectura<br/> | Porcentaje de uso actual de cpu para esta máquina virtual.<br/>                          |
| [**CPUUtilizationHistory**](ivmaccountant-cpuutilizationhistory.md)<br/> | Solo lectura<br/> | Uso reciente de la CPU de esta máquina virtual (como una matriz de valores de porcentaje).<br/>       |
| [**DiskBytesRead**](ivmaccountant-diskbytesread.md)<br/>                 | Solo lectura<br/> | Número total de bytes leídos por todos los controladores de almacenamiento para esta máquina virtual.<br/>          |
| [**DiskBytesWritten**](ivmaccountant-diskbyteswritten.md)<br/>           | Solo lectura<br/> | Número total de bytes escritos por todos los controladores de almacenamiento para esta máquina virtual.<br/>       |
| [**NetworkBytesReceived**](ivmaccountant-networkbytesreceived.md)<br/>   | Solo lectura<br/> | Número total de bytes recibidos por todos los adaptadores de red virtual para esta máquina virtual.<br/> |
| [**NetworkBytesSent**](ivmaccountant-networkbytessent.md)<br/>           | Solo lectura<br/> | Número total de bytes enviados por todos los adaptadores de red virtual para esta máquina virtual.<br/>     |
| [**Uptime**](ivmaccountant-uptime.md)<br/>                               | Solo lectura<br/> | Número de segundos que la máquina virtual se ha estado ejecutando.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMAccountant se define como \_ 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



 

