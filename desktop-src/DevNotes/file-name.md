---
description: Representa un atributo de nombre de archivo. Un archivo tiene un atributo de nombre de archivo para cada directorio en el que se especifica.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: FILE_NAME estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9b09b9c58228c9028a5ac9d26d834bdc21a5c02201338767af84dc713bc3aa60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076149"
---
# <a name="file_name-structure"></a>FILE \_ NAME (estructura)

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa un atributo de nombre de archivo. Un archivo tiene un atributo de nombre de archivo para cada directorio en el que se especifica.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ParentDirectory**
</dt> <dd>

Referencia de archivo al directorio que indexa con este nombre. Vea MFT SEGMENT REFERENCE ( [**REFERENCIA DE SEGMENTO DE \_ \_ MFT).**](mft-segment-reference.md)

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**FileNameLength**
</dt> <dd>

Longitud del nombre de archivo, en caracteres Unicode.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas de nombre de archivo.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE \_ NAME \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE \_ NAME \_ DOS** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

Primer carácter del nombre de archivo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión principal 3 y la versión secundaria 0 o 1, como notifica [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
