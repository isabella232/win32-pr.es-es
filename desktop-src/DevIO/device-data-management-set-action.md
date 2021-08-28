---
description: Defina el conjunto de acciones para el código de control ATRIBUTOS DE IOCTL \_ STORAGE \_ MANAGE DATA \_ \_ \_ SET.
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 602243e31645e1cc4706e3a3a2b954bb68fc2cbda58a0f0b6c9076ae6b0797f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654925"
---
# <a name="device_data_management_set_action"></a>ACCIÓN DEL \_ CONJUNTO DE ADMINISTRACIÓN DE DATOS DE \_ \_ \_ DISPOSITIVOS

Los siguientes valores constantes son el conjunto de valores posibles para el tipo **DE ACCIÓN DEVICE DATA MANAGEMENT \_ \_ \_ SET, \_** que se define como tipo **DWORD**.

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ None**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



No se realiza ninguna acción.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**Recorte de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Se realiza una acción de recorte.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**Notificación DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

2 \| **DeviceDsmActionFlag \_ nonDestructive** (0x80000002)
</dt> <dt>



Se realiza una acción de notificación. Los parámetros están en una [**estructura DEVICE DSM NOTIFICATION \_ \_ \_ PARAMETERS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) **DeviceDsmActionFlag \_ nonDestructive** (0x80000000) es una marca de bits para indicar a la pila de controladores que esta operación no es destructiva.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**
</dt> <dd> <dl> <dt>

3 \| **DeviceDsmActionFlag \_ nonDestructive** (0x80000003)
</dt> <dt>



Se realiza una acción de lectura de descarga. Los parámetros están en una [**estructura DEVICE \_ DSM \_ OFFLOAD READ \_ \_ PARAMETERS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) La salida está en una [**estructura STORAGE \_ OFFLOAD READ \_ \_ OUTPUT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) **DeviceDsmActionFlag \_ nonDestructive** (0x80000000) es una marca de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Se realiza una acción de escritura de descarga. Los parámetros están en una [**estructura DEVICE \_ DSM \_ OFFLOAD WRITE \_ \_ PARAMETERS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) La salida está en una [**estructura STORAGE \_ OFFLOAD WRITE \_ \_ OUTPUT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output)

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Asignación deviceDsmAction \_**
</dt> <dd> <dl> <dt>

5 \| **DeviceDsmActionFlag \_ nonDestructive** (0x80000005)
</dt> <dt>



Se devuelve un mapa de bits de asignación para el primer intervalo de conjunto de datos pasado. La salida está en una estructura [**DEVICE DATA SET LB PROVISIONING \_ \_ \_ \_ \_ STATE.**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) **DeviceDsmActionFlag \_ nonDestructive** (0x80000000) es una marca de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction \_ Repair**
</dt> <dd> <dl> <dt>

6 \| **DeviceDsmActionFlag \_ nonDestructive** (0x80000006)
</dt> <dt>



Se realiza una acción de reparación. **DeviceDsmActionFlag \_ nonDestructive** (0x80000000) es una marca de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**Limpieza de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

7 \| **DeviceDsmActionFlag \_ nonDestructive** (0x80000007)
</dt> <dt>



Se realiza una acción de limpieza. **DeviceDsmActionFlag \_ nonDestructive** (0x80000000) es una marca de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**Resistencia de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

8 \| **DeviceDsmActionFlag \_ nonDestructive** (0x80000008)
</dt> <dt>



Se realiza una acción de resistencia. **DeviceDsmActionFlag \_ nonDestructive** (0x80000000) es una marca de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                         |
| Header<br/>                   | <dl> <dt>WinIoCtl.h (incluir Windows.h)</dt> </dl> |



 

 




