---
title: Serialización
description: La serialización es el proceso de escribir valores en las estructuras de datos de C (Structs, matrices y valores primitivos) como un elemento XML. La deserialización es el proceso inverso.
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- Servicios Web de serialización para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f986c6cec9a035424aaafe1c51f4dc0d3ee014
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104279756"
---
# <a name="serialization"></a>Serialización

La serialización es el proceso de escribir valores en las estructuras de datos de C (Structs, matrices y valores primitivos) como un elemento XML. La deserialización es el proceso inverso.


La serialización es el proceso de escribir valores en las estructuras de datos de C (estructuras, matrices y valores primitivos) como un elemento XML. La deserialización es el proceso inverso.

Ambos procesos dependen de una descripción de la asignación entre las estructuras de datos de C y el XML.

![Diagrama que muestra cómo la serialización y la deserialización se basan en una descripción de la asignación entre las estructuras de datos de C y el XML.](images/xmlmapping.png)

Para serializar un valor, la aplicación llama a [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) o [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).

Para deserializar un valor, la aplicación llama a [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) o [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).

## <a name="security"></a>Seguridad

El [lector XML](xml-reader.md) se utiliza en el proceso de deserialización. Consulte la sección seguridad en el lector XML para obtener información de seguridad relacionada con XML.

El deserializador continúa deserializando los datos hasta que se ha completado la lectura del elemento que se está deserializando. El proceso de deserialización produce un error cuando encuentra algún documento XML que no se ajusta a la descripción de los datos que se están deserializando. En ese momento, el lector XML que se está usando deja de ser válido y se devuelve un error.

De forma predeterminada, la deserialización es estricta. Entre las condiciones que provocan errores en la deserialización se incluyen, pero no se limita a:

-   Faltan elementos esperados
-   Los campos de elemento inesperados aparecen entre los elementos necesarios
-   Contenido de elementos adicionales después de los campos obligatorios, a menos que el **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**
-   Atributos inesperados, a menos que se especifique la marca [**WS \_ struct \_ Ignore \_ \_ attributes no controlados**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx)
-   Valor de tipo de datos inesperado fuera del intervalo especificado
-   El recuento del elemento repetido está fuera del intervalo especificado

La serialización de una gran cantidad de datos puede provocar una asignación de memoria excesiva y provocar ataques de denegación de servicio. El usuario que está deserializando los datos debe especificar un objeto de montón para asignar los datos y el usuario puede usar el límite de asignación del montón para evitar ataques de asignación de memoria.

La compatibilidad con el intervalo de tipos de datos, incluida la longitud máxima de la cadena, el número máximo de elementos de la matriz, etc. permite al usuario controlar el tamaño máximo de los distintos tipos de datos. El usuario puede especificar el intervalo en la descripción o el esquema de los datos para limitar el tamaño máximo de los diferentes datos.

Un valor de cadena que contiene un cero incrustado se admite en los formatos de conexión (texto, binario, MTOM). Al deserializar una cadena con un cero incrustado, el usuario debe usar una cadena de cuenta (cadena de WS \_ ) para que el cero no confunda el cálculo de la longitud de la cadena. Si un valor de cadena que contiene un cero incrustado se deserializa en un campo que espera una cadena terminada en cero, se devuelve un error y se produce un error en la deserialización. Si se usa wsutil para generar descripciones de datos, se debe utilizar la opción de cadena/String: WS \_ si se espera una cadena con cero incrustado.

Las siguientes devoluciones de llamada se utilizan con la serialización:

-   [**\_devolución de \_ llamada de comparación de WS Duration \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_devolución de \_ llamada de tipo de lectura de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_devolución de \_ llamada de tipo de escritura de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

Las enumeraciones siguientes se usan con la serialización:

-   [**\_asignación de campos de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [**\_Opciones de campo de WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_opción de lectura de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [**tipo de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [**\_asignación de tipo WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [**\_opción de escritura de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

Las siguientes funciones se usan con la serialización:

-   [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

Las siguientes estructuras se usan con la serialización:

-   [**\_Descripción del atributo WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [**Descripción de WS \_ bool \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [**Descripción de WS \_ bytes \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [**Descripción de la \_ matriz de bytes WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [**Descripción de la \_ matriz de caracteres WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [**\_Descripción de \_ tipo \_ personalizado de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [**Descripción de WS \_ DateTime \_**](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [**Descripción de WS \_ decimal \_**](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [**\_valor predeterminado de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [**Descripción de WS- \_ Double \_**](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [**Descripción de la duración de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [**\_Descripción del elemento WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [**Descripción de la dirección del punto de conexión de WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [**Descripción de la \_ enumeración WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [**\_valor de enumeración de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [**\_Descripción del error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [**\_Descripción del campo WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [**Descripción de WS \_ float \_**](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [**\_Descripción del GUID de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [**Descripción de WS \_ INT16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [**\_Descripción de INT32 de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [**Descripción de WS \_ INT64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [**Descripción de WS \_ INT8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [**\_intervalo de elementos de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [**Descripción de la \_ cadena WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [**Descripción de la \_ estructura WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [**Descripción de WS \_ TIMESPAN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [**Descripción de WS \_ UINT16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [**Descripción de WS \_ UINT32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [**Descripción de WS \_ UINT64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [**Descripción de WS \_ UINT8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [**Descripción de la Unión de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [**\_Descripción del \_ campo de unión de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [**\_Descripción del \_ identificador \_ único de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [**Descripción de la matriz de WS \_ UTF8 \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [**Descripción de WS \_ void \_**](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [**Descripción de WS \_ WSZ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [**\_Descripción de \_ QNAME \_ XML de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [**Descripción de la \_ cadena XML de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




