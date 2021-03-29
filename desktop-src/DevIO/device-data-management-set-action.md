---
description: Defina el conjunto de acciones para el \_ código de \_ control administrar atributos del conjunto de datos de almacenamiento de ioctl \_ \_ \_ .
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907218"
---
# <a name="device_data_management_set_action"></a>\_acción de \_ conjunto de administración de datos de dispositivo \_ \_

Los siguientes valores constantes son el conjunto de valores posibles para el tipo de **\_ \_ \_ \_ acción set de administración de datos del dispositivo** , que se define como tipo **DWORD**.

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ ninguno**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



No se realiza ninguna acción.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Se realiza una acción de recorte.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**\_Notificación DeviceDsmAction**
</dt> <dd> <dl> <dt>

2 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000002)
</dt> <dt>



Se realiza una acción de notificación. Los parámetros se encuentran en una estructura de [**parámetros de notificación de DSM del dispositivo \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) . La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**
</dt> <dd> <dl> <dt>

3 \| **DeviceDsmActionFlag no \_ destructivo** (0x80000003)
</dt> <dt>



Se realiza una acción de lectura de descarga. Los parámetros se encuentran en una estructura [**DSM de dispositivo \_ \_ Descargar \_ \_ parámetros de lectura**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) . La salida está en una estructura de [**salida de lectura de descarga de almacenamiento \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) . La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Se realiza una acción de escritura de descarga. Los parámetros se encuentran en una estructura de [**\_ \_ \_ \_ parámetros de escritura del DSM de dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) . La salida está en una estructura de [**salida de escritura de descarga de almacenamiento \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Asignación de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

5 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000005)
</dt> <dt>



Se devuelve un mapa de bits de asignación para el primer intervalo de conjunto de datos pasado. La salida se encuentra en un conjunto de datos de dispositivo estructura de [**\_ \_ \_ \_ \_ Estado de aprovisionamiento lb**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) . La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**Reparación de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

6 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000006)
</dt> <dt>



Se realiza una acción de reparación. La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**\_Limpieza DeviceDsmAction**
</dt> <dd> <dl> <dt>

7 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000007)
</dt> <dt>



Se realiza una acción de limpieza. La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**Resistencia de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

8 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000008)
</dt> <dt>



Se realiza una acción de resistencia. La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.

**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                         |
| Encabezado<br/>                   | <dl> <dt>WinIoCtl. h (incluir Windows. h)</dt> </dl> |



 

 




