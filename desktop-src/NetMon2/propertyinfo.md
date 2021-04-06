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
# <a name="propertyinfo-structure"></a><span data-ttu-id="0c484-103">PROPERTYINFO (estructura)</span><span class="sxs-lookup"><span data-stu-id="0c484-103">PROPERTYINFO structure</span></span>

<span data-ttu-id="0c484-104">La estructura de datos **PROPERTYINFO** define una propiedad del protocolo.</span><span class="sxs-lookup"><span data-stu-id="0c484-104">The **PROPERTYINFO** data structure defines one property of the protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c484-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c484-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="0c484-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c484-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c484-107">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="0c484-107">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-108">Establezca este campo en cero.</span><span class="sxs-lookup"><span data-stu-id="0c484-108">Set this field to zero.</span></span> <span data-ttu-id="0c484-109">En la salida, Monitor de red devuelve un identificador a la propiedad después de que la propiedad se agregue a la base de datos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c484-109">On output, Network Monitor returns a handle to the property after the property is added to the property database.</span></span>

</dd> <dt>

<span data-ttu-id="0c484-110">**Versión**</span><span class="sxs-lookup"><span data-stu-id="0c484-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0c484-111">Reserved.</span></span> <span data-ttu-id="0c484-112">Debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="0c484-112">Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0c484-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="0c484-113">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-114">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-114">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="0c484-115">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="0c484-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-116">Descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-116">Description of the property.</span></span> <span data-ttu-id="0c484-117">La descripción aparece en la barra de estado de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="0c484-117">The description appears on the Network Monitor status bar.</span></span>

</dd> <dt>

<span data-ttu-id="0c484-118">**DataType**</span><span class="sxs-lookup"><span data-stu-id="0c484-118">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-119">Tipo de datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-119">Data type of the property.</span></span> <span data-ttu-id="0c484-120">Este miembro puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0c484-120">This member can have one of the following values.</span></span>



| <span data-ttu-id="0c484-121">Value</span><span class="sxs-lookup"><span data-stu-id="0c484-121">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="0c484-122">Significado</span><span class="sxs-lookup"><span data-stu-id="0c484-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <span data-ttu-id="0c484-123"><dt>**PROP \_ Type \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-123"><dt>**PROP\_TYPE\_VOID**</dt></span></span> </dl>                                           | <span data-ttu-id="0c484-124">No se conoce el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-124">Property type is unknown.</span></span> <span data-ttu-id="0c484-125">No hay ninguna longitud o formato implícito.</span><span class="sxs-lookup"><span data-stu-id="0c484-125">There is no implied length or format.</span></span><br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <span data-ttu-id="0c484-126"><dt>**\_Resumen de tipo de prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-126"><dt>**PROP\_TYPE\_SUMMARY**</dt></span></span> </dl>                                  | <span data-ttu-id="0c484-127">Resumen del tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-127">Summarizing property type.</span></span> <span data-ttu-id="0c484-128">Indica la primera instancia de la propiedad que el analizador asocia a un marco.</span><span class="sxs-lookup"><span data-stu-id="0c484-128">Indicates the first property instance that the parser attaches to a frame.</span></span> <span data-ttu-id="0c484-129">\_ \_ El Resumen de tipo prop puede servir como marcador de posición para los grupos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c484-129">PROP\_TYPE\_SUMMARY can serve as a placeholder for groups of properties.</span></span> <span data-ttu-id="0c484-130">Este valor indica que la propiedad no está definida en el *RFC* del protocolo.</span><span class="sxs-lookup"><span data-stu-id="0c484-130">This value indicates that the property is not defined in the protocol *RFC*.</span></span><br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <span data-ttu-id="0c484-131"><dt>**tipo de PROP \_ \_ byte**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-131"><dt>**PROP\_TYPE\_BYTE**</dt></span></span> </dl>                                           | <span data-ttu-id="0c484-132">Datos numéricos con un tamaño de un byte (entidad de 8 bits).</span><span class="sxs-lookup"><span data-stu-id="0c484-132">Numeric data with a size of one byte (8-bit entity).</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <span data-ttu-id="0c484-133"><dt>**PROP ( \_ tipo de \_ palabra)**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-133"><dt>**PROP\_TYPE\_WORD**</dt></span></span> </dl>                                           | <span data-ttu-id="0c484-134">Datos numéricos con un tamaño de dos bytes (entidad de 16 bits).</span><span class="sxs-lookup"><span data-stu-id="0c484-134">Numeric data with a size of two bytes (16-bit entity).</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <span data-ttu-id="0c484-135"><dt>**PROP ( \_ tipo \_ DWORD)**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-135"><dt>**PROP\_TYPE\_DWORD**</dt></span></span> </dl>                                        | <span data-ttu-id="0c484-136">Datos numéricos con un tamaño de cuatro bytes (entidad de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="0c484-136">Numeric data with a size of four bytes (32-bit entity).</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <span data-ttu-id="0c484-137"><dt>**PROP \_ Type \_ LARGEINT**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-137"><dt>**PROP\_TYPE\_LARGEINT**</dt></span></span> </dl>                               | <span data-ttu-id="0c484-138">Datos numéricos con un tamaño de ocho bytes (entidad de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="0c484-138">Numeric data with a size of eight bytes (64-bit entity).</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <span data-ttu-id="0c484-139"><dt>**PROP \_ Type \_ addr**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-139"><dt>**PROP\_TYPE\_ADDR**</dt></span></span> </dl>                                           | <span data-ttu-id="0c484-140">Dirección MAC (entidad de 6 bytes).</span><span class="sxs-lookup"><span data-stu-id="0c484-140">MAC address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <span data-ttu-id="0c484-141"><dt>**\_hora del tipo de prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-141"><dt>**PROP\_TYPE\_TIME**</dt></span></span> </dl>                                           | <span data-ttu-id="0c484-142">**SYSTEMTIME** (estructura).</span><span class="sxs-lookup"><span data-stu-id="0c484-142">**SYSTEMTIME** structure.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <span data-ttu-id="0c484-143"><dt>**PROP \_ Type ( \_ cadena)**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-143"><dt>**PROP\_TYPE\_STRING**</dt></span></span> </dl>                                     | <span data-ttu-id="0c484-144">Datos de texto ASCII.</span><span class="sxs-lookup"><span data-stu-id="0c484-144">ASCII text data.</span></span> <span data-ttu-id="0c484-145">Este tipo de datos no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="0c484-145">This data type is not NULL-terminated.</span></span> <br/> <span data-ttu-id="0c484-146">En el caso de los datos Unicode, cuando se especifican datos de texto ASCII, la \_ marca IFLAG Unicode también se debe establecer cuando se llama a la función de instancia de propiedad Attach.</span><span class="sxs-lookup"><span data-stu-id="0c484-146">For Unicode data, when ASCII text data is specified, the IFLAG\_UNICODE flag must also be set when the attach property instance function is called.</span></span><br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <span data-ttu-id="0c484-147"><dt>**PROP \_ Type \_ IP \_ Address**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-147"><dt>**PROP\_TYPE\_IP\_ADDRESS**</dt></span></span> </dl>                        | <span data-ttu-id="0c484-148">Dirección IP.</span><span class="sxs-lookup"><span data-stu-id="0c484-148">IP Address.</span></span> <span data-ttu-id="0c484-149">(entidad de 4 bytes).</span><span class="sxs-lookup"><span data-stu-id="0c484-149">(4-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <span data-ttu-id="0c484-150"><dt>**PROP \_ Type \_ IPX \_ Address**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-150"><dt>**PROP\_TYPE\_IPX\_ADDRESS**</dt></span></span> </dl>                     | <span data-ttu-id="0c484-151">Dirección IPX.</span><span class="sxs-lookup"><span data-stu-id="0c484-151">IPX Address.</span></span> <span data-ttu-id="0c484-152">(entidad de 10 bytes).</span><span class="sxs-lookup"><span data-stu-id="0c484-152">(10-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <span data-ttu-id="0c484-153"><dt>**PROP \_ Type \_ BYTESWAPPED \_ Word**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-153"><dt>**PROP\_TYPE\_BYTESWAPPED\_WORD**</dt></span></span> </dl>      | <span data-ttu-id="0c484-154">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0c484-154">Obsolete.</span></span> <span data-ttu-id="0c484-155">Para los datos de palabras de intercambio de bytes, establezca **DataType** en prop \_ Type \_ Word y establezca la \_ marca IFLAG swapd al llamar a una función de instancia de propiedad **Attach** .</span><span class="sxs-lookup"><span data-stu-id="0c484-155">For byte-swapped WORD data, set **DataType** to PROP\_TYPE\_WORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <span data-ttu-id="0c484-156"><dt>**PROP \_ Type \_ BYTESWAPPED \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-156"><dt>**PROP\_TYPE\_BYTESWAPPED\_DWORD**</dt></span></span> </dl>   | <span data-ttu-id="0c484-157">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0c484-157">Obsolete.</span></span> <span data-ttu-id="0c484-158">Para los datos DWORD de intercambio de bytes, establezca **DataType** en prop \_ Type \_ DWORD y establezca la \_ marca IFLAG swapd al llamar a una función de instancia de propiedad **Attach** .</span><span class="sxs-lookup"><span data-stu-id="0c484-158">For byte-swapped DWORD data, set **DataType** to PROP\_TYPE\_DWORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <span data-ttu-id="0c484-159"><dt>**tipo de PROP ( \_ \_ cadena con tipo) \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-159"><dt>**PROP\_TYPE\_TYPED\_STRING**</dt></span></span> </dl>                  | <span data-ttu-id="0c484-160">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0c484-160">Obsolete.</span></span> <span data-ttu-id="0c484-161">En el caso de los datos de cadena de tipo variable, establezca **DataType** en \_ cadena de tipo prop \_ y establezca la \_ marca IFLAG Unicode al llamar a una función de instancia de propiedad **Attach** .</span><span class="sxs-lookup"><span data-stu-id="0c484-161">For variable-type string data, set **DataType** to PROP\_TYPE\_STRING and set the IFLAG\_UNICODE flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <span data-ttu-id="0c484-162"><dt>**\_ \_ datos sin procesar de tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-162"><dt>**PROP\_TYPE\_RAW\_DATA**</dt></span></span> </dl>                              | <span data-ttu-id="0c484-163">Datos sin procesar de longitud y formato desconocidos.</span><span class="sxs-lookup"><span data-stu-id="0c484-163">Raw data of unknown length and format.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <span data-ttu-id="0c484-164"><dt>**PROP ( \_ Comentario de tipo) \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-164"><dt>**PROP\_TYPE\_COMMENT**</dt></span></span> </dl>                                  | <span data-ttu-id="0c484-165">Igual que el \_ tipo de prop \_ void.</span><span class="sxs-lookup"><span data-stu-id="0c484-165">Same as PROP\_TYPE\_VOID.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <span data-ttu-id="0c484-166"><dt>**PROP \_ Type \_ SRCFRIENDLYNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-166"><dt>**PROP\_TYPE\_SRCFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="0c484-167">Dirección del nombre descriptivo del código fuente.</span><span class="sxs-lookup"><span data-stu-id="0c484-167">Address of source-friendly name.</span></span> <span data-ttu-id="0c484-168">Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0c484-168">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <span data-ttu-id="0c484-169"><dt>**PROP \_ Type \_ DSTFRIENDLYNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-169"><dt>**PROP\_TYPE\_DSTFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="0c484-170">Dirección del nombre descriptivo del destino.</span><span class="sxs-lookup"><span data-stu-id="0c484-170">Address of destination friendly name.</span></span> <span data-ttu-id="0c484-171">Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0c484-171">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <span data-ttu-id="0c484-172"><dt>**PROP \_ Type \_ TOKENRING \_ dirección**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-172"><dt>**PROP\_TYPE\_TOKENRING\_ADDRESS**</dt></span></span> </dl>   | <span data-ttu-id="0c484-173">Dirección de token-ring.</span><span class="sxs-lookup"><span data-stu-id="0c484-173">Token-ring address.</span></span> <span data-ttu-id="0c484-174">Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0c484-174">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <span data-ttu-id="0c484-175"><dt>**PROP \_ Type \_ FDDI \_ Address**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-175"><dt>**PROP\_TYPE\_FDDI\_ADDRESS**</dt></span></span> </dl>                  | <span data-ttu-id="0c484-176">Dirección FDDI.</span><span class="sxs-lookup"><span data-stu-id="0c484-176">FDDI address.</span></span> <span data-ttu-id="0c484-177">Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0c484-177">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <span data-ttu-id="0c484-178"><dt>**PROP \_ Type \_ Ethernet \_ Address**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-178"><dt>**PROP\_TYPE\_ETHERNET\_ADDRESS**</dt></span></span> </dl>      | <span data-ttu-id="0c484-179">Dirección Ethernet.</span><span class="sxs-lookup"><span data-stu-id="0c484-179">Ethernet address.</span></span> <span data-ttu-id="0c484-180">Monitor de red no proporciona compatibilidad con el formato integrado para este tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0c484-180">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <span data-ttu-id="0c484-181"><dt>**PROP \_ ( \_ identificador de objeto de tipo) \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-181"><dt>**PROP\_TYPE\_OBJECT\_IDENTIFIER**</dt></span></span> </dl>   | <span data-ttu-id="0c484-182">Identificador de objeto SNMP con codificación BER.</span><span class="sxs-lookup"><span data-stu-id="0c484-182">BER-encoded SNMP object identifier.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <span data-ttu-id="0c484-183"><dt>**PROP \_ Type \_ Vines \_ IP \_ Address**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-183"><dt>**PROP\_TYPE\_VINES\_IP\_ADDRESS**</dt></span></span> </dl>     | <span data-ttu-id="0c484-184">Dirección IP de Vines (entidad de 6 bytes).</span><span class="sxs-lookup"><span data-stu-id="0c484-184">Vines IP address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <span data-ttu-id="0c484-185"><dt>**PROP \_ Type \_ var \_ Len \_ Small \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-185"><dt>**PROP\_TYPE\_VAR\_LEN\_SMALL\_INT**</dt></span></span> </dl> | <span data-ttu-id="0c484-186">Valor numérico sin una longitud determinada previamente, pero no más de 8 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="0c484-186">Numeric value without a pre-determined length, but no more than 8 bytes long.</span></span> <span data-ttu-id="0c484-187">La longitud de los datos adjuntos determina la longitud del valor.</span><span class="sxs-lookup"><span data-stu-id="0c484-187">The length of the attached data determines the length of the value.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="0c484-188">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="0c484-188">**DataQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-189">Calificador de datos de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-189">The data qualifier of a property.</span></span> <span data-ttu-id="0c484-190">Este miembro proporciona información precisa sobre el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0c484-190">This member provides precise information about the data type.</span></span>

<span data-ttu-id="0c484-191">El valor de **Qualifier** puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0c484-191">**DataQualifier** can have one of the following values.</span></span>



| <span data-ttu-id="0c484-192">Value</span><span class="sxs-lookup"><span data-stu-id="0c484-192">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="0c484-193">Significado</span><span class="sxs-lookup"><span data-stu-id="0c484-193">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <span data-ttu-id="0c484-194"><dt>**PROP \_ . \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-194"><dt>**PROP\_QUAL\_NONE**</dt></span></span> </dl>                                      | <span data-ttu-id="0c484-195">El tipo de datos de la propiedad es la única especificación de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-195">The property data type is the only specification of the property.</span></span> <br/> <span data-ttu-id="0c484-196">Cuando se establece este valor, el miembro Union de la estructura se establece en **null** y, a continuación, se omite.</span><span class="sxs-lookup"><span data-stu-id="0c484-196">When this value is set, the union member of the structure is set to **NULL**, and then ignored.</span></span><br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <span data-ttu-id="0c484-197"><dt>**PROPal \_ \_ Range**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-197"><dt>**PROP\_QUAL\_RANGE**</dt></span></span> </dl>                                   | <span data-ttu-id="0c484-198">Se espera que el valor numérico esté dentro de un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="0c484-198">The numeric value is expected to be within a given range.</span></span> <span data-ttu-id="0c484-199">Defina el intervalo en el miembro **lpRange** .</span><span class="sxs-lookup"><span data-stu-id="0c484-199">Define the range in the **lpRange** member.</span></span><br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <span data-ttu-id="0c484-200"><dt>**PROPia \_ \_ set**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-200"><dt>**PROP\_QUAL\_SET**</dt></span></span> </dl>                                         | <span data-ttu-id="0c484-201">El valor de una propiedad se compara con un conjunto de valores que se especifican en el miembro **lpSet** de la Unión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="0c484-201">The value of a property is compared to a set of values that are specified in the **lpSet** member of the structure's union.</span></span> <span data-ttu-id="0c484-202">El valor de una propiedad puede ser un **byte**, una **palabra**, un **valor DWORD**, un **LARGEINT** o una **hora**.</span><span class="sxs-lookup"><span data-stu-id="0c484-202">The value of a property can be a **BYTE**, **WORD**, **DWORD**, **LARGEINT** or **TIME**.</span></span><br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <span data-ttu-id="0c484-203"><dt>**PROP \_ . \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-203"><dt>**PROP\_QUAL\_BITFIELD**</dt></span></span> </dl>                          | <span data-ttu-id="0c484-204">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0c484-204">Obsolete.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <span data-ttu-id="0c484-205"><dt>**PROPia con \_ \_ etiqueta \_ establecido**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-205"><dt>**PROP\_QUAL\_LABELED\_SET**</dt></span></span> </dl>                | <span data-ttu-id="0c484-206">El valor de una propiedad se compara con un valor en un conjunto de pares de etiqueta de valor.</span><span class="sxs-lookup"><span data-stu-id="0c484-206">The value of a property is compared to a value in a set of value label pairs.</span></span> <span data-ttu-id="0c484-207">Los pares de etiqueta de valor se especifican en el miembro **lpSet** de la Unión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="0c484-207">The value label pairs are specified in the **lpSet** member of the structure's union.</span></span> <br/> <span data-ttu-id="0c484-208">En el momento de la presentación, si el valor de la propiedad coincide con un valor del conjunto, se muestran tanto un valor como la etiqueta asociada.</span><span class="sxs-lookup"><span data-stu-id="0c484-208">At display time, if the value of the property matches a value in the set, then both a value, and the associated label are displayed.</span></span><br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <span data-ttu-id="0c484-209"><dt>**PROPia con la etiqueta de campo de \_ \_ \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-209"><dt>**PROP\_QUAL\_LABELED\_BITFIELD**</dt></span></span> </dl> | <span data-ttu-id="0c484-210">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0c484-210">Obsolete.</span></span> <span data-ttu-id="0c484-211">\_ \_ En su lugar, use las marcas prop.</span><span class="sxs-lookup"><span data-stu-id="0c484-211">Use PROP\_QUAL\_FLAGS instead.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <span data-ttu-id="0c484-212"><dt>**PROPia \_ \_ const**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-212"><dt>**PROP\_QUAL\_CONST**</dt></span></span> </dl>                                   | <span data-ttu-id="0c484-213">El valor de una propiedad se compara con una constante que se especifica en el miembro de **valor** de la Unión.</span><span class="sxs-lookup"><span data-stu-id="0c484-213">The value of a property is compared to a constant that is specified in the **Value** member of the union.</span></span> <br/> <span data-ttu-id="0c484-214">En el momento de la presentación, si los valores de propiedad y la constante no coinciden, aparece un mensaje de error con formato con el valor establecido como normal.</span><span class="sxs-lookup"><span data-stu-id="0c484-214">At display time, if the property values and constant do not match, a formatted error message appears with the value set as Normal.</span></span><br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <span data-ttu-id="0c484-215"><dt>**marcas PROPn \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-215"><dt>**PROP\_QUAL\_FLAGS**</dt></span></span> </dl>                                   | <span data-ttu-id="0c484-216">El valor de la propiedad se compara con los BITs específicos identificados en el miembro **lpSet** de la Unión.</span><span class="sxs-lookup"><span data-stu-id="0c484-216">The value of the property is compared to specific BITs identified in the **lpSet** member of the union.</span></span><br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <span data-ttu-id="0c484-217"><dt>**PROPy ( \_ \_ matriz)**</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-217"><dt>**PROP\_QUAL\_ARRAY**</dt></span></span> </dl>                                   | <span data-ttu-id="0c484-218">El valor de una propiedad especifica una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="0c484-218">The value of a property specifies an array of values.</span></span> <span data-ttu-id="0c484-219">La longitud de los datos adjuntos determina la longitud de una matriz.</span><span class="sxs-lookup"><span data-stu-id="0c484-219">The length of attached data determines the length of an array.</span></span> <br/> <span data-ttu-id="0c484-220">Cuando se establece el valor de la matriz PROPy \_ \_ , el miembro Union de la estructura de datos **PROPERTYINFO** se establece en **null** y se omite.</span><span class="sxs-lookup"><span data-stu-id="0c484-220">When the PROP\_QUAL\_ARRAY value is set, the union member of the **PROPERTYINFO** data structure is set to **NULL** and ignored.</span></span><br/>                                                    |



 

</dd> <dt>

<span data-ttu-id="0c484-221">**lpExtendedInfo**</span><span class="sxs-lookup"><span data-stu-id="0c484-221">**lpExtendedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-222">Reserved (miembro de Union).</span><span class="sxs-lookup"><span data-stu-id="0c484-222">Reserved (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="0c484-223">**lpRange**</span><span class="sxs-lookup"><span data-stu-id="0c484-223">**lpRange**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-224">Puntero a una estructura de [rango](range.md) que define un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="0c484-224">Pointer to a [RANGE](range.md) structure that defines a range of values.</span></span> <span data-ttu-id="0c484-225">Este miembro debe establecerse si el miembro de **calificador** de la estructura se ha establecido en propness \_ \_ Range (miembro de Union).</span><span class="sxs-lookup"><span data-stu-id="0c484-225">This member must be set if the **DataQualifier** member of this structure is set to PROP\_QUAL\_RANGE (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="0c484-226">**lpSet**</span><span class="sxs-lookup"><span data-stu-id="0c484-226">**lpSet**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-227">Puntero a una estructura de [conjunto](set.md) que especifica un conjunto de valores o etiquetas.</span><span class="sxs-lookup"><span data-stu-id="0c484-227">Pointer to a [SET](set.md) structure that specifies a set of values or labels.</span></span> <span data-ttu-id="0c484-228">Este miembro debe establecerse si el miembro de **calificador** de la estructura se ha establecido en propia \_ \_ Set, propia \_ \_ etiquetada \_ set o props \_ \_ (miembro de Union).</span><span class="sxs-lookup"><span data-stu-id="0c484-228">This member must be set if the **DataQualifier** member of the structure is set to PROP\_QUAL\_SET, PROP\_QUAL\_LABELED\_SET, or PROP\_QUAL\_FLAGS (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="0c484-229">**Máscara**</span><span class="sxs-lookup"><span data-stu-id="0c484-229">**Bitmask**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-230">Obsoleto (miembro de Union).</span><span class="sxs-lookup"><span data-stu-id="0c484-230">Obsolete (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="0c484-231">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0c484-231">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-232">Valor constante que se usa cuando se establece el elemento **Qualifier** en propism \_ \_ const (miembro de Union).</span><span class="sxs-lookup"><span data-stu-id="0c484-232">Constant value used when the **DataQualifier** is set to PROP\_QUAL\_CONST (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="0c484-233">**FormatStringSize**</span><span class="sxs-lookup"><span data-stu-id="0c484-233">**FormatStringSize**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-234">Tamaño máximo que se usa solo para la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-234">Maximum size used only for the property description.</span></span>

</dd> <dt>

<span data-ttu-id="0c484-235">**InstanceData**</span><span class="sxs-lookup"><span data-stu-id="0c484-235">**InstanceData**</span></span>
</dt> <dd>

<span data-ttu-id="0c484-236">Especifique la función de formato a la que se llama para dar formato a los datos mostrados para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c484-236">Specify the format function that is called to format the displayed data for the property.</span></span> <span data-ttu-id="0c484-237">Para usar el formateador genérico, especifique la función **FormatPropertyInstance** .</span><span class="sxs-lookup"><span data-stu-id="0c484-237">To use the generic formatter, specify the **FormatPropertyInstance** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c484-238">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c484-238">Remarks</span></span>

<span data-ttu-id="0c484-239">La estructura **PROPERTYINFO** se utiliza en las llamadas a la función [AddProperty](/previous-versions/bb251873(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="0c484-239">The **PROPERTYINFO** structure is used in calls to the [AddProperty](/previous-versions/bb251873(v=msdn.10)) function.</span></span> <span data-ttu-id="0c484-240">La función **AddProperty** agrega una definición de propiedad única a la [*base de datos de propiedades*](p.md)de analizador.</span><span class="sxs-lookup"><span data-stu-id="0c484-240">The **AddProperty** function adds a single property definition to the parser [*property database*](p.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c484-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c484-241">Requirements</span></span>



| <span data-ttu-id="0c484-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c484-242">Requirement</span></span> | <span data-ttu-id="0c484-243">Value</span><span class="sxs-lookup"><span data-stu-id="0c484-243">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0c484-244">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c484-244">Minimum supported client</span></span><br/> | <span data-ttu-id="0c484-245">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c484-245">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0c484-246">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c484-246">Minimum supported server</span></span><br/> | <span data-ttu-id="0c484-247">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c484-247">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0c484-248">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c484-248">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c484-249"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c484-249"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c484-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c484-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c484-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="0c484-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="0c484-252">VARIEDAD</span><span class="sxs-lookup"><span data-stu-id="0c484-252">RANGE</span></span>](range.md)
</dt> <dt>

[<span data-ttu-id="0c484-253">SET</span><span class="sxs-lookup"><span data-stu-id="0c484-253">SET</span></span>](set.md)
</dt> </dl>

 

