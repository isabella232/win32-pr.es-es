---
description: Representa una dirección en la tabla de archivos maestros (MFT). La dirección se etiqueta con un número de secuencia reutilizado circularmente que se establece en el momento en que la referencia del segmento MFT era válida.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Estructura de MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152710"
---
# <a name="mft_segment_reference-structure"></a>Estructura de referencia de \_ segmento MFT \_

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa una dirección en la tabla de archivos maestros (MFT). La dirección se etiqueta con un número de secuencia reutilizado circularmente que se establece en el momento en que la referencia del segmento MFT era válida.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**SegmentNumberLowPart**
</dt> <dd>

Parte baja del número de segmento.

</dd> <dt>

**SegmentNumberHighPart**
</dt> <dd>

Parte alta del número de segmento.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Número de secuencia distinto de cero. El valor 0 está reservado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

El tipo de datos de **\_ referencia de archivo** se define como se indica a continuación.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
