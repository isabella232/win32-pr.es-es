---
description: Tipos de partición válidos usados por los controladores de disco.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Tipos de partición de disco (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668373"
---
# <a name="disk-partition-types"></a>Tipos de partición de disco

En la tabla siguiente se identifican los tipos de partición válidos que usan los controladores de disco.



| Constante o valor                                                                                                                                                                                                                                      | Descripción                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <dt>**Partición \_ de ENTRADA \_ no utilizada**</dt> <dt>0x00</dt> </dl> | Una partición de entrada sin usar.<br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <dt>**Partición \_ de 0x05 EXTENDIda**</dt> <dt></dt> </dl>              | Una partición extendida.<br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <dt>**Partición \_ de FAT \_ 12**</dt> <dt>0x01</dt> </dl>                   | Una partición del sistema de archivos FAT12.<br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <dt>**Partición \_ de FAT \_ 16**</dt> <dt>0x04</dt> </dl>                   | Una partición del sistema de archivos FAT16.<br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <dt>**Partición \_ de FAT32**</dt> <dt>0x0B</dt> </dl>                       | Una partición del sistema de archivos FAT32.<br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <dt>**Partición \_ de**</dt> <dt>0X07</dt> de IFS </dl>                             | Una partición IFS.<br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <dt>**Partición \_ de LDM**</dt> <dt>0x42</dt> </dl>                             | Una partición del administrador de discos lógicos (LDM).<br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <dt>**Partición \_ de NTFT**</dt> <dt>0x80</dt> </dl>                          | Una partición NTFT.<br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <dt>**Válido \_ NTFT**</dt> <dt>0xC0</dt> </dl>                                      | Una partición NTFT válida.<br/> El bit alto de un código de tipo de partición indica que una partición forma parte de un reflejo de NTFT o una matriz seccionada.<br/> |



## <a name="remarks"></a>Observaciones

Hay varias macros que pueden ayudarle a detectar el tipo de partición: **IsContainerPartition**, **IsFTPartition** y **IsRecognizedPartition**. Para obtener más información, vea WinIoCtl. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>WinIoCtl. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de partición \_ \_ ex**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[**\_MBR de información de partición \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[**ESTABLECER \_ información de partición \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




