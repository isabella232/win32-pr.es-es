---
description: La estructura de datos PROPERTYINFO define una propiedad del protocolo.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: PROPERTYINFO (estructura) (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001702"
---
# <a name="propertyinfo-structure"></a>PROPERTYINFO (estructura)

La estructura de datos **PROPERTYINFO** define una propiedad del protocolo.

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



## <a name="members"></a>Miembros

<dl> <dt>

**hProperty**
</dt> <dd>

Establezca este campo en cero. En la salida, Monitor de red devuelve un identificador a la propiedad después de que la propiedad se agregue a la base de datos de propiedades.

</dd> <dt>

**Versión**
</dt> <dd>

Reservado. Debe establecerse en cero.

</dd> <dt>

**Label**
</dt> <dd>

Nombre de la propiedad.

</dd> <dt>

**Comentario**
</dt> <dd>

Descripción de la propiedad. La descripción aparece en la barra de estado de Monitor de red.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo de datos de la propiedad. Este miembro puede tener uno de los valores siguientes.



| Value                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**PROP \_ Type \_ void**</dt> </dl>                                           | No se conoce el tipo de propiedad. No hay ninguna longitud o formato implícito.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**\_Resumen de tipo de prop \_**</dt> </dl>                                  | Resumen del tipo de propiedad. Indica la primera instancia de la propiedad que el analizador asocia a un marco. \_ \_ El Resumen de tipo prop puede servir como marcador de posición para los grupos de propiedades. Este valor indica que la propiedad no está definida en el *RFC* del protocolo.<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**tipo de PROP \_ \_ byte**</dt> </dl>                                           | Datos numéricos con un tamaño de un byte (entidad de 8 bits).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**PROP ( \_ tipo de \_ palabra)**</dt> </dl>                                           | Datos numéricos con un tamaño de dos bytes (entidad de 16 bits).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**PROP ( \_ tipo \_ DWORD)**</dt> </dl>                                        | Datos numéricos con un tamaño de cuatro bytes (entidad de 32 bits).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**PROP \_ Type \_ LARGEINT**</dt> </dl>                               | Datos numéricos con un tamaño de ocho bytes (entidad de 64 bits).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**PROP \_ Type \_ addr**</dt> </dl>                                           | Dirección MAC (entidad de 6 bytes).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**\_hora del tipo de prop \_**</dt> </dl>                                           | **SYSTEMTIME** (estructura).<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**PROP \_ Type ( \_ cadena)**</dt> </dl>                                     | Datos de texto ASCII. Este tipo de datos no termina en NULL. <br/> En el caso de los datos Unicode, cuando se especifican datos de texto ASCII, la \_ marca IFLAG Unicode también se debe establecer cuando se llama a la función de instancia de propiedad Attach.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**PROP \_ Type \_ IP \_ Address**</dt> </dl>                        | Dirección IP. (entidad de 4 bytes).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**PROP \_ Type \_ IPX \_ Address**</dt> </dl>                     | Dirección IPX. (entidad de 10 bytes).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**PROP \_ Type \_ BYTESWAPPED \_ Word**</dt> </dl>      | Obsoleto. Para los datos de palabras de intercambio de bytes, establezca **DataType** en prop \_ Type \_ Word y establezca la \_ marca IFLAG swapd al llamar a una función de instancia de propiedad **Attach** .<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**PROP \_ Type \_ BYTESWAPPED \_ DWORD**</dt> </dl>   | Obsoleto. Para los datos DWORD de intercambio de bytes, establezca **DataType** en prop \_ Type \_ DWORD y establezca la \_ marca IFLAG swapd al llamar a una función de instancia de propiedad **Attach** .<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**tipo de PROP ( \_ \_ cadena con tipo) \_**</dt> </dl>                  | Obsoleto. En el caso de los datos de cadena de tipo variable, establezca **DataType** en \_ cadena de tipo prop \_ y establezca la \_ marca IFLAG Unicode al llamar a una función de instancia de propiedad **Attach** .<br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**\_ \_ datos sin procesar de tipo prop \_**</dt> </dl>                              | Datos sin procesar de longitud y formato desconocidos.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**PROP ( \_ Comentario de tipo) \_**</dt> </dl>                                  | Igual que el \_ tipo de prop \_ void.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**PROP \_ Type \_ SRCFRIENDLYNAME**</dt> </dl>          | Dirección del nombre descriptivo del código fuente. Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**PROP \_ Type \_ DSTFRIENDLYNAME**</dt> </dl>          | Dirección del nombre descriptivo del destino. Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**PROP \_ Type \_ TOKENRING \_ dirección**</dt> </dl>   | Dirección de token-ring. Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**PROP \_ Type \_ FDDI \_ Address**</dt> </dl>                  | Dirección FDDI. Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**PROP \_ Type \_ Ethernet \_ Address**</dt> </dl>      | Dirección Ethernet. Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**PROP \_ ( \_ identificador de objeto de tipo) \_**</dt> </dl>   | Identificador de objeto SNMP con codificación BER.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**PROP \_ Type \_ Vines \_ IP \_ Address**</dt> </dl>     | Dirección IP de Vines (entidad de 6 bytes).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**PROP \_ Type \_ var \_ Len \_ Small \_ int**</dt> </dl> | Valor numérico sin una longitud determinada previamente, pero no más de 8 bytes de longitud. La longitud de los datos adjuntos determina la longitud del valor.<br/>                                                                                                                                                |



 

</dd> <dt>

**Qualifier**
</dt> <dd>

Calificador de datos de una propiedad. Este miembro proporciona información precisa sobre el tipo de datos.

El valor de **Qualifier** puede tener uno de los valores siguientes.



| Value                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**PROP \_ . \_ ninguno**</dt> </dl>                                      | El tipo de datos de la propiedad es la única especificación de la propiedad. <br/> Cuando se establece este valor, el miembro Union de la estructura se establece en **null** y, a continuación, se omite.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**PROPal \_ \_ Range**</dt> </dl>                                   | Se espera que el valor numérico esté dentro de un intervalo determinado. Defina el intervalo en el miembro **lpRange** .<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**PROPia \_ \_ set**</dt> </dl>                                         | El valor de una propiedad se compara con un conjunto de valores que se especifican en el miembro **lpSet** de la Unión de la estructura. El valor de una propiedad puede ser un **byte**, una **palabra**, un **valor DWORD**, un **LARGEINT** o una **hora**.<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**PROP \_ . \_**</dt> </dl>                          | Obsoleto.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**PROPia con \_ \_ etiqueta \_ establecido**</dt> </dl>                | El valor de una propiedad se compara con un valor en un conjunto de pares de etiqueta de valor. Los pares de etiqueta de valor se especifican en el miembro **lpSet** de la Unión de la estructura. <br/> En el momento de la presentación, si el valor de la propiedad coincide con un valor del conjunto, se muestran tanto un valor como la etiqueta asociada.<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**PROPia con la etiqueta de campo de \_ \_ \_ bits**</dt> </dl> | Obsoleto. \_ \_ En su lugar, use las marcas prop.<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**PROPia \_ \_ const**</dt> </dl>                                   | El valor de una propiedad se compara con una constante que se especifica en el miembro de **valor** de la Unión. <br/> En el momento de la presentación, si los valores de propiedad y la constante no coinciden, aparece un mensaje de error con formato con el valor establecido como normal.<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**marcas PROPn \_ \_**</dt> </dl>                                   | El valor de la propiedad se compara con los BITs específicos identificados en el miembro **lpSet** de la Unión.<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**PROPy ( \_ \_ matriz)**</dt> </dl>                                   | El valor de una propiedad especifica una matriz de valores. La longitud de los datos adjuntos determina la longitud de una matriz. <br/> Cuando se establece el valor de la matriz PROPy \_ \_ , el miembro Union de la estructura de datos **PROPERTYINFO** se establece en **null** y se omite.<br/>                                                    |



 

</dd> <dt>

**lpExtendedInfo**
</dt> <dd>

Reserved (miembro de Union).

</dd> <dt>

**lpRange**
</dt> <dd>

Puntero a una estructura de [rango](range.md) que define un intervalo de valores. Este miembro debe establecerse si el miembro de **calificador** de la estructura se ha establecido en propness \_ \_ Range (miembro de Union).

</dd> <dt>

**lpSet**
</dt> <dd>

Puntero a una estructura de [conjunto](set.md) que especifica un conjunto de valores o etiquetas. Este miembro debe establecerse si el miembro de **calificador** de la estructura se ha establecido en propia \_ \_ Set, propia \_ \_ etiquetada \_ set o props \_ \_ (miembro de Union).

</dd> <dt>

**Máscara**
</dt> <dd>

Obsoleto (miembro de Union).

</dd> <dt>

**Valor**
</dt> <dd>

Valor constante que se usa cuando se establece el elemento **Qualifier** en propism \_ \_ const (miembro de Union).

</dd> <dt>

**FormatStringSize**
</dt> <dd>

Tamaño máximo que se usa solo para la descripción de la propiedad.

</dd> <dt>

**InstanceData**
</dt> <dd>

Especifique la función de formato a la que se llama para dar formato a los datos mostrados para la propiedad. Para usar el formateador genérico, especifique la función **FormatPropertyInstance** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **PROPERTYINFO** se utiliza en las llamadas a la función [AddProperty](/previous-versions/bb251873(v=msdn.10)) . La función **AddProperty** agrega una definición de propiedad única a la [*base de datos de propiedades*](p.md)de analizador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[VARIEDAD](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

