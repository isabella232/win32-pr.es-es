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
# <a name="serialization"></a><span data-ttu-id="be4e2-107">Serialización</span><span class="sxs-lookup"><span data-stu-id="be4e2-107">Serialization</span></span>

<span data-ttu-id="be4e2-108">La serialización es el proceso de escribir valores en las estructuras de datos de C (Structs, matrices y valores primitivos) como un elemento XML.</span><span class="sxs-lookup"><span data-stu-id="be4e2-108">Serialization is the process of writing values in C data structures (structs, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="be4e2-109">La deserialización es el proceso inverso.</span><span class="sxs-lookup"><span data-stu-id="be4e2-109">Deserialization is the reverse process.</span></span>


<span data-ttu-id="be4e2-110">La serialización es el proceso de escribir valores en las estructuras de datos de C (estructuras, matrices y valores primitivos) como un elemento XML.</span><span class="sxs-lookup"><span data-stu-id="be4e2-110">Serialization is the process of writing values in C data structures (structures, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="be4e2-111">La deserialización es el proceso inverso.</span><span class="sxs-lookup"><span data-stu-id="be4e2-111">Deserialization is the reverse process.</span></span>

<span data-ttu-id="be4e2-112">Ambos procesos dependen de una descripción de la asignación entre las estructuras de datos de C y el XML.</span><span class="sxs-lookup"><span data-stu-id="be4e2-112">Both processes rely on a description of the mapping between the C data structures and the XML.</span></span>

![Diagrama que muestra cómo la serialización y la deserialización se basan en una descripción de la asignación entre las estructuras de datos de C y el XML.](images/xmlmapping.png)

<span data-ttu-id="be4e2-114">Para serializar un valor, la aplicación llama a [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) o [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span><span class="sxs-lookup"><span data-stu-id="be4e2-114">To serialize a value, the application calls [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) or [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span></span>

<span data-ttu-id="be4e2-115">Para deserializar un valor, la aplicación llama a [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) o [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span><span class="sxs-lookup"><span data-stu-id="be4e2-115">To deserialize a value, the application calls [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) or [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span></span>

## <a name="security"></a><span data-ttu-id="be4e2-116">Seguridad</span><span class="sxs-lookup"><span data-stu-id="be4e2-116">Security</span></span>

<span data-ttu-id="be4e2-117">El [lector XML](xml-reader.md) se utiliza en el proceso de deserialización.</span><span class="sxs-lookup"><span data-stu-id="be4e2-117">[XML Reader](xml-reader.md) is used in deserialization process.</span></span> <span data-ttu-id="be4e2-118">Consulte la sección seguridad en el lector XML para obtener información de seguridad relacionada con XML.</span><span class="sxs-lookup"><span data-stu-id="be4e2-118">Refer to the security section in XML Reader for XML related security information.</span></span>

<span data-ttu-id="be4e2-119">El deserializador continúa deserializando los datos hasta que se ha completado la lectura del elemento que se está deserializando.</span><span class="sxs-lookup"><span data-stu-id="be4e2-119">The deserializer continues to deserialize data until it has completed reading the element being deserialized.</span></span> <span data-ttu-id="be4e2-120">El proceso de deserialización produce un error cuando encuentra algún documento XML que no se ajusta a la descripción de los datos que se están deserializando.</span><span class="sxs-lookup"><span data-stu-id="be4e2-120">Deserialization process fails when it encounter any XML document that does not conform to the description of the data being deserialized.</span></span> <span data-ttu-id="be4e2-121">En ese momento, el lector XML que se está usando deja de ser válido y se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="be4e2-121">At that point XML reader being used becomes invalid, and an error is returned.</span></span>

<span data-ttu-id="be4e2-122">De forma predeterminada, la deserialización es estricta.</span><span class="sxs-lookup"><span data-stu-id="be4e2-122">By default deserialization is strict.</span></span> <span data-ttu-id="be4e2-123">Entre las condiciones que provocan errores en la deserialización se incluyen, pero no se limita a:</span><span class="sxs-lookup"><span data-stu-id="be4e2-123">Some conditions that cause deserialization to fail include but not limited to:</span></span>

-   <span data-ttu-id="be4e2-124">Faltan elementos esperados</span><span class="sxs-lookup"><span data-stu-id="be4e2-124">Expected elements is missing</span></span>
-   <span data-ttu-id="be4e2-125">Los campos de elemento inesperados aparecen entre los elementos necesarios</span><span class="sxs-lookup"><span data-stu-id="be4e2-125">Unexpected element fields appear between required elements</span></span>
-   <span data-ttu-id="be4e2-126">Contenido de elementos adicionales después de los campos obligatorios, a menos que el **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="be4e2-126">Extra element content after required fields, unless the **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span></span>
-   <span data-ttu-id="be4e2-127">Atributos inesperados, a menos que se especifique la marca [**WS \_ struct \_ Ignore \_ \_ attributes no controlados**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="be4e2-127">Unexpected attributes, unless [**WS\_STRUCT\_IGNORE\_UNHANDLED\_ATTRIBUTES**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) flag is specified</span></span>
-   <span data-ttu-id="be4e2-128">Valor de tipo de datos inesperado fuera del intervalo especificado</span><span class="sxs-lookup"><span data-stu-id="be4e2-128">Unexpected data type value that is out of specified range</span></span>
-   <span data-ttu-id="be4e2-129">El recuento del elemento repetido está fuera del intervalo especificado</span><span class="sxs-lookup"><span data-stu-id="be4e2-129">Count of repeating element is out of the specified range</span></span>

<span data-ttu-id="be4e2-130">La serialización de una gran cantidad de datos puede provocar una asignación de memoria excesiva y provocar ataques de denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="be4e2-130">Serializing large amount of data might cause excessive memory allocation and can cause denial of service attack.</span></span> <span data-ttu-id="be4e2-131">El usuario que está deserializando los datos debe especificar un objeto de montón para asignar los datos y el usuario puede usar el límite de asignación del montón para evitar ataques de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="be4e2-131">The user that is deserializing data must specify a Heap object to allocate the data, and the user can use the heap allocation limit to prevent memory allocation attack.</span></span>

<span data-ttu-id="be4e2-132">La compatibilidad con el intervalo de tipos de datos, incluida la longitud máxima de la cadena, el número máximo de elementos de la matriz, etc. permite al usuario controlar el tamaño máximo de los distintos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="be4e2-132">Range support for data types, including max length for string, max element count in array, etc. allows the user to control the maximum size for different data types.</span></span> <span data-ttu-id="be4e2-133">El usuario puede especificar el intervalo en la descripción o el esquema de los datos para limitar el tamaño máximo de los diferentes datos.</span><span class="sxs-lookup"><span data-stu-id="be4e2-133">User can specify range in data description or schema to limit the maximum size of different data.</span></span>

<span data-ttu-id="be4e2-134">Un valor de cadena que contiene un cero incrustado se admite en los formatos de conexión (texto, binario, MTOM).</span><span class="sxs-lookup"><span data-stu-id="be4e2-134">A string value containing an embedded zero is supported in the wire formats (text, binary, MTOM).</span></span> <span data-ttu-id="be4e2-135">Al deserializar una cadena con un cero incrustado, el usuario debe usar una cadena de cuenta (cadena de WS \_ ) para que el cero no confunda el cálculo de la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="be4e2-135">When deserializing a string with an embedded zero, the user should use a counted string (WS\_STRING) so the zero will not confuse the calculation of the length of the string.</span></span> <span data-ttu-id="be4e2-136">Si un valor de cadena que contiene un cero incrustado se deserializa en un campo que espera una cadena terminada en cero, se devuelve un error y se produce un error en la deserialización.</span><span class="sxs-lookup"><span data-stu-id="be4e2-136">If a string value containing an embedded zero is deserialized into a field that is expecting a zero-terminated string, an error is returned, and deserialization fails.</span></span> <span data-ttu-id="be4e2-137">Si se usa wsutil para generar descripciones de datos, se debe utilizar la opción de cadena/String: WS \_ si se espera una cadena con cero incrustado.</span><span class="sxs-lookup"><span data-stu-id="be4e2-137">If wsutil is used to generate data descriptions, /string:WS\_STRING option should be used if string with embedded zero is expected.</span></span>

<span data-ttu-id="be4e2-138">Las siguientes devoluciones de llamada se utilizan con la serialización:</span><span class="sxs-lookup"><span data-stu-id="be4e2-138">The following callbacks are used with serialization:</span></span>

-   [<span data-ttu-id="be4e2-139">**\_devolución de \_ llamada de comparación de WS Duration \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-139">**WS\_DURATION\_COMPARISON\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [<span data-ttu-id="be4e2-140">**\_devolución de \_ llamada de tipo de lectura de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-140">**WS\_READ\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [<span data-ttu-id="be4e2-141">**\_devolución de \_ llamada de tipo de escritura de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-141">**WS\_WRITE\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

<span data-ttu-id="be4e2-142">Las enumeraciones siguientes se usan con la serialización:</span><span class="sxs-lookup"><span data-stu-id="be4e2-142">The following enumerations are used with serialization:</span></span>

-   [<span data-ttu-id="be4e2-143">**\_asignación de campos de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-143">**WS\_FIELD\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [<span data-ttu-id="be4e2-144">**\_Opciones de campo de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-144">**WS\_FIELD\_OPTIONS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="be4e2-145">**\_opción de lectura de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-145">**WS\_READ\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [<span data-ttu-id="be4e2-146">**tipo de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-146">**WS\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [<span data-ttu-id="be4e2-147">**\_asignación de tipo WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-147">**WS\_TYPE\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [<span data-ttu-id="be4e2-148">**\_opción de escritura de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-148">**WS\_WRITE\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

<span data-ttu-id="be4e2-149">Las siguientes funciones se usan con la serialización:</span><span class="sxs-lookup"><span data-stu-id="be4e2-149">The following functions are used with serialization:</span></span>

-   [<span data-ttu-id="be4e2-150">**WsReadAttribute**</span><span class="sxs-lookup"><span data-stu-id="be4e2-150">**WsReadAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [<span data-ttu-id="be4e2-151">**WsReadElement**</span><span class="sxs-lookup"><span data-stu-id="be4e2-151">**WsReadElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [<span data-ttu-id="be4e2-152">**WsReadType**</span><span class="sxs-lookup"><span data-stu-id="be4e2-152">**WsReadType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [<span data-ttu-id="be4e2-153">**WsWriteAttribute**</span><span class="sxs-lookup"><span data-stu-id="be4e2-153">**WsWriteAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [<span data-ttu-id="be4e2-154">**WsWriteElement**</span><span class="sxs-lookup"><span data-stu-id="be4e2-154">**WsWriteElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [<span data-ttu-id="be4e2-155">**WsWriteType**</span><span class="sxs-lookup"><span data-stu-id="be4e2-155">**WsWriteType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

<span data-ttu-id="be4e2-156">Las siguientes estructuras se usan con la serialización:</span><span class="sxs-lookup"><span data-stu-id="be4e2-156">The following structures are used with serialization:</span></span>

-   [<span data-ttu-id="be4e2-157">**\_Descripción del atributo WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-157">**WS\_ATTRIBUTE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [<span data-ttu-id="be4e2-158">**Descripción de WS \_ bool \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-158">**WS\_BOOL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [<span data-ttu-id="be4e2-159">**Descripción de WS \_ bytes \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-159">**WS\_BYTES\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [<span data-ttu-id="be4e2-160">**Descripción de la \_ matriz de bytes WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-160">**WS\_BYTE\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [<span data-ttu-id="be4e2-161">**Descripción de la \_ matriz de caracteres WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-161">**WS\_CHAR\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [<span data-ttu-id="be4e2-162">**\_Descripción de \_ tipo \_ personalizado de WS**</span><span class="sxs-lookup"><span data-stu-id="be4e2-162">**WS\_CUSTOM\_TYPE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [<span data-ttu-id="be4e2-163">**Descripción de WS \_ DateTime \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-163">**WS\_DATETIME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [<span data-ttu-id="be4e2-164">**Descripción de WS \_ decimal \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-164">**WS\_DECIMAL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [<span data-ttu-id="be4e2-165">**\_valor predeterminado de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-165">**WS\_DEFAULT\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [<span data-ttu-id="be4e2-166">**Descripción de WS- \_ Double \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-166">**WS\_DOUBLE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [<span data-ttu-id="be4e2-167">**Descripción de la duración de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-167">**WS\_DURATION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [<span data-ttu-id="be4e2-168">**\_Descripción del elemento WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-168">**WS\_ELEMENT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [<span data-ttu-id="be4e2-169">**Descripción de la dirección del punto de conexión de WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-169">**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [<span data-ttu-id="be4e2-170">**Descripción de la \_ enumeración WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-170">**WS\_ENUM\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [<span data-ttu-id="be4e2-171">**\_valor de enumeración de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-171">**WS\_ENUM\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [<span data-ttu-id="be4e2-172">**\_Descripción del error de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-172">**WS\_FAULT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [<span data-ttu-id="be4e2-173">**\_Descripción del campo WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-173">**WS\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [<span data-ttu-id="be4e2-174">**Descripción de WS \_ float \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-174">**WS\_FLOAT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [<span data-ttu-id="be4e2-175">**\_Descripción del GUID de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-175">**WS\_GUID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [<span data-ttu-id="be4e2-176">**Descripción de WS \_ INT16 \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-176">**WS\_INT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [<span data-ttu-id="be4e2-177">**\_Descripción de INT32 de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-177">**WS\_INT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [<span data-ttu-id="be4e2-178">**Descripción de WS \_ INT64 \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-178">**WS\_INT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [<span data-ttu-id="be4e2-179">**Descripción de WS \_ INT8 \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-179">**WS\_INT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [<span data-ttu-id="be4e2-180">**\_intervalo de elementos de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-180">**WS\_ITEM\_RANGE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [<span data-ttu-id="be4e2-181">**Descripción de la \_ cadena WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-181">**WS\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [<span data-ttu-id="be4e2-182">**Descripción de la \_ estructura WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-182">**WS\_STRUCT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [<span data-ttu-id="be4e2-183">**Descripción de WS \_ TIMESPAN \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-183">**WS\_TIMESPAN\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [<span data-ttu-id="be4e2-184">**Descripción de WS \_ UINT16 \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-184">**WS\_UINT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [<span data-ttu-id="be4e2-185">**Descripción de WS \_ UINT32 \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-185">**WS\_UINT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [<span data-ttu-id="be4e2-186">**Descripción de WS \_ UINT64 \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-186">**WS\_UINT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [<span data-ttu-id="be4e2-187">**Descripción de WS \_ UINT8 \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-187">**WS\_UINT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [<span data-ttu-id="be4e2-188">**Descripción de la Unión de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-188">**WS\_UNION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [<span data-ttu-id="be4e2-189">**\_Descripción del \_ campo de unión de WS \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-189">**WS\_UNION\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [<span data-ttu-id="be4e2-190">**\_Descripción del \_ identificador \_ único de WS**</span><span class="sxs-lookup"><span data-stu-id="be4e2-190">**WS\_UNIQUE\_ID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [<span data-ttu-id="be4e2-191">**Descripción de la matriz de WS \_ UTF8 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-191">**WS\_UTF8\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [<span data-ttu-id="be4e2-192">**Descripción de WS \_ void \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-192">**WS\_VOID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [<span data-ttu-id="be4e2-193">**Descripción de WS \_ WSZ \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-193">**WS\_WSZ\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [<span data-ttu-id="be4e2-194">**\_Descripción de \_ QNAME \_ XML de WS**</span><span class="sxs-lookup"><span data-stu-id="be4e2-194">**WS\_XML\_QNAME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [<span data-ttu-id="be4e2-195">**Descripción de la \_ cadena XML de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be4e2-195">**WS\_XML\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




