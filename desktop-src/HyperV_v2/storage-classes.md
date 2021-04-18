---
description: 'Los objetos de almacenamiento se dividen en tres tipos: Controladores, unidades y elementos multimedia.'
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: Clases de almacenamiento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c17ad2530a86e7f404fe19eaeb3ef5a1cd7895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688358"
---
# <a name="storage-classes"></a>Clases de almacenamiento

Los objetos de almacenamiento se dividen en tres tipos: Controladores, unidades y elementos multimedia.

Hay dos controladores, un controlador IDE emulado y un controlador SCSI sintético. Ambos controladores admiten la conexión de unidades que hospedan los medios.

A continuación se enumeran las clases WMI de virtualización relacionadas con el almacenamiento. También hay compatibilidad con los medios de disquete sintético. No se admite la conexión a una unidad de disquete física.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                      | Descripción                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ AffectedStorageJobElement**](msvm-affectedstoragejobelement.md)<br/>       | Representa la asociación entre un trabajo y los elementos administrados que pueden verse afectados por su ejecución.<br/>                                                                                               |
| [**\_BasedOn MSVM**](msvm-basedon.md)<br/>                                           | Asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior.<br/>                                                                                                           |
| [**MSVM \_ ControlledBy**](msvm-controlledby.md)<br/>                                 | Asocia un dispositivo de almacenamiento con el controlador de almacenamiento que posee el dispositivo.<br/>                                                                                                                          |
| [**MSVM \_ DiskDrive**](msvm-diskdrive.md)<br/>                                       | Representa una unidad de disco duro dentro de una máquina virtual.<br/>                                                                                                                                              |
| [**MSVM \_ DisketteController**](msvm-diskettecontroller.md)<br/>                     | Representa el controlador de disquete en la máquina virtual.<br/>                                                                                                                                               |
| [**MSVM \_ DisketteDrive**](msvm-diskettedrive.md)<br/>                               | Representa una unidad de disquete dentro de la máquina virtual.<br/>                                                                                                                                                  |
| [**MSVM \_ DVDDrive**](msvm-dvddrive.md)<br/>                                         | Representa una unidad de DVD dentro de una máquina virtual.<br/>                                                                                                                                                    |
| [**MSVM \_ IDEController**](msvm-idecontroller.md)<br/>                               | Representa una controladora IDE.<br/>                                                                                                                                                                          |
| [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)<br/>             | Administra los medios virtuales (archivos. vhd,. vhdx,. ISO o. VFD) para una máquina virtual.<br/>                                                                                                                    |
| [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md)<br/>                                   | Representa medios de unidad de almacenamiento y se usa para rellenar las unidades de almacenamiento.<br/>                                                                                                                             |
| [**MSVM \_ MediaPresent**](msvm-mediapresent.md)<br/>                                 | Asocia una unidad de almacenamiento con el medio insertado en la unidad.<br/>                                                                                                                                     |
| [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md)<br/>                   | Proporciona información detallada acerca de una imagen de almacenamiento montada manualmente.<br/>                                                                                                                                  |
| [**MSVM \_ ProtocolControllerForUnit**](msvm-protocolcontrollerforunit.md)<br/>       | Esta asociación indica que una subclase del dispositivo lógico (por ejemplo, un volumen de almacenamiento) está conectada a través de un controlador de protocolo específico.<br/>                                                       |
| [**MSVM \_ SCSIProtocolController**](msvm-scsiprotocolcontroller.md)<br/>             | Representa una controladora SCSI sintética.<br/>                                                                                                                                                                |
| [**MSVM \_ StorageAlert**](msvm-storagealert.md)<br/>                                 | Representa un evento que se genera cada vez que cambia la propiedad **OperationalStatus** de la clase [**MSVM \_ ResourcePool**](msvm-resourcepool.md) o [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) .<br/> |
| [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)<br/> | Representa la configuración relacionada específicamente con la asignación de almacenamiento virtual.<br/>                                                                                                                         |
| [**MSVM \_ StorageJob**](msvm-storagejob.md)<br/>                                     | Representa un trabajo de operación de almacenamiento creado por el servicio de administración de imágenes de Hyper-V de Microsoft.<br/>                                                                                                          |
| [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)<br/>     | Proporciona datos de configuración para un disco duro virtual.<br/>                                                                                                                                                         |
| [**MSVM \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md)<br/>                 | Proporciona información de estado de una imagen de disco duro virtual existente.<br/>                                                                                                                                    |



 

 

 




