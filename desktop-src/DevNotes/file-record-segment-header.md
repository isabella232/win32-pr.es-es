---
description: Representa el segmento de registro de archivo. Este es el encabezado de cada segmento de registro de archivo de la tabla de archivos maestra (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Estructura de FILE_RECORD_SEGMENT_HEADER
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
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274847"
---
# <a name="file_record_segment_header-structure"></a>\_Estructura de \_ encabezado de segmento de registro de archivo \_

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa el segmento de registro de archivo. Este es el encabezado de cada segmento de registro de archivo de la tabla de archivos maestra (MFT).

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

Encabezado de multisector definido por el administrador de caché. La estructura de [**\_ \_ encabezado de varios sectores**](multi-sector-header.md) siempre contiene la firma "archivo" y una descripción de la ubicación y el tamaño de la matriz de la secuencia de actualización.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reservado.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

El número de secuencia global. Este valor se incrementa cada vez que se libera un segmento de registro de archivo; es 0 si no se utiliza el segmento. El campo **SequenceNumber** de una referencia de archivo debe coincidir con el contenido de este campo; Si no coinciden, la referencia de archivo es incorrecta y probablemente está obsoleta.

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

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**Archivo \_ de \_Segmento \_ de registro en \_ uso** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**Archivo \_ de Índice de nombre de archivo \_ \_ \_ presente** (0x0002)
</dt> </dl> </dd> <dt>

**Reserved3**
</dt> <dd>

Reservado.

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

Referencia de archivo al segmento de registro de archivo base para este archivo. Si este es el registro del archivo base, el valor es 0. Consulte [**\_ \_ referencia de segmento de MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved4**
</dt> <dd>

Reservado.

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

La matriz de secuencias de actualización para proteger las transferencias multisector del segmento de registro de archivos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
