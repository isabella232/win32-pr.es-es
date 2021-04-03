---
description: Representa una entrada en la lista de atributos.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Estructura de ATTRIBUTE_LIST_ENTRY
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
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906966"
---
# <a name="attribute_list_entry-structure"></a>Estructura de entrada de \_ lista de atributos \_

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
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ INFORMACIÓN**</dt> <dt>0x10</dt> </dl> | Atributos de archivo (como de solo lectura y archivo), marcas de tiempo (por ejemplo, creación de archivos y última modificación) y el número de vínculos físicos.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ ENUMERAr**</dt> <dt>0x20</dt> </dl>                   | Una lista de atributos que constituyen el archivo y la referencia de archivo del registro de archivo MFT en el que se encuentra cada atributo.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ NOMBRE**</dt> <dt>0x30</dt> </dl>                                  | Nombre del archivo, en caracteres Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID.**</dt> <dt>0x40</dt> </dl>                                  | Identificador de objeto de 16 bytes asignado por el servicio de seguimiento de vínculos.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$Volume \_ NOMBRE**</dt> <dt>0x60</dt> </dl>                            | Etiqueta de volumen. Presente en el archivo de $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$Volume \_**</dt> <dt>0X70</dt> de información </dl>       | Información del volumen. Presente en el archivo de $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$Data**</dt> <dt>0x80</dt> </dl>                                                  | Contenido del archivo.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$Index \_**</dt> <dt>0x90</dt> raíz </dl>                               | Se usa para implementar la asignación de nombres de archivo para directorios grandes.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$Index \_**</dt> <dt>0XA0</dt> de asignación </dl>             | Se usa para implementar la asignación de nombres de archivo para directorios grandes.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$Bitmap**</dt> <dt>0xB0</dt> </dl>                                            | Índice de mapa de bits para un directorio grande.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ PUNTO**</dt> <dt>0xC0</dt> </dl>                      | Los datos del punto de reanálisis.<br/>                                                                                                          |



 

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

El número de clúster virtual más bajo (VCN) para este atributo. Este miembro es cero a menos que el atributo requiera varios segmentos de registro de archivos y a menos que esta entrada sea una referencia a un segmento que no sea el primero. En este caso, este valor es el VCN más bajo descrito por el segmento al que se hace referencia.

</dd> <dt>

**SegmentReference**
</dt> <dd>

El segmento de la tabla de archivos maestros (MFT) en el que reside el atributo. Consulte [**\_ \_ referencia de segmento de MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**AttributeName**
</dt> <dd>

Inicio del nombre del atributo opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La lista de atributos es una lista ordenada de estructuras de **\_ \_ entradas de lista de atributos** alineados quadword. Esta lista se ordena primero por el código de tipo de atributo y, a continuación, por el nombre del atributo (si está presente). Dos atributos no pueden tener el mismo código de tipo, nombre y VCN más bajo. Por lo tanto, puede haber como máximo un atributo para cada código de tipo sin nombre.

Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
