---
description: Representa una entrada en la lista de atributos.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: ATTRIBUTE_LIST_ENTRY estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0c0154de52dbefa6d29278ca05e924db6f6c1d84b124fe21b3092e728a0d07fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956144"
---
# <a name="attribute_list_entry-structure"></a>ESTRUCTURA ATTRIBUTE \_ LIST \_ ENTRY

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa una entrada en la lista de atributos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**AttributeTypeCode**
</dt> <dd>

Código de tipo de atributo.



| Value                                                                                                                                                                                                                                           | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_ Información**</dt> <dt>0x10</dt> </dl> | Atributos de archivo (como solo lectura y archivo), marcas de tiempo (como la creación de archivos y la última modificación) y el recuento de vínculos duros.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_ List**</dt> <dt>0x20</dt> </dl>                   | Lista de atributos que son el archivo y la referencia de archivo del registro de archivo MFT en el que se encuentra cada atributo.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_ Nombre**</dt> <dt>0x30</dt> </dl>                                  | Nombre del archivo, en caracteres Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_ Identificador**</dt> <dt>0x40</dt> </dl>                                  | Identificador de objeto de 16 bytes asignado por el servicio de seguimiento de vínculos.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$VOLUME \_ Nombre**</dt> <dt>0x60</dt> </dl>                            | Etiqueta de volumen. Presente en el $Volume archivo.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$VOLUME \_ Información**</dt> <dt>0x70</dt> </dl>       | Información del volumen. Presente en el $Volume archivo.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$DATA**</dt> <dt>0x80</dt> </dl>                                                  | Contenido del archivo.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$INDEX \_ Root**</dt> <dt>0x90</dt> </dl>                               | Se usa para implementar la asignación de nombres de archivo para directorios grandes.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$INDEX \_ Asignación**</dt> <dt>0xA0</dt> </dl>             | Se usa para implementar la asignación de nombres de archivo para directorios grandes.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$BITMAP**</dt> <dt>0xB0</dt> </dl>                                            | Índice de mapa de bits para un directorio grande.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ Point**</dt> <dt>0xC0</dt> </dl>                      | Datos de punto de reanción.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

Tamaño de esta estructura, más el búfer de nombres opcional, en bytes.

</dd> <dt>

**AttributeNameLength**
</dt> <dd>

Tamaño del nombre del atributo opcional, en caracteres. Si existe un nombre, este valor es distinto de cero y la estructura va seguida inmediatamente de una cadena Unicode del número de caracteres especificado.

</dd> <dt>

**AttributeNameOffset**
</dt> <dd>

Reservado.

</dd> <dt>

**LowestVcn**
</dt> <dd>

Número de clúster virtual (VCN) más bajo para este atributo. Este miembro es cero a menos que el atributo requiera varios segmentos de registro de archivo y a menos que esta entrada sea una referencia a un segmento distinto del primero. En este caso, este valor es el VCN más bajo que describe el segmento al que se hace referencia.

</dd> <dt>

**SegmentReference**
</dt> <dd>

Segmento de tabla de archivos maestros (MFT) en el que reside el atributo. Consulte MFT SEGMENT REFERENCE ( REFERENCIA [**\_ DE \_ SEGMENTOS DE MFT).**](mft-segment-reference.md)

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**AttributeName**
</dt> <dd>

Inicio del nombre del atributo opcional.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La lista de atributos es una lista ordenada de estructuras **ATTRIBUTE \_ LIST \_ ENTRY** alineadas con cuatro palabras. Esta lista se ordena primero por el código de tipo de atributo y, después, por el nombre del atributo (si está presente). No hay dos atributos que puedan tener el mismo código de tipo, nombre y VCN más bajo. Por lo tanto, puede haber como máximo un atributo para cada código de tipo sin un nombre.

Esta definición de estructura solo es válida para la versión principal 3 y la versión secundaria 0 o 1, como se notifica en [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
