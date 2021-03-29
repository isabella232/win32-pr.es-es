---
description: Representa un atributo de nombre de archivo. Un archivo tiene un atributo de nombre de archivo para cada directorio en el que se escribe.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Estructura de FILE_NAME
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
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080093"
---
# <a name="file_name-structure"></a>Estructura de nombre de archivo \_

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa un atributo de nombre de archivo. Un archivo tiene un atributo de nombre de archivo para cada directorio en el que se escribe.

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

Referencia de archivo al directorio que indexa este nombre. Consulte [**\_ \_ referencia de segmento de MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**FileNameLength**
</dt> <dd>

La longitud del nombre de archivo, en caracteres Unicode.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas de nombre de archivo.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**Archivo \_ de NOMBRE \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**Archivo \_ de NAME \_ dos** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

Primer carácter del nombre de archivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
