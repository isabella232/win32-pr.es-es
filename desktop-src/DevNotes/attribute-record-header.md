---
description: Representa un registro de atributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Estructura de ATTRIBUTE_RECORD_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906965"
---
# <a name="attribute_record_header-structure"></a>Estructura del encabezado del \_ registro de atributos \_

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa un registro de atributo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**TypeCode**
</dt> <dd>

Código de tipo de atributo.



| Value                                                                                                                                                                                                                                           | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ INFORMACIÓN**</dt> <dt>0x10</dt> </dl> | Atributos de archivo (como de solo lectura y archivo), marcas de tiempo (por ejemplo, creación de archivos y última modificación) y el número de vínculos físicos.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ ENUMERAr**</dt> <dt>0x20</dt> </dl>                   | Una lista de atributos que constituyen el archivo y la referencia de archivo del registro de archivo MFT en el que se encuentra cada atributo.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ NOMBRE**</dt> <dt>0x30</dt> </dl>                                  | Nombre del archivo, en caracteres Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID.**</dt> <dt>0x40</dt> </dl>                                  | Identificador de objeto de 64 bytes asignado por el servicio de seguimiento de vínculos.<br/>                                                              |
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

Tamaño del registro de atributo, en bytes. Este valor refleja el tamaño necesario para la variante de registro y siempre se redondea al límite de quadword más próximo.

</dd> <dt>

**FormCode**
</dt> <dd>

Código del formulario de atributo.



| Value                                                                                                                                                                                                                            | Significado                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**Residente \_ de FORMULARIO**</dt> <dt>0x00</dt> </dl>          | El valor se encuentra en el registro de archivo y sigue inmediatamente al encabezado del registro de atributo.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> No <dt>**residente \_ FORMULARIO**</dt> <dt>0x01</dt> </dl> | El valor está contenido en otros sectores del disco.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

Tamaño del nombre del atributo opcional, en caracteres, o 0 si no hay ningún nombre de atributo. La longitud máxima del nombre del atributo es de 255 caracteres.

</dd> <dt>

**NameOffset**
</dt> <dd>

Desplazamiento del nombre del atributo desde el inicio del registro del atributo, en bytes. Si el miembro **NameLength** es 0, este miembro es indefinido.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas de atributo.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Atributo \_ de \_ \_ Máscara de compresión de marca** (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Atributo \_ de MARCA \_ Sparse** (0x8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Atributo \_ de MARCA \_ cifrada** (0x4000)
</dt> </dl> </dd> <dt>

**Instancia**
</dt> <dd>

Instancia única para este atributo en el registro de archivo.

</dd> <dt>

**Forma**
</dt> <dd>

Si el miembro **FormCode** es \_ un formulario residente, la Unión es una estructura **residente** . Si **FormCode** es \_ un formulario no residente, la Unión es una estructura no **residente** .

<dl> <dt>

**LaserPrep**
</dt> <dd> <dl> <dt>

**ValueLength**
</dt> <dd>

Tamaño del valor del atributo, en bytes.

</dd> <dt>

**ValueOffset**
</dt> <dd>

Desplazamiento al valor desde el inicio del registro de atributo, en bytes.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

**No residente**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

El número de clúster virtual más bajo (VCN) incluido en este registro de atributo.

</dd> <dt>

**HighestVcn**
</dt> <dd>

El valor VCN más alto incluido en este registro de atributo.

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

El desplazamiento a la asignación empareja la matriz desde el inicio del registro del atributo, en bytes. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**AllocatedLength**
</dt> <dd>

Tamaño asignado del archivo, en bytes. Este valor es un múltiplo par del tamaño del clúster. Este miembro no es válido si el miembro **LowestVcn** es distinto de cero.

</dd> <dt>

**FileSize**
</dt> <dd>

Tamaño del archivo (byte más alto que se puede leer más 1), en bytes. Este miembro no es válido si **LowestVcn** es distinto de cero.

</dd> <dt>

**ValidDataLength**
</dt> <dd>

La longitud de datos válida (byte inicializado más alto más 1), en bytes. Este valor se redondea al límite del clúster más próximo. Este miembro no es válido si **LowestVcn** es distinto de cero.

</dd> <dt>

**TotalAllocated**
</dt> <dd>

El total asignado para el archivo (la suma de los clústeres asignados).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Los registros de atributos siempre están alineados en un límite quadword.

Si el atributo no es residente, el encabezado del registro de atributo contiene una lista de información de recuperación que proporciona una asignación entre VCN y el número de clúster lógico (LCN) para el atributo. Si la información de recuperación no cabe en el segmento de archivo base, puede almacenarse en un segmento de registro de archivo externo. Si todavía no cabe en un segmento de registro de archivo externo, hay una disposición en la lista de atributos para que contenga varias entradas para un atributo que requiera información de recuperación adicional.

La matriz de pares de asignación se almacena en un formato comprimido y presupone que el sistema descomprime y almacena en caché la información. Consta de una serie de pares NextVcn/CurrentLcn. Por ejemplo, si un archivo tiene una sola ejecución de 8 clústeres a partir de LCN 128 y el archivo se inicia en LowestVcn 0, la matriz de pares de asignación tiene una sola entrada, que es NextVcn = 8 y CurrentLcn = 128. La matriz es una secuencia de bytes que almacena los cambios en las variables de trabajo cuando se procesa secuencialmente. El flujo de bytes se va a interpretar como una secuencia terminada en cero de triples, como se indica a continuación:

recuento de bytes = *v* + (*l* \* 16)

donde *v* es el número de bytes de VCN de orden inferior modificados y *l* es el número de bytes de LCN de orden inferior modificados.

El algoritmo de descompresión es el siguiente:

1.  Inicialice NextVcn en `Attribute->LowestVcn` y CurrentLcn en 0.
2.  Inicialice el puntero de secuencia de bytes a `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  Establezca CurrentVcn en NextVcn.
4.  Lee el siguiente byte de la secuencia. Si es 0, interrumpa; en caso contrario, extraiga *v* y *l* como se ha descrito anteriormente.
5.  Interprete los siguientes *v* bytes como una cantidad firmada, con el byte de orden inferior en primer lugar. Desempaquete Sign-Extended en 64 bits y agréguelo a NextVcn.
6.  Interprete los siguientes bytes de *l* como una cantidad firmada, con el byte de orden inferior en primer lugar. Desempaquete Sign-Extended en 64 bits y agréguelo a CurrentLcn. Si esto produce un CurrentLcn de 0, el valor de VCNs de CurrentVcn a NextVcn-1 no está asignado.
7.  Actualice la información de asignación almacenada en caché desde CurrentVcn, NextVcn y CurrentLcn.
8.  Vaya al paso 3.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
