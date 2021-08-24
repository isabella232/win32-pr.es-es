---
description: 'Los objetos de almacenamiento se separan en tres tipos: controladores, unidades y medios.'
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: Clases de almacenamiento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c46efc17b3df5e1a509cec3565c6aaa7b65ff06d189951b100ac06d93a957e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829675"
---
# <a name="storage-classes"></a>Clases de almacenamiento

Los objetos de almacenamiento se separan en tres tipos: controladores, unidades y medios.

Hay dos controladores, un controlador IDE emulado y un controlador SCSI sintético. Ambos controladores admiten los datos adjuntos de las unidades que hospedan los medios.

Las siguientes son clases WMI de virtualización relacionadas con el almacenamiento. También se admiten disquetes sintéticos. No se admite la conexión a un disquete físico.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                      | Descripción                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AffectedStorageJobElement**](msvm-affectedstoragejobelement.md)<br/>       | Representa la asociación entre un trabajo y los elementos administrados que pueden verse afectados por su ejecución.<br/>                                                                                               |
| [**Msvm \_ BasedOn**](msvm-basedon.md)<br/>                                           | Asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento desde extensiones de nivel inferior.<br/>                                                                                                           |
| [**Msvm \_ ControlledBy**](msvm-controlledby.md)<br/>                                 | Asocia un dispositivo de almacenamiento al controlador de almacenamiento que posee el dispositivo.<br/>                                                                                                                          |
| [**Msvm \_ DiskDrive**](msvm-diskdrive.md)<br/>                                       | Representa una unidad de disco duro dentro de una máquina virtual.<br/>                                                                                                                                              |
| [**Msvm \_ DisketteController**](msvm-diskettecontroller.md)<br/>                     | Representa el disquete de la máquina virtual.<br/>                                                                                                                                               |
| [**Msvm \_ DisketteDrive**](msvm-diskettedrive.md)<br/>                               | Representa una unidad de disquete dentro de la máquina virtual.<br/>                                                                                                                                                  |
| [**Msvm \_ DVDDrive**](msvm-dvddrive.md)<br/>                                         | Representa una unidad de DVD dentro de una máquina virtual.<br/>                                                                                                                                                    |
| [**IDEController de Msvm \_**](msvm-idecontroller.md)<br/>                               | Representa un controlador IDE.<br/>                                                                                                                                                                          |
| [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)<br/>             | Administra los medios virtuales (archivos .vhd, .vhdx, .iso o .vfd) de una máquina virtual.<br/>                                                                                                                    |
| [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)<br/>                                   | Representa los medios de unidad de almacenamiento y se usa para rellenar las unidades de almacenamiento.<br/>                                                                                                                             |
| [**Msvm \_ MediaPresent**](msvm-mediapresent.md)<br/>                                 | Asocia una unidad de almacenamiento a los medios insertados en la unidad.<br/>                                                                                                                                     |
| [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md)<br/>                   | Proporciona información detallada sobre una imagen de almacenamiento montada manualmente.<br/>                                                                                                                                  |
| [**Msvm \_ ProtocolControllerForUnit**](msvm-protocolcontrollerforunit.md)<br/>       | Esta asociación indica que una subclase de dispositivo lógico (por ejemplo, un volumen de almacenamiento) está conectada a través de un controlador de protocolo específico.<br/>                                                       |
| [**Msvm \_ SCSIProtocolController**](msvm-scsiprotocolcontroller.md)<br/>             | Representa un controlador SCSI sintético.<br/>                                                                                                                                                                |
| [**StorageAlert de Msvm \_**](msvm-storagealert.md)<br/>                                 | Representa un evento que se genera cada vez que cambia la propiedad **OperationalStatus** de la clase [**\_ Msvm ResourcePool**](msvm-resourcepool.md) o [**Msvm \_ LogicalDisk.**](msvm-logicaldisk.md)<br/> |
| [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)<br/> | Representa la configuración específicamente relacionada con la asignación de almacenamiento virtual.<br/>                                                                                                                         |
| [**Msvm \_ StorageJob**](msvm-storagejob.md)<br/>                                     | Representa un trabajo de operación de almacenamiento creado por el Microsoft Hyper-V Image Management Service.<br/>                                                                                                          |
| [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)<br/>     | Proporciona datos de configuración para un disco duro virtual.<br/>                                                                                                                                                         |
| [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md)<br/>                 | Proporciona información de estado para una imagen de disco duro virtual existente.<br/>                                                                                                                                    |



 

 

 




