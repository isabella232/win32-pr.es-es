---
title: Interfaz IVMAccountant (VPCCOMInterfaces. h)
description: Proporciona acceso a información relacionada con cuentas para una máquina virtual.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Interfaz IVMAccountant Virtual PC
- Interfaz IVMAccountant Virtual PC, descripción
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
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803757"
---
# <a name="ivmaccountant-interface"></a>Interfaz IVMAccountant

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Proporciona acceso a información relacionada con cuentas para una máquina virtual. Para recuperar el **IVMAccountant** de una máquina virtual, use la propiedad [**IVMVirtualMachine:: contable**](ivmvirtualmachine-accountant.md) .

## <a name="members"></a>Miembros

La interfaz **IVMAccountant** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMAccountant** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMAccountant** tiene estas propiedades.



| Propiedad                                                                        | Tipo de acceso          | Descripción                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**Gráfico**](ivmaccountant-cpuutilization.md)<br/>               | Solo lectura<br/> | El porcentaje de uso actual de la CPU para esta máquina virtual.<br/>                          |
| [**CPUUtilizationHistory**](ivmaccountant-cpuutilizationhistory.md)<br/> | Solo lectura<br/> | El uso de CPU reciente de esta máquina virtual (como una matriz de valores de porcentaje).<br/>       |
| [**DiskBytesRead**](ivmaccountant-diskbytesread.md)<br/>                 | Solo lectura<br/> | Número total de bytes leídos por todos los controladores de almacenamiento de esta máquina virtual.<br/>          |
| [**DiskBytesWritten**](ivmaccountant-diskbyteswritten.md)<br/>           | Solo lectura<br/> | Número total de bytes escritos por todos los controladores de almacenamiento de esta máquina virtual.<br/>       |
| [**NetworkBytesReceived**](ivmaccountant-networkbytesreceived.md)<br/>   | Solo lectura<br/> | El número total de bytes recibidos por todos los adaptadores de red virtual para esta máquina virtual.<br/> |
| [**NetworkBytesSent**](ivmaccountant-networkbytessent.md)<br/>           | Solo lectura<br/> | El número total de bytes enviados por todos los adaptadores de red virtual para esta máquina virtual.<br/>     |
| [**Actividad**](ivmaccountant-uptime.md)<br/>                               | Solo lectura<br/> | El número de segundos que se ha estado ejecutando la máquina virtual.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant se define como 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



 

