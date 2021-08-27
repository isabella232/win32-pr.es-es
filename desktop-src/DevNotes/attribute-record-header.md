---
description: Representa un registro de atributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: ATTRIBUTE_RECORD_HEADER estructura
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
ms.openlocfilehash: 9664af36448bb125dc8d5fde3c4d22b04e58b1ca341acad561b94708acbf143c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045395"
---
# <a name="attribute_record_header-structure"></a>ESTRUCTURA ATTRIBUTE \_ RECORD \_ HEADER

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
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_ Información**</dt> <dt>0x10</dt> </dl> | Atributos de archivo (como solo lectura y archivo), marcas de tiempo (como la creación de archivos y la última modificación) y el recuento de vínculos duros.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_ List**</dt> <dt>0x20</dt> </dl>                   | Lista de atributos que forma el archivo y la referencia de archivo del registro de archivo MFT en el que se encuentra cada atributo.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_ Nombre**</dt> <dt>0x30</dt> </dl>                                  | Nombre del archivo, en caracteres Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_ Identificador**</dt> <dt>0x40</dt> </dl>                                  | Identificador de objeto de 64 bytes asignado por el servicio de seguimiento de vínculos.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$VOLUME \_ Nombre**</dt> <dt>0x60</dt> </dl>                            | Etiqueta de volumen. Presente en el $Volume archivo.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$VOLUME \_ Información**</dt> <dt>0x70</dt> </dl>       | Información del volumen. Presente en el $Volume archivo.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$DATA**</dt> <dt>0x80</dt> </dl>                                                  | Contenido del archivo.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$INDEX \_ Root**</dt> <dt>0x90</dt> </dl>                               | Se usa para implementar la asignación de nombres de archivo para directorios grandes.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$INDEX \_ Asignación**</dt> <dt>0xA0</dt> </dl>             | Se usa para implementar la asignación de nombres de archivo para directorios grandes.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$BITMAP**</dt> <dt>0xB0</dt> </dl>                                            | Índice de mapa de bits para un directorio grande.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ Point**</dt> <dt>0xC0</dt> </dl>                      | Los datos de punto de reanción.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

Tamaño del registro de atributo, en bytes. Este valor refleja el tamaño necesario para la variante de registro y siempre se redondea al límite de cuatro palabras más cercano.

</dd> <dt>

**FormCode**
</dt> <dd>

Código del formulario de atributo.



| Value                                                                                                                                                                                                                            | Significado                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**RESIDENT \_ Formulario**</dt> <dt>0x00</dt> </dl>          | El valor está contenido en el registro de archivo y sigue inmediatamente al encabezado del registro de atributo.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <dt>**NONRESIDENT \_ Formulario**</dt> <dt>0x01</dt> </dl> | El valor se encuentra en otros sectores del disco.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

Tamaño del nombre del atributo opcional, en caracteres, o 0 si no hay ningún nombre de atributo. La longitud máxima del nombre del atributo es de 255 caracteres.

</dd> <dt>

**NameOffset**
</dt> <dd>

Desplazamiento del nombre del atributo desde el inicio del registro de atributo, en bytes. Si el **miembro NameLength** es 0, este miembro no está definido.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas de atributo.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE \_ MÁSCARA \_ DE COMPRESIÓN \_ DE** MARCAS (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE \_ FLAG \_ SPARSE** (0x8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE \_ FLAG \_ ENCRYPTED** (0x4000)
</dt> </dl> </dd> <dt>

**Instancia**
</dt> <dd>

Instancia única de este atributo en el registro de archivo.

</dd> <dt>

**Forma**
</dt> <dd>

Si el **miembro FormCode** es RESIDENT \_ FORM, la unión es una **estructura Resident.** Si **FormCode** es NONRESIDENT \_ FORM, la unión es una **estructura nonresident.**

<dl> <dt>

**Residente**
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

**Nonresident**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

Número de clúster virtual (VCN) más bajo cubierto por este registro de atributo.

</dd> <dt>

**HighestVcn**
</dt> <dd>

El vcn más alto cubierto por este registro de atributo.

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

Desplazamiento a la matriz de pares de asignación desde el inicio del registro de atributo, en bytes. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**AllocatedLength**
</dt> <dd>

Tamaño asignado del archivo, en bytes. Este valor es un múltiplo par del tamaño del clúster. Este miembro no es válido si el **miembro LowestVcn** es distinto de cero.

</dd> <dt>

**FileSize**
</dt> <dd>

Tamaño del archivo (byte más alto que se puede leer más 1), en bytes. Este miembro no es válido si **LowestVcn** es distinto de cero.

</dd> <dt>

**ValidDataLength**
</dt> <dd>

Longitud de datos válida (byte inicializado más 1), en bytes. Este valor se redondea al límite del clúster más cercano. Este miembro no es válido si **LowestVcn** es distinto de cero.

</dd> <dt>

**TotalAllocated**
</dt> <dd>

El total asignado para el archivo (la suma de los clústeres asignados).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión principal 3 y la versión secundaria 0 o 1, como notifica [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Los registros de atributo siempre se alinean en un límite de cuatro palabras.

Si el atributo no es id. , el encabezado de registro de atributo contiene una lista de información de recuperación que proporciona una asignación entre VCN y el número de clúster lógico (LCN) para el atributo. Si la información de recuperación no cabe en el segmento de archivo base, se puede almacenar en un segmento de registro de archivo externo por sí mismo. Si sigue sin caber en un segmento de registro de archivo externo, hay un aprovisionamiento en la lista de atributos para contener varias entradas para un atributo que requiere información de recuperación adicional.

La matriz de pares de asignación se almacena en un formato comprimido y supone que el sistema descomprime y almacena en caché la información. Consta de una serie de pares NextVcn/CurrentLcn. Por ejemplo, si un archivo tiene una sola ejecución de 8 clústeres a partir de LCN 128 y el archivo comienza en LowestVcn 0, la matriz de pares de asignación tiene una sola entrada, que es NextVcn=8 y CurrentLcn=128. La matriz es una secuencia de bytes que almacena los cambios en las variables de trabajo cuando se procesan secuencialmente. La secuencia de bytes se interpretará como una secuencia terminada en cero de triples, como se muestra a continuación:

count byte = *v* + (*l* \* 16)

donde *v* es el número de bytes VCN de orden bajo cambiados y *l* es el número de bytes LCN de orden bajo modificados.

El algoritmo de descompresión es el siguiente:

1.  Inicialice NextVcn en `Attribute->LowestVcn` y CurrentLcn en 0.
2.  Inicialice el puntero de flujo de bytes en `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  Establezca CurrentVcn en NextVcn.
4.  Lea el byte siguiente de la secuencia. Si es 0, se interrumpirá. si no, *extraiga v* y *l* como se ha descrito anteriormente.
5.  Interprete los *bytes v* siguientes como una cantidad firmada, con el byte de orden bajo en primer lugar. Desempaquete la extensión de inicio de sesión en 64 bits y agrégala a NextVcn.
6.  Interprete los *bytes l* siguientes como una cantidad firmada, con el byte de orden bajo en primer lugar. Desempaquete la extensión de inicio de sesión en 64 bits y agrégala a CurrentLcn. Si esto genera un Valor CurrentLcn de 0, los VCN de CurrentVcn a NextVcn–1 no se asignarán.
7.  Actualice la información de asignación almacenada en caché de CurrentVcn, NextVcn y CurrentLcn.
8.  Vaya al paso 3.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
