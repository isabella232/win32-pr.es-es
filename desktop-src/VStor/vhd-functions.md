---
description: 'Más información sobre: <span id=vhd.vhd_functions></span> Funciones de disco virtual'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Funciones de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32133e3afa8402de8483a68eb4957b261b46e556
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477221"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Funciones de disco virtual

Las siguientes funciones se usan en discos virtuales:

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>En esta sección


| Tema | Descripción | 
|-------|-------------|
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></p> | <p>Aplica una instantánea del disco virtual actual para los archivos de conjunto de VHD.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></p> | <p>Asocia un elemento primario a un disco virtual abierto con la <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> principal.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></p> | <p>Conecta un disco duro virtual (VHD) o un archivo de imagen de CD o DVD (ISO) mediante la localización de un proveedor de VHD adecuado para realizar los datos adjuntos.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></p> | <p>Interrumpe una operación reflejada iniciada previamente y establece que el reflejo sea el disco virtual activo.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></p> | <p>Reduce el tamaño de un archivo de almacenamiento de respaldo de disco duro virtual (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></p> | <p>Crea un archivo de imagen de disco duro virtual (VHD), ya sea mediante parámetros predeterminados o mediante un disco virtual existente o un disco físico.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></p> | <p>Elimina una instantánea de un archivo de conjunto de VHD.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></p> | <p>Elimina los metadatos de un disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></p> | <p>Separa un disco duro virtual (VHD) o un archivo de imagen de CD o DVD (ISO) mediante la búsqueda de un proveedor de discos virtuales adecuado para realizar la operación.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></p> | <p>Enumera los metadatos asociados a un disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></p> | <p>Aumenta el tamaño de un disco duro virtual (VHD) fijo o ampliable dinámicamente.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></p> | <p>Devuelve las relaciones entre los discos duros virtuales (VHD) o el archivo de imagen de CD o DVD (ISO) o los volúmenes contenidos en esos discos y su disco o volumen primario.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></p> | <p>Recupera información sobre un disco duro virtual.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></p> | <p>Recupera los metadatos especificados del disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></p> | <p>Comprueba el progreso de una operación asincrónica de disco duro virtual (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></p> | <p>Recupera la ruta de acceso al objeto de dispositivo físico que contiene un disco duro virtual (VHD) o un archivo de imagen de CD o DVD (ISO).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></p> | <p>Combina un disco duro virtual (VHD) secundario en una cadena de diferenciación con uno o varios discos virtuales primarios de la cadena.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></p> | <p>Inicia una operación reflejada para un disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></p> | <p>Modifica el contenido interno de un archivo de disco virtual. Se puede usar para establecer la hoja activa o para corregir las entradas de instantánea.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></p> | <p>Abre un disco duro virtual (VHD) o un archivo de imagen de CD o DVD (ISO) para su uso.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></p> | <p>Recupera información sobre los cambios en las áreas especificadas de un disco duro virtual (VHD) al que realiza el seguimiento de cambios resistentes (RCT).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></p> | <p>Emite una solicitud SCSI incrustada directamente a un disco duro virtual.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></p> | <p>Cambia el tamaño de un disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></p> | <p>Establece información sobre un disco duro virtual (VHD).</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></p> | <p>Establece un elemento de metadatos para un disco virtual.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></p> | <p>Crea una instantánea del disco virtual actual para los archivos de conjunto de VHD.</p> | 


 

 

 
