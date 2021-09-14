---
description: La estructura de datos PROPERTYINFO define una propiedad del protocolo.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: Estructura PROPERTYINFO (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362136"
---
# <a name="propertyinfo-structure"></a>PROPERTYINFO (estructura)

La **estructura de datos PROPERTYINFO** define una propiedad del protocolo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**hProperty**
</dt> <dd>

Establezca este campo en cero. En la salida, Monitor de red devuelve un identificador a la propiedad después de agregar la propiedad a la base de datos de propiedades.

</dd> <dt>

**Versión**
</dt> <dd>

Reservado. Debe establecerse en cero.

</dd> <dt>

**Label**
</dt> <dd>

Nombre de la propiedad.

</dd> <dt>

**Comment**
</dt> <dd>

Descripción de la propiedad. La descripción aparece en la Monitor de red de estado.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo de datos de la propiedad. Este miembro puede tener uno de los siguientes valores.



| Value                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**PROP \_ TYPE \_ VOID**</dt> </dl>                                           | El tipo de propiedad es desconocido. No hay ninguna longitud ni formato implícitos.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**RESUMEN \_ DE TIPO \_ PROP**</dt> </dl>                                  | Resumen del tipo de propiedad. Indica la primera instancia de propiedad que el analizador asocia a un marco. PROP \_ TYPE \_ SUMMARY puede actuar como marcador de posición para grupos de propiedades. Este valor indica que la propiedad no está definida en el protocolo *RFC*.<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**BYTE \_ DE TIPO \_ PROP**</dt> </dl>                                           | Datos numéricos con un tamaño de un byte (entidad de 8 bits).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**PROP \_ TYPE \_ WORD**</dt> </dl>                                           | Datos numéricos con un tamaño de dos bytes (entidad de 16 bits).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**PROP \_ TYPE \_ DWORD**</dt> </dl>                                        | Datos numéricos con un tamaño de cuatro bytes (entidad de 32 bits).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**TIPO \_ DE PROP \_ LARGEINT**</dt> </dl>                               | Datos numéricos con un tamaño de ocho bytes (entidad de 64 bits).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**ADDR \_ DE TIPO \_ PROP**</dt> </dl>                                           | Dirección MAC (entidad de 6 bytes).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**PROP \_ TYPE \_ TIME**</dt> </dl>                                           | **Estructura SYSTEMTIME.**<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**PROP \_ TYPE \_ STRING**</dt> </dl>                                     | Datos de texto ASCII. Este tipo de datos no termina en NULL. <br/> En el caso de los datos Unicode, cuando se especifican datos de texto ASCII, también se debe establecer la marca UNICODE IFLAG cuando se llama a la función de instancia \_ de la propiedad attach.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**DIRECCIÓN \_ IP DE TIPO \_ PROP \_**</dt> </dl>                        | Dirección IP. (entidad de 4 bytes).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**DIRECCIÓN \_ \_ IPX DE TIPO PROP \_**</dt> </dl>                     | Dirección IPX. (entidad de 10 bytes).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**PALABRA \_ \_ BYTESWAPPED DE TIPO \_ PROP**</dt> </dl>      | Obsoleto. Para los datos word intercambiados por bytes, establezca **DataType** en PROP TYPE WORD y establezca la marca IFLAG SWAPPED al llamar a una \_ función de instancia de propiedad \_ \_ **Attach.**<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**DWORD \_ \_ DE TIPO PROP \_ BYTESWAPPED**</dt> </dl>   | Obsoleto. Para los datos DWORD intercambiados por bytes, establezca **DataType** en PROP TYPE DWORD y establezca la marca IFLAG SWAPPED al llamar a una función de instancia de \_ \_ propiedad \_ **Attach.**<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**PROP \_ TYPE \_ TYPED \_ STRING**</dt> </dl>                  | Obsoleto. Para los datos de cadena de tipo variable, establezca **DataType** en PROP TYPE STRING y establezca la marca UNICODE IFLAG al llamar \_ a una función de instancia de propiedad \_ \_ **Attach.**<br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**DATOS SIN \_ \_ PROCESAR DE TIPO \_ PROP**</dt> </dl>                              | Datos sin procesar de longitud y formato desconocidos.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**COMENTARIO \_ DE TIPO \_ PROP**</dt> </dl>                                  | Igual que PROP \_ TYPE \_ VOID.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**PROP \_ TYPE \_ SRCFRIENDLYNAME**</dt> </dl>          | Dirección del nombre descriptivo del origen. Monitor de red no proporciona compatibilidad de formato integrada para este tipo de datos.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**PROP \_ TYPE \_ DSTFRIENDLYNAME**</dt> </dl>          | Dirección del nombre descriptivo de destino. Monitor de red no proporciona compatibilidad de formato integrada para este tipo de datos.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**DIRECCIÓN \_ \_ TOKENRING DE TIPO \_ PROP**</dt> </dl>   | Dirección de anillo de token. Monitor de red no proporciona compatibilidad de formato integrada para este tipo de datos.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**DIRECCIÓN \_ \_ FDDI DE TIPO \_ PROP**</dt> </dl>                  | Dirección FDDI. Monitor de red no proporciona compatibilidad de formato integrada para este tipo de datos.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**DIRECCIÓN \_ \_ ETHERNET DE TIPO \_ PROP**</dt> </dl>      | Dirección Ethernet. Monitor de red no proporciona compatibilidad de formato integrada para este tipo de datos.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**IDENTIFICADOR DE \_ OBJETO \_ DE TIPO \_ PROP**</dt> </dl>   | Identificador de objeto SNMP codificado en BER.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**DIRECCIÓN \_ \_ IP DEL TIPO PROP PARA LA \_ \_ PROPIEDAD**</dt> </dl>     | Dirección IP de Parras (entidad de 6 bytes).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**PROP \_ TYPE \_ VAR \_ LEN \_ SMALL \_ INT**</dt> </dl> | Valor numérico sin una longitud determinada previamente, pero no más de 8 bytes de longitud. La longitud de los datos adjuntos determina la longitud del valor.<br/>                                                                                                                                                |



 

</dd> <dt>

**DataQualifier**
</dt> <dd>

Calificador de datos de una propiedad. Este miembro proporciona información precisa sobre el tipo de datos.

**DataQualifier** puede tener uno de los siguientes valores.



| Value                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**PROP \_ QUAL \_ NONE**</dt> </dl>                                      | El tipo de datos de propiedad es la única especificación de la propiedad. <br/> Cuando se establece este valor, el miembro de unión de la estructura se establece en **NULL** y, a continuación, se omite.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**PROP \_ QUAL \_ RANGE**</dt> </dl>                                   | Se espera que el valor numérico esté dentro de un intervalo determinado. Defina el intervalo en el **miembro lpRange.**<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**PROP \_ QUAL \_ SET**</dt> </dl>                                         | El valor de una propiedad se compara con un conjunto de valores que se especifican en el **miembro lpSet** de la unión de la estructura. El valor de una propiedad puede ser **BYTE,** **WORD,** **DWORD,** **LARGEINT** o **TIME.**<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**CAMPO DE \_ BITS DE PROP QUAL \_**</dt> </dl>                          | Obsoleto.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**PROP \_ QUAL \_ LABELED \_ SET**</dt> </dl>                | El valor de una propiedad se compara con un valor de un conjunto de pares de etiquetas de valor. Los pares de etiquetas de valor se especifican en el **miembro lpSet** de la unión de la estructura. <br/> En el momento de la presentación, si el valor de la propiedad coincide con un valor del conjunto, se muestran tanto un valor como la etiqueta asociada.<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**CAMPO \_ DE BITS CON LA ETIQUETA \_ PROP QUAL \_**</dt> </dl> | Obsoleto. Use PROP \_ QUAL \_ FLAGS en su lugar.<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**PROP \_ QUAL \_ CONST**</dt> </dl>                                   | El valor de una propiedad se compara con una constante especificada en el **miembro Value** de la unión. <br/> En el momento de la presentación, si los valores de propiedad y la constante no coinciden, aparece un mensaje de error con formato con el valor establecido como Normal.<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**MARCAS \_ DE PROP QUAL \_**</dt> </dl>                                   | El valor de la propiedad se compara con los BIT específicos identificados en el **miembro lpSet** de la unión.<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**PROP \_ QUAL \_ ARRAY**</dt> </dl>                                   | El valor de una propiedad especifica una matriz de valores. La longitud de los datos adjuntos determina la longitud de una matriz. <br/> Cuando se establece el valor PROP QUAL ARRAY, el miembro de unión de la estructura de datos PROPERTYINFO se \_ \_ establece en **NULL** y se omite. <br/>                                                    |



 

</dd> <dt>

**lpExtendedInfo**
</dt> <dd>

Reservado (miembro de unión).

</dd> <dt>

**lpRange**
</dt> <dd>

Puntero a una [estructura RANGE](range.md) que define un intervalo de valores. Este miembro debe establecerse si el **miembro DataQualifier** de esta estructura está establecido en PROP \_ QUAL RANGE \_ (miembro de unión).

</dd> <dt>

**lpSet**
</dt> <dd>

Puntero a una [estructura SET](set.md) que especifica un conjunto de valores o etiquetas. Este miembro debe establecerse si el **miembro DataQualifier** de la estructura se establece en PROP \_ QUAL SET, PROP QUAL LABELED SET o PROP QUAL \_ \_ \_ \_ \_ \_ FLAGS (miembro de unión).

</dd> <dt>

**Máscara**
</dt> <dd>

Obsoleto (miembro de unión).

</dd> <dt>

**Valor**
</dt> <dd>

Valor constante utilizado cuando **DataQualifier** se establece en PROP \_ QUAL \_ CONST (miembro de unión).

</dd> <dt>

**FormatStringSize**
</dt> <dd>

Tamaño máximo usado solo para la descripción de la propiedad.

</dd> <dt>

**InstanceData**
</dt> <dd>

Especifique la función de formato a la que se llama para dar formato a los datos mostrados para la propiedad . Para usar el formateador genérico, especifique la **función FormatPropertyInstance.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **estructura PROPERTYINFO** se usa en las llamadas a [la función AddProperty.](/previous-versions/bb251873(v=msdn.10)) La **función AddProperty** agrega una definición de propiedad única a la base de datos de propiedades [*del analizador.*](p.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[GAMA](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

