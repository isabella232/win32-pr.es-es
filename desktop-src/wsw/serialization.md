---
title: Serialización
description: La serialización es el proceso de escribir valores en estructuras de datos de C (estructuras, matrices y valores primitivos) como un elemento XML. La deserialización es el proceso inverso.
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- Servicios web de serialización para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ecfa82844a45c6a5c2fcdabbc867c08d5531fd7c9d92a16c5eb8cbd9090af01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440715"
---
# <a name="serialization"></a>Serialización

La serialización es el proceso de escribir valores en estructuras de datos de C (estructuras, matrices y valores primitivos) como un elemento XML. La deserialización es el proceso inverso.


La serialización es el proceso de escribir valores en estructuras de datos de C (estructuras, matrices y valores primitivos) como un elemento XML. La deserialización es el proceso inverso.

Ambos procesos se basan en una descripción de la asignación entre las estructuras de datos de C y el XML.

![Diagrama que muestra cómo la serialización y la deserialización se basan en una descripción de la asignación entre las estructuras de datos de C y el XML.](images/xmlmapping.png)

Para serializar un valor, la aplicación llama a [**WsWriteElement,**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) o [**WsWriteType.**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

Para deserializar un valor, la aplicación llama [**a WsReadElement,**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement) [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) o [**WsReadType.**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)

## <a name="security"></a>Seguridad

[El Lector XML](xml-reader.md) se usa en el proceso de deserialización. Consulte la sección de seguridad del Lector XML para información de seguridad relacionada con XML.

El deserializador continúa deserializar los datos hasta que haya terminado de leer el elemento que se está deserialización. Se produce un error en el proceso de deserialización cuando encuentra cualquier documento XML que no se ajuste a la descripción de los datos que se están deserialización. En ese momento, el lector XML que se usa deja de ser válido y se devuelve un error.

De forma predeterminada, la deserialización es estricta. Algunas condiciones que hacen que la deserialización no se puedan producir incluyen, entre otras:

-   Faltan elementos esperados
-   Aparecen campos de elementos inesperados entre los elementos necesarios
-   Contenido de elemento adicional después de los campos obligatorios, a menos que **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**
-   Atributos inesperados, a menos que se especifique la marca [**\_ IGNORE \_ \_ UNHANDLED \_ ATTRIBUTES de WS STRUCT**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx)
-   Valor de tipo de datos inesperado que está fuera del intervalo especificado
-   El recuento de elementos repetidos está fuera del intervalo especificado

Serializar una gran cantidad de datos puede provocar una asignación excesiva de memoria y puede provocar ataques por denegación de servicio. El usuario que deserializará los datos debe especificar un objeto Montón para asignar los datos y el usuario puede usar el límite de asignación del montón para evitar ataques de asignación de memoria.

La compatibilidad con intervalos para tipos de datos, incluida la longitud máxima de la cadena, el número máximo de elementos en la matriz, etc., permite al usuario controlar el tamaño máximo de los distintos tipos de datos. El usuario puede especificar el intervalo en la descripción o el esquema de los datos para limitar el tamaño máximo de los distintos datos.

Un valor de cadena que contiene un cero incrustado se admite en los formatos de conexión (texto, binario, MTOM). Al deserializar una cadena con un cero incrustado, el usuario debe usar una cadena con recuento (WS STRING) para que el cero no confunda el cálculo de la longitud de \_ la cadena. Si un valor de cadena que contiene un cero incrustado se deserializa en un campo que espera una cadena terminada en cero, se devuelve un error y se produce un error de deserialización. Si wsutil se usa para generar descripciones de datos, se debe usar la opción /string:WS STRING si se espera una cadena con \_ cero incrustado.

Las devoluciones de llamada siguientes se usan con la serialización:

-   [**DEVOLUCIÓN DE LLAMADA \_ DE \_ COMPARACIÓN DE \_ DURACIÓN DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**WS \_ READ \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**WS \_ WRITE \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

Las enumeraciones siguientes se usan con serialización:

-   [**ASIGNACIÓN DE \_ CAMPOS WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [**OPCIONES DE \_ CAMPO WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [**WS \_ READ \_ OPTION**](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [**WS \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [**ASIGNACIÓN DE TIPOS DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [**WS \_ WRITE \_ OPTION**](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

Las funciones siguientes se usan con la serialización:

-   [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

Las estructuras siguientes se usan con serialización:

-   [**DESCRIPCIÓN DEL ATRIBUTO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [**DESCRIPCIÓN DE WS \_ BOOL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [**DESCRIPCIÓN DE \_ BYTES WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [**DESCRIPCIÓN DE LA \_ MATRIZ \_ DE BYTES WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [**DESCRIPCIÓN DE LA \_ MATRIZ WS CHAR \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [**DESCRIPCIÓN DEL \_ TIPO \_ PERSONALIZADO DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [**DESCRIPCIÓN \_ DE DATETIME DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [**WS \_ DECIMAL \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [**VALOR PREDETERMINADO DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [**WS \_ DOUBLE \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [**DESCRIPCIÓN DE LA DURACIÓN DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [**DESCRIPCIÓN DEL \_ ELEMENTO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [**DESCRIPCIÓN DE LA \_ DIRECCIÓN DEL PUNTO DE CONEXIÓN \_ \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [**DESCRIPCIÓN DE \_ LA ENUMERACIÓN DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [**WS \_ ENUM \_ VALUE**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [**DESCRIPCIÓN DEL ERROR DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [**DESCRIPCIÓN DEL \_ CAMPO WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [**DESCRIPCIÓN \_ DE WS FLOAT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [**DESCRIPCIÓN DEL GUID de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [**WS \_ INT16 \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [**WS \_ INT32 \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [**WS \_ INT64 \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [**WS \_ INT8 \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [**INTERVALO DE ELEMENTOS DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [**DESCRIPCIÓN DE LA \_ CADENA WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [**DESCRIPCIÓN DE STRUCT de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [**WS \_ TIMESPAN \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [**DESCRIPCIÓN DE \_ WS UINT16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [**DESCRIPCIÓN DE \_ WS UINT32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [**DESCRIPCIÓN DE \_ WS UINT64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [**DESCRIPCIÓN \_ DE WS \_ UINT8**](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [**DESCRIPCIÓN DE WS \_ UNION \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [**DESCRIPCIÓN DEL \_ CAMPO WS UNION \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [**DESCRIPCIÓN DEL IDENTIFICADOR \_ \_ ÚNICO DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [**DESCRIPCIÓN DE LA \_ MATRIZ UTF8 \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [**DESCRIPCIÓN DE WS \_ VOID \_**](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [**DESCRIPCIÓN DE \_ WS \_ WSZ**](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [**WS \_ XML \_ QNAME \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [**DESCRIPCIÓN DE LA \_ CADENA XML \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




