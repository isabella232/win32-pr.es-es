---
description: Representa una dirección en la tabla de archivos maestros (MFT). La dirección se etiqueta con un número de secuencia reutilizado circularmente que se establece en el momento en que la referencia de segmento MFT era válida.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: MFT_SEGMENT_REFERENCE estructura
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
ms.openlocfilehash: 0ef3ad4e727465b5ceb24c1ecc785f62b747da8113b8853bffc3431604089066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827091"
---
# <a name="mft_segment_reference-structure"></a>Estructura MFT \_ SEGMENT \_ REFERENCE

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa una dirección en la tabla de archivos maestros (MFT). La dirección se etiqueta con un número de secuencia reutilizado circularmente que se establece en el momento en que la referencia de segmento MFT era válida.

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

## <a name="remarks"></a>Comentarios

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión principal 3 y la versión secundaria 0 o 1, como notifica [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

El **tipo de datos FILE \_ REFERENCE** se define de la manera siguiente.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
