---
description: Representa el segmento de registro de archivo. Este es el encabezado de cada segmento de registro de archivo de la tabla de archivos maestros (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: FILE_RECORD_SEGMENT_HEADER estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0c9d7a3653ad965141e691546866f599d8615f5f12feb92fa25c861d7c429b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260605"
---
# <a name="file_record_segment_header-structure"></a>FILE RECORD SEGMENT HEADER (Estructura DE \_ \_ \_ ENCABEZADO)

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa el segmento de registro de archivo. Este es el encabezado de cada segmento de registro de archivo de la tabla de archivos maestros (MFT).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**MultiSectorHeader**
</dt> <dd>

Encabezado multisector definido por el administrador de caché. La [**estructura MULTI SECTOR \_ \_ HEADER**](multi-sector-header.md) siempre contiene la firma "FILE" y una descripción de la ubicación y el tamaño de la matriz de secuencia de actualización.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reservado.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

El número de secuencia global. Este valor se incrementa cada vez que se libera un segmento de registro de archivo; es 0 si no se usa el segmento. El **campo SequenceNumber** de una referencia de archivo debe coincidir con el contenido de este campo; Si no coinciden, la referencia de archivo es incorrecta y probablemente obsoleta.

</dd> <dt>

**Reserved2**
</dt> <dd>

Reservado.

</dd> <dt>

**FirstAttributeOffset**
</dt> <dd>

Desplazamiento del primer registro de atributo, en bytes.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas de archivo.

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE \_ SEGMENTO \_ DE REGISTRO EN \_ \_ USO** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE \_ ÍNDICE \_ DE NOMBRE DE ARCHIVO \_ \_ PRESENTE** (0x0002)
</dt> </dl> </dd> <dt>

**Reserved3**
</dt> <dd>

Reservado.

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

Referencia de archivo al segmento de registro de archivo base para este archivo. Si este es el registro de archivo base, el valor es 0. Vea MFT SEGMENT REFERENCE ( [**REFERENCIA DE SEGMENTO DE \_ \_ MFT).**](mft-segment-reference.md)

</dd> <dt>

**Reserved4**
</dt> <dd>

Reservado.

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

Matriz de secuencia de actualización para proteger las transferencias multisector del segmento de registro de archivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión principal 3 y la versión secundaria 0 o 1, como notifica [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
