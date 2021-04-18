---
description: Las siguientes constantes de propiedad de dispositivo deben ser compatibles con todas las interfaces de interfaz IWiaItem, IWiaItem2 y IWiaDrvItem, a menos que se indique lo contrario en sus descripciones.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Constantes de propiedad de elementos WIA comunes (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705682"
---
# <a name="common-wia-item-property-constants"></a><span data-ttu-id="4c501-103">Constantes comunes de propiedades de elementos WIA</span><span class="sxs-lookup"><span data-stu-id="4c501-103">Common WIA Item Property Constants</span></span>

<span data-ttu-id="4c501-104">Las siguientes constantes de propiedad de dispositivo deben ser compatibles con todas las interfaces de [interfaz](https://msdn.microsoft.com/library/ms793976.aspx) [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) y IWiaDrvItem, a menos que se indique lo contrario en sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="4c501-104">The following device property constants must be supported by all [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) and [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) interfaces unless otherwise noted in their descriptions.</span></span>

<span data-ttu-id="4c501-105">El prefijo "WIA \_ IPA \_ " indica una propiedad de elemento para todos los dispositivos y es la Convención de nomenclatura que se usa en C/C++.</span><span class="sxs-lookup"><span data-stu-id="4c501-105">The prefix "WIA\_IPA\_" indicates an item property for all devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="4c501-106">Con fines de scripting, estas constantes usan el prefijo "Picture" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="4c501-106">For scripting purposes these constants use the prefix "Picture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="4c501-107">El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="4c501-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4c501-108">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="4c501-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4c501-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c501-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <span data-ttu-id="4c501-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4c501-111">Esta marca controla el acceso al elemento y si se elimina el elemento.</span><span class="sxs-lookup"><span data-stu-id="4c501-111">This flag controls access to the item as well as whether the item is deleted.</span></span><br/> <span data-ttu-id="4c501-112">Se requiere para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-112">Required for all WIA 2.0 items.</span></span><br/> <span data-ttu-id="4c501-113">Tipo: <strong>VT_I4</strong>; Lectura/escritura o solo lectura, dependiendo de la capacidad del elemento de cambiar sus derechos de acceso; Valores válidos: WIA_PROP_FLAG</span><span class="sxs-lookup"><span data-stu-id="4c501-113">Type: <strong>VT_I4</strong>; Read/Write or Read Only, depending on the item's ability to have its access rights changed; Valid values: WIA_PROP_FLAG</span></span><br/> <span data-ttu-id="4c501-114">En la tabla siguiente se muestran las cinco marcas que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-114">The following table has the five flags that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-115">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="4c501-115">Access Right</span></span></th>
<th><span data-ttu-id="4c501-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c501-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-117">WIA_ITEM_READ</span><span class="sxs-lookup"><span data-stu-id="4c501-117">WIA_ITEM_READ</span></span></td>
<td><span data-ttu-id="4c501-118">El elemento tiene acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c501-118">Item has read-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-119">WIA_ITEM_WRITE</span><span class="sxs-lookup"><span data-stu-id="4c501-119">WIA_ITEM_WRITE</span></span></td>
<td><span data-ttu-id="4c501-120">El elemento tiene acceso de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="4c501-120">Item has write-only access.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-121">WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="4c501-121">WIA_ITEM_CAN_BE_DELETED</span></span></td>
<td><span data-ttu-id="4c501-122">El elemento tiene acceso de solo eliminación.</span><span class="sxs-lookup"><span data-stu-id="4c501-122">Item has delete-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-123">WIA_ITEM_RD</span><span class="sxs-lookup"><span data-stu-id="4c501-123">WIA_ITEM_RD</span></span></td>
<td><span data-ttu-id="4c501-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="4c501-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-125">WIA_ITEM_RWD</span><span class="sxs-lookup"><span data-stu-id="4c501-125">WIA_ITEM_RWD</span></span></td>
<td><span data-ttu-id="4c501-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="4c501-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <span data-ttu-id="4c501-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-128">Esta propiedad está reservada para un uso futuro y no se implementa en este momento.</span><span class="sxs-lookup"><span data-stu-id="4c501-128">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="4c501-129">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-129">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <span data-ttu-id="4c501-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-131">Contiene el número de bits por canal para la imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-131">Contains the number of bits per channel for the image.</span></span> <span data-ttu-id="4c501-132">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-132">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-133">Se requiere para todos los elementos de imagen almacenados o habilitados para la adquisición de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-133">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="4c501-134">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-134">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <span data-ttu-id="4c501-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-136">Contiene el tamaño del búfer, en bytes, que se utiliza durante una transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-136">Contains the size of the buffer, in bytes, used during a data transfer.</span></span> <span data-ttu-id="4c501-137">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-137">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-138">Una aplicación puede leer esta propiedad para determinar el tamaño de búfer especificado por el controlador para las transferencias de datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-138">An application can read this property to determine the driver-specified buffer size for data transfers.</span></span> <span data-ttu-id="4c501-139">El servicio WIA también lee esta propiedad para asignar memoria para el minicontrolador durante la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-139">The WIA service also reads this property to allocate memory for the minidriver during the data transfer</span></span></p>
<p><span data-ttu-id="4c501-140">Opcional para todos los elementos de WIA 2,0 habilitados para transferencia.</span><span class="sxs-lookup"><span data-stu-id="4c501-140">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-141">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-141">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="4c501-142">La propiedad <strong>WIA_IPA_BUFFER_SIZE</strong> contiene la cantidad mínima de datos que una aplicación puede solicitar en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="4c501-142">The <strong>WIA_IPA_BUFFER_SIZE</strong> property contains is the minimum amount of data an application can request at any given time.</span></span> <span data-ttu-id="4c501-143">Cuanto mayor sea el tamaño del búfer, mayores serán las solicitudes al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-143">The larger the buffer size, the larger the requests to the device will be.</span></span> <span data-ttu-id="4c501-144">Esto puede hacer que el dispositivo parezca lento y no responda, puede reducir el rendimiento general del sistema y puede consumir demasiados recursos.</span><span class="sxs-lookup"><span data-stu-id="4c501-144">This can make the device seem slow and unresponsive, can slow the overall system performance, and can consume excessive resources.</span></span> <span data-ttu-id="4c501-145">Los tamaños de búfer que son demasiado pequeños pueden reducir el rendimiento de la transferencia de datos al requerir muchas solicitudes más pequeñas.</span><span class="sxs-lookup"><span data-stu-id="4c501-145">Buffer sizes that are too small can slow performance of the data transfer by requiring many smaller requests.</span></span> <span data-ttu-id="4c501-146">Elija un tamaño de búfer razonable teniendo en cuenta el tamaño típico de una solicitud de datos en el dispositivo y equilibre el número de solicitudes con respecto al tamaño de esas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="4c501-146">Choose a reasonable buffer size by considering the typical size of a data request to your device and balancing the number of requests against the size of those requests.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <span data-ttu-id="4c501-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-148">Contiene el número de bytes en una línea de exploración de la imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-148">Contains the number of bytes in one scan line of the image.</span></span> <span data-ttu-id="4c501-149">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-149">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-150">Opcional para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-150">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-151">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-151">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <span data-ttu-id="4c501-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-153">Contiene el número de canales por píxel de la imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-153">Contains the number of channels per pixel for the image.</span></span> <span data-ttu-id="4c501-154">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-154">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-155">Se requiere para todos los elementos de imagen almacenados o habilitados para la adquisición de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-155">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="4c501-156">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-156">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <span data-ttu-id="4c501-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-158">Esta propiedad está reservada para un uso futuro y no se implementa en este momento.</span><span class="sxs-lookup"><span data-stu-id="4c501-158">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="4c501-159">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-159">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <span data-ttu-id="4c501-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-161">Contiene el tipo de compresión actual utilizado.</span><span class="sxs-lookup"><span data-stu-id="4c501-161">Contains the current compression type used.</span></span> <span data-ttu-id="4c501-162">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-162">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-163">Una aplicación Lee esta propiedad para determinar el tipo de compresión de imagen o establece esta propiedad para establecer la configuración de compresión.</span><span class="sxs-lookup"><span data-stu-id="4c501-163">An application reads this property to determine the image compression type or sets this property to configure the compression setting.</span></span></p>
<p><span data-ttu-id="4c501-164">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4c501-164">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4c501-165">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-165">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="4c501-166">El símbolo <strong>V</strong> indica que la constante solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-166">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="4c501-167">(Solo está disponible a través de la interfaz <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="4c501-167">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-168">Tipo de compresión</span><span class="sxs-lookup"><span data-stu-id="4c501-168">Compression Type</span></span></th>
<th><span data-ttu-id="4c501-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c501-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-170">WIA_COMPRESSION_NONE</span><span class="sxs-lookup"><span data-stu-id="4c501-170">WIA_COMPRESSION_NONE</span></span></td>
<td><span data-ttu-id="4c501-171">Sin compresión.</span><span class="sxs-lookup"><span data-stu-id="4c501-171">No compression.</span></span> <span data-ttu-id="4c501-172">Vea la <strong>Nota</strong> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4c501-172">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-173">WIA_COMPRESSION_AUTO</span><span class="sxs-lookup"><span data-stu-id="4c501-173">WIA_COMPRESSION_AUTO</span></span></td>
<td><span data-ttu-id="4c501-174">Modo de compresión automática.</span><span class="sxs-lookup"><span data-stu-id="4c501-174">Automatic compression mode.</span></span> <span data-ttu-id="4c501-175">Vea la <strong>Nota</strong> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4c501-175">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-176">WIA_COMPRESSION_BI_RLE4</span><span class="sxs-lookup"><span data-stu-id="4c501-176">WIA_COMPRESSION_BI_RLE4</span></span></td>
<td><span data-ttu-id="4c501-177">Compresión RLE4</span><span class="sxs-lookup"><span data-stu-id="4c501-177">RLE4 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-178">WIA_COMPRESSION_BI_RLE8</span><span class="sxs-lookup"><span data-stu-id="4c501-178">WIA_COMPRESSION_BI_RLE8</span></span></td>
<td><span data-ttu-id="4c501-179">Compresión RLE8</span><span class="sxs-lookup"><span data-stu-id="4c501-179">RLE8 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-180">WIA_COMPRESSION_G3</span><span class="sxs-lookup"><span data-stu-id="4c501-180">WIA_COMPRESSION_G3</span></span></td>
<td><span data-ttu-id="4c501-181">Compresión de grupo 3</span><span class="sxs-lookup"><span data-stu-id="4c501-181">Group 3 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-182">WIA_COMPRESSION_G4</span><span class="sxs-lookup"><span data-stu-id="4c501-182">WIA_COMPRESSION_G4</span></span></td>
<td><span data-ttu-id="4c501-183">Compresión de grupo 4</span><span class="sxs-lookup"><span data-stu-id="4c501-183">Group 4 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-184">WIA_COMPRESSION_JPEG</span><span class="sxs-lookup"><span data-stu-id="4c501-184">WIA_COMPRESSION_JPEG</span></span></td>
<td><span data-ttu-id="4c501-185">Compresión JPEG.</span><span class="sxs-lookup"><span data-stu-id="4c501-185">JPEG compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-186">WIA_COMPRESSION_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-186">WIA_COMPRESSION_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-187">Compresión JBIG.</span><span class="sxs-lookup"><span data-stu-id="4c501-187">JBIG compression.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-189">Compresión JPEG 2000.</span><span class="sxs-lookup"><span data-stu-id="4c501-189">JPEG 2000 compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-190">WIA_COMPRESSION_PNG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-190">WIA_COMPRESSION_PNG<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-191">Compresión PNG.</span><span class="sxs-lookup"><span data-stu-id="4c501-191">PNG compression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="4c501-192">Cuando se WIA_COMPRESSION_NONE esta propiedad y WIA_IPA_FORMAT es WiaImgFmt_PDFA o WiaImgFmt_XPS; a continuación, WIA_COMPRESSION_NONE significa que el modo de compresión es indefinido y el escáner debe decidir en un modo.</span><span class="sxs-lookup"><span data-stu-id="4c501-192">When this property is WIA_COMPRESSION_NONE, and WIA_IPA_FORMAT is either WiaImgFmt_PDFA or WiaImgFmt_XPS; then WIA_COMPRESSION_NONE means that the compression mode is undefined and the scanner must decide on a mode.</span></span></p>
<p><span data-ttu-id="4c501-193">WIA_COMPRESSION_AUTO es un nuevo valor de propiedad definido para la propiedad WIA_IPA_COMPRESSION.</span><span class="sxs-lookup"><span data-stu-id="4c501-193">WIA_COMPRESSION_AUTO is a new property value defined for the WIA_IPA_COMPRESSION property.</span></span> <span data-ttu-id="4c501-194">Este valor es válido para todos los elementos de origen de datos de imagen programables, incluidos el plano y el alimentador.</span><span class="sxs-lookup"><span data-stu-id="4c501-194">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="4c501-195">Cuando este valor es compatible con el controlador mini de WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_COMPRESSION para habilitar la detección automática del modo de compresión en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-195">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_COMPRESSION in order to enable automatic compression mode detection at the device.</span></span> <span data-ttu-id="4c501-196">WIA_COMPRESSION_AUTO puede trabajar con y sin que se admita o se habilite el color automático completo (WIA_DATA_AUTO y WIA_DEPTH_AUTO).</span><span class="sxs-lookup"><span data-stu-id="4c501-196">WIA_COMPRESSION_AUTO can work with and without full auto-color being supported or enabled (WIA_DATA_AUTO and WIA_DEPTH_AUTO).</span></span></p>
<p><span data-ttu-id="4c501-197">WIA_COMPRESSION_AUTO es muy útil con formatos de archivo de transferencia que admiten varios tipos de datos y profundidades de bits, como WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="4c501-197">WIA_COMPRESSION_AUTO is most useful with transfer file formats that support multiple data types and bit depths, such as WiaImgFmt_RAW.</span></span> <span data-ttu-id="4c501-198">Para obtener más información acerca de los formatos de archivo de transferencia, consulte WIA_IPA_FORMAT en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="4c501-198">For more information about transfer file formats, see WIA_IPA_FORMAT in this table.</span></span></p>
<p><span data-ttu-id="4c501-199">Es opitonal que el mini-driver de WIA compatibilidad con WIA_COMPRESSION_AUTO.</span><span class="sxs-lookup"><span data-stu-id="4c501-199">It is opitonal for the WIA mini-driver to suport WIA_COMPRESSION_AUTO.</span></span> <span data-ttu-id="4c501-200">Cuando se admite, el mini controlador WIA nunca debe establecerlo como valor predeterminado para WIA_IPA_COMPRESSION; solo la aplicación WIA puede establecer este valor.</span><span class="sxs-lookup"><span data-stu-id="4c501-200">When it is supported, the WIA mini-driver must never set it as the default value for WIA_IPA_COMPRESSION; only the WIA application can set this value.</span></span></p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <span data-ttu-id="4c501-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-202">Contiene la configuración de tipo de datos actual para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-202">Contains the current data type setting for the device.</span></span> <span data-ttu-id="4c501-203">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-203">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-204">Una aplicación Lee esta propiedad para determinar el tipo de datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-204">An application reads this property to determine the data type of the image.</span></span> <span data-ttu-id="4c501-205">Una aplicación escribe esta propiedad para establecer el tipo de datos actual de la imagen que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="4c501-205">An application writes this property to set the current data type of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="4c501-206">Esta propiedad es necesaria para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-206">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="4c501-207">Debe ser de lectura y escritura para todos los elementos habilitados para adquisición de WIA 2,0 y solo lectura para los elementos de almacenamiento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-207">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="4c501-208">Tipo: <strong>VT_I4</strong>; Acceso para los sistemas operativos anteriores a Windows Vista: esta propiedad es de solo lectura para cámaras y lectura/escritura para escáneres; Acceso para Windows Vista y versiones posteriores: esta propiedad es de solo lectura para los elementos de WIA_CATEGORY_FOLDER y WIA_CATEGORY_FINISHED_FILE, y de lectura y escritura para todas las demás categorías de elementos de WIA 2,0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4c501-208">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: This property is Read Only for cameras and Read/Write for scanners; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4c501-209">En la tabla siguiente se incluyen las seis constantes que son válidas con cuando <strong>WIA_IPA_FORMAT</strong> no se establece en WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="4c501-209">The following table has the six constants that are valid with when <strong>WIA_IPA_FORMAT</strong> is not set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-210">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4c501-210">Data Type</span></span></th>
<th><span data-ttu-id="4c501-211">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c501-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-212">WIA_DATA_AUTO</span><span class="sxs-lookup"><span data-stu-id="4c501-212">WIA_DATA_AUTO</span></span></td>
<td><span data-ttu-id="4c501-213">Válido para todos los elementos de origen de datos de imagen programables, incluidos el plano y el alimentador.</span><span class="sxs-lookup"><span data-stu-id="4c501-213">Valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="4c501-214">Cuando este valor es compatible con el controlador mini de WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_DATATYPE para habilitar la detección automática de colores en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-214">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DATATYPE in order to enable automatic color detection at the device.</span></span> <span data-ttu-id="4c501-215">Cuando se establece WIA_DATA_AUTO, el controlador mini de WIA debe actualizar WIA_IPA_DEPTH en el mismo elemento para WIA_DEPTH_AUTO (que debe ser un valor compatible Si el dispositivo admite el color automático).</span><span class="sxs-lookup"><span data-stu-id="4c501-215">When WIA_DATA_AUTO is set, the WIA mini-driver must update WIA_IPA_DEPTH on the same item to WIA_DEPTH_AUTO (which must be a supported value if the device supports automatic color).</span></span><br/> <span data-ttu-id="4c501-216">Este es un valor opcional, pero es necesario cuando WIA_DEPTH_AUTO es compatible con WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="4c501-216">This is an optional value, but it is required when WIA_DEPTH_AUTO is supported for WIA_IPA_DEPTH.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-217">WIA_DATA_COLOR</span><span class="sxs-lookup"><span data-stu-id="4c501-217">WIA_DATA_COLOR</span></span></td>
<td><span data-ttu-id="4c501-218">Los datos de digitalización son de color rojo, verde y azul (RGB).</span><span class="sxs-lookup"><span data-stu-id="4c501-218">Scan data is red, green, blue (RGB) color.</span></span> <span data-ttu-id="4c501-219">El formato de color completo se describe mediante las siguientes propiedades de WIA: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-219">The full color format is described using the following WIA properties: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span></span><br/> <span data-ttu-id="4c501-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span></span><br/> <span data-ttu-id="4c501-221"><strong>WIA_IPA_PLANAR</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-221"><strong>WIA_IPA_PLANAR</strong></span></span><br/> <span data-ttu-id="4c501-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span></span><br/> <span data-ttu-id="4c501-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span></span><br/> <span data-ttu-id="4c501-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-225">WIA_DATA_COLOR_DITHER</span><span class="sxs-lookup"><span data-stu-id="4c501-225">WIA_DATA_COLOR_DITHER</span></span></td>
<td><span data-ttu-id="4c501-226">Igual que WIA_DATA_COLOR con la diferencia de que los datos se han interpolado mediante el patrón de interpolación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="4c501-226">Same as WIA_DATA_COLOR except that the data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-227">WIA_DATA_COLOR_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="4c501-227">WIA_DATA_COLOR_THRESHOLD</span></span></td>
<td><span data-ttu-id="4c501-228">Igual que WIA_DATA_COLOR, salvo que el valor de umbral se usa al examinar los datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-228">Same as WIA_DATA_COLOR except that the threshold value is used when scanning the data.</span></span> <span data-ttu-id="4c501-229">Los valores de color sobre el valor de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> se convierten al brillo completo; los colores que se encuentran debajo de este valor se convierten a negro.</span><span class="sxs-lookup"><span data-stu-id="4c501-229">Color values over the <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> value are converted to full brightness; colors under this value are converted to black.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-230">WIA_DATA_DITHER</span><span class="sxs-lookup"><span data-stu-id="4c501-230">WIA_DATA_DITHER</span></span></td>
<td><span data-ttu-id="4c501-231">Los datos de recorrido se comparan con el patrón de interpolación seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="4c501-231">Scan data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-232">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="4c501-232">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="4c501-233">Examinar datos representa la intensidad.</span><span class="sxs-lookup"><span data-stu-id="4c501-233">Scan data represents intensity.</span></span> <span data-ttu-id="4c501-234">La paleta es una escala de grises fija y equidistante con una profundidad especificada por <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-234">The palette is a fixed, equally-spaced gray scale with a depth specified by <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-235">WIA_DATA_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="4c501-235">WIA_DATA_THRESHOLD</span></span></td>
<td><span data-ttu-id="4c501-236">El umbral es un bit por píxel de datos en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="4c501-236">The threshold is one bit per pixel of black-and-white data.</span></span> <span data-ttu-id="4c501-237">Los datos sobre el valor actual de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> se convierten a blanco; los datos con este valor se convierten a negro.</span><span class="sxs-lookup"><span data-stu-id="4c501-237">Data over the current value of <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> is converted to white; data under this value is converted to black.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="4c501-238">La propiedad <strong>WIA_IPA_DATATYPE</strong> también se usa para describir el tipo de transferencia de datos sin procesar que se va a utilizar cuando la aplicación establece WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="4c501-238">The <strong>WIA_IPA_DATATYPE</strong> property is also used to describe the type of RAW data transfer to be used when the application sets WiaImgFmt_RAW.</span></span> <span data-ttu-id="4c501-239">El controlador debe establecer la propiedad <strong>WIA_IPA_DATATYPE</strong> en una lista de valores permitidos de los que la aplicación puede elegir uno.</span><span class="sxs-lookup"><span data-stu-id="4c501-239">The driver should set the <strong>WIA_IPA_DATATYPE</strong> property to a list of allowed values from which the application can pick one.</span></span></p>
<p><span data-ttu-id="4c501-240">Si el dispositivo se puede establecer en un solo valor, cree un tipo de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> y coloque el valor válido en él.</span><span class="sxs-lookup"><span data-stu-id="4c501-240">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="4c501-241">Compruebe la propiedad <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> para determinar la profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="4c501-241">Check the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property to determine the bit depth.</span></span> <span data-ttu-id="4c501-242">Esta propiedad normalmente contiene un valor único para las cámaras.</span><span class="sxs-lookup"><span data-stu-id="4c501-242">This property usually contains a single value for cameras.</span></span></p>
<p><span data-ttu-id="4c501-243">En la tabla siguiente se enumeran las constantes válidas con <strong>WIA_IPA_DATATYPE</strong> cuando <strong>WIA_IPA_FORMAT</strong> está establecido en WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="4c501-243">The following table lists the constants that are valid with <strong>WIA_IPA_DATATYPE</strong> when <strong>WIA_IPA_FORMAT</strong> is set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-244">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4c501-244">Data Type</span></span></th>
<th><span data-ttu-id="4c501-245">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c501-245">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-246">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="4c501-246">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="4c501-247">Examinar datos representa la intensidad.</span><span class="sxs-lookup"><span data-stu-id="4c501-247">Scan data represents intensity.</span></span> <span data-ttu-id="4c501-248">La paleta es una escala de grises fija y equidistante con una profundidad especificada por la propiedad <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> .</span><span class="sxs-lookup"><span data-stu-id="4c501-248">The palette is a fixed, equally spaced grayscale with a depth specified by the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span> <span data-ttu-id="4c501-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="4c501-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-250">WIA_DATA_RAW_BGR</span><span class="sxs-lookup"><span data-stu-id="4c501-250">WIA_DATA_RAW_BGR</span></span></td>
<td><span data-ttu-id="4c501-251">Los datos de recorrido están en el ColorSpace de BGR (Blue-Green-red).</span><span class="sxs-lookup"><span data-stu-id="4c501-251">Scan data is in the BGR (blue-green-red) colorspace.</span></span> <span data-ttu-id="4c501-252">El formato de color completo se describe mediante followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span><span class="sxs-lookup"><span data-stu-id="4c501-252">The full color format is described using the followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span></span><br/> <span data-ttu-id="4c501-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span><span class="sxs-lookup"><span data-stu-id="4c501-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span></span><br/> <span data-ttu-id="4c501-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span></span><br/> <span data-ttu-id="4c501-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span></span><br/> <span data-ttu-id="4c501-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span><span class="sxs-lookup"><span data-stu-id="4c501-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span></span><br/> <span data-ttu-id="4c501-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.</span><span class="sxs-lookup"><span data-stu-id="4c501-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-258">WIA_DATA_RAW_CMY</span><span class="sxs-lookup"><span data-stu-id="4c501-258">WIA_DATA_RAW_CMY</span></span></td>
<td><span data-ttu-id="4c501-259">Los datos de recorrido están en el ColorSpace cian-fucsia-amarillo (CMY).</span><span class="sxs-lookup"><span data-stu-id="4c501-259">Scan data is in the cyan-magenta-yellow (CMY) colorspace.</span></span> <span data-ttu-id="4c501-260">El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="4c501-260">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="4c501-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.</span><span class="sxs-lookup"><span data-stu-id="4c501-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-262">WIA_DATA_RAW_CMYK</span><span class="sxs-lookup"><span data-stu-id="4c501-262">WIA_DATA_RAW_CMYK</span></span></td>
<td><span data-ttu-id="4c501-263">Los datos de recorrido están en el ColorSpace cian-magenta-amarillo-negro (CMYK).</span><span class="sxs-lookup"><span data-stu-id="4c501-263">Scan data is in the cyan-magenta-yellow-black (CMYK) colorspace.</span></span> <span data-ttu-id="4c501-264">El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="4c501-264">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="4c501-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 4.</span><span class="sxs-lookup"><span data-stu-id="4c501-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-266">WIA_DATA_RAW_RGB</span><span class="sxs-lookup"><span data-stu-id="4c501-266">WIA_DATA_RAW_RGB</span></span></td>
<td><span data-ttu-id="4c501-267">Los datos de recorrido están en el ColorSpace rojo-verde-azul (RGB).</span><span class="sxs-lookup"><span data-stu-id="4c501-267">Scan data is in the red-green-blue (RGB) colorspace.</span></span> <span data-ttu-id="4c501-268">El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="4c501-268">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="4c501-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.</span><span class="sxs-lookup"><span data-stu-id="4c501-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-270">WIA_DATA_RAW_YUV</span><span class="sxs-lookup"><span data-stu-id="4c501-270">WIA_DATA_RAW_YUV</span></span></td>
<td><span data-ttu-id="4c501-271">Los datos de análisis están en el ColorSpace de luminancia: diferencia de azul: diferencia roja (YUV).</span><span class="sxs-lookup"><span data-stu-id="4c501-271">Scan data is in the luminance-blue difference-red difference (YUV) colorspace.</span></span> <span data-ttu-id="4c501-272">El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="4c501-272">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="4c501-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.</span><span class="sxs-lookup"><span data-stu-id="4c501-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-274">WIA_DATA_RAW_YUVK</span><span class="sxs-lookup"><span data-stu-id="4c501-274">WIA_DATA_RAW_YUVK</span></span></td>
<td><span data-ttu-id="4c501-275">Los datos de análisis están en la luminancia: diferencia de azul, diferencia de color rojo y negro (YUVK) ColorSpace.</span><span class="sxs-lookup"><span data-stu-id="4c501-275">Scan data is in the luminance-blue difference-red difference-black (YUVK) colorspace.</span></span> <span data-ttu-id="4c501-276">El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="4c501-276">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="4c501-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 4.</span><span class="sxs-lookup"><span data-stu-id="4c501-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <span data-ttu-id="4c501-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-279">WIA_IPA_DEPTH contiene el valor de profundidad de bits de una imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-279">WIA_IPA_DEPTH Contains the bit depth setting of an image.</span></span> <span data-ttu-id="4c501-280">El minicontrolador crea y mantiene esta propiedad. Una aplicación Lee esta propiedad para determinar el valor de profundidad de bits de la imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-280">The minidriver creates and maintains this property.An application reads this property to determine the bit depth setting of the image.</span></span> <span data-ttu-id="4c501-281">Es posible que la aplicación también pueda establecer este valor en la profundidad de bits deseada.</span><span class="sxs-lookup"><span data-stu-id="4c501-281">The application might also be able to set this value to the desired bit depth.</span></span></p>
<p><span data-ttu-id="4c501-282">Si el dispositivo se puede establecer en un solo valor, cree un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo y coloque el valor válido en él.</span><span class="sxs-lookup"><span data-stu-id="4c501-282">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="4c501-283">Esta propiedad es necesaria para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-283">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="4c501-284">Debe ser de lectura y escritura para todos los elementos habilitados para adquisición de WIA 2,0 y solo lectura para los elementos de almacenamiento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-284">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="4c501-285">Tipo: <strong>VT_I4</strong>; Acceso para los sistemas operativos anteriores a Windows Vista: lectura y escritura; Acceso para Windows Vista y versiones posteriores: esta propiedad es de solo lectura para los elementos de WIA_CATEGORY_FOLDER y WIA_CATEGORY_FINISHED_FILE, y de lectura y escritura para todas las demás categorías de elementos de WIA 2,0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4c501-285">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: Read/Write; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4c501-286">WIA_DEPTH_AUTO se define como 0 bits por píxel y es un nuevo valor de propiedad definido para la WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="4c501-286">WIA_DEPTH_AUTO is defined as 0 bits per pixel, and it is a new property value defined for the WIA_IPA_DEPTH.</span></span> <span data-ttu-id="4c501-287">Este valor es válido para todos los elementos de origen de datos de imagen programables, incluidos el plano y el alimentador.</span><span class="sxs-lookup"><span data-stu-id="4c501-287">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="4c501-288">Cuando WIA_DEPTH_AUTO es compatible con el controlador mini de WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_DEPTH en este valor para habilitar la detección automática de colores en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-288">When WIA_DEPTH_AUTO is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DEPTH to this value, to enable automatic color detection at the device.</span></span> <span data-ttu-id="4c501-289">Cuando se establece WIA_DEPTH_AUTO, el mini controlador WIA debe actualizar WIA_IPA_DATATYPE en el mismo elemento para WIA_DATA_AUTO (que debe ser un valor compatible, si el dispositivo admite el color automático).</span><span class="sxs-lookup"><span data-stu-id="4c501-289">When WIA_DEPTH_AUTO is set, the WIA mini-driver must update WIA_IPA_DATATYPE on the same item to WIA_DATA_AUTO (which must be a supported value, if the device supports automatic color).</span></span></p>
<p><span data-ttu-id="4c501-290">WIA_DEPTH_AUTO es un valor opcional, pero se requiere cuando se admite WIA_DATA_AUTO para WIA_IPA_DATATYPE.</span><span class="sxs-lookup"><span data-stu-id="4c501-290">WIA_DEPTH_AUTO is an optional value, but it becomes required when WIA_DATA_AUTO is supported for WIA_IPA_DATATYPE.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <span data-ttu-id="4c501-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-292">Contiene la extensión de nombre de archivo para un formato de archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="4c501-292">Contains the file name extension for a particular file format.</span></span> <span data-ttu-id="4c501-293">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-293">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-294">Opcional para todos los elementos de WIA 2,0 habilitados para transferencia.</span><span class="sxs-lookup"><span data-stu-id="4c501-294">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-295">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-295">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="4c501-296">El controlador actualiza esta propiedad para reflejar el valor actual de la propiedad <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</span><span class="sxs-lookup"><span data-stu-id="4c501-296">The driver updates this property to reflect the current value of the <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> property.</span></span></p>
<p><span data-ttu-id="4c501-297">Por ejemplo, si se WiaImgFmt_JPEG <strong>WIA_IPA_FORMAT</strong> , <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> debe ser <strong>jpg</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c501-297">For example, if <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_JPEG, then <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> should be <strong>jpg</strong>.</span></span> <span data-ttu-id="4c501-298">Si <strong>WIA_IPA_FORMAT</strong> es WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION debe ser BMP.</span><span class="sxs-lookup"><span data-stu-id="4c501-298">If <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_BMP, then WIA_IPA_FILENAME_EXTENSION should be BMP.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="4c501-299">La extensión de nombre de archivo no incluye el punto.</span><span class="sxs-lookup"><span data-stu-id="4c501-299">The file name extension does not include the dot.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="4c501-300">Esta propiedad se recomienda para los controladores que admiten formatos estándar y es necesario para los controladores que implementan formatos definidos de forma personalizada.</span><span class="sxs-lookup"><span data-stu-id="4c501-300">This property is recommended for drivers that support standard formats and is required for drivers that implement custom-defined formats.</span></span> <span data-ttu-id="4c501-301">Informa a la aplicación de la extensión de nombre de archivo correcta que se va a usar durante la transferencia de archivos con formato privado.</span><span class="sxs-lookup"><span data-stu-id="4c501-301">It informs the application of the correct file name extension to use during the transfer of privately formatted files.</span></span> <span data-ttu-id="4c501-302">Por ejemplo, si A. Datum Corporation creó un controlador WIA que transfirió un archivo en un formato nuevo, la compañía podría especificar una extensión de &quot; ADC &quot; .</span><span class="sxs-lookup"><span data-stu-id="4c501-302">For example, if the A. Datum Corporation created a WIA driver that transferred a file in a new format, the company could specify an extension of &quot;adc&quot;.</span></span> <span data-ttu-id="4c501-303">Esto permite a las aplicaciones transferir datos en ese formato a un archivo y crear un nombre de archivo como, por ejemplo, <em>archivo. ADC</em>, que es útil para otras personas que entienden la nueva extensión.</span><span class="sxs-lookup"><span data-stu-id="4c501-303">This allows applications to transfer data in that format to a file and to create a file name such as <em>myfile.adc</em>,which is useful to others who understand the new extension.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <span data-ttu-id="4c501-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-305">Contiene el formato actual de la imagen que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="4c501-305">Contains the current format of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="4c501-306">Una aplicación Lee esta propiedad para determinar el formato de la imagen que va a recibir.</span><span class="sxs-lookup"><span data-stu-id="4c501-306">An application reads this property to determine the format of the image that it is about to receive.</span></span> <span data-ttu-id="4c501-307">Una aplicación escribe esta propiedad para establecer el formato.</span><span class="sxs-lookup"><span data-stu-id="4c501-307">An application writes this property to set the format.</span></span> <span data-ttu-id="4c501-308">Esta propiedad depende de la propiedad <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> .</span><span class="sxs-lookup"><span data-stu-id="4c501-308">This property depends on the <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> property.</span></span> <span data-ttu-id="4c501-309">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-309">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-310">Si el dispositivo se puede establecer en un solo valor, cree un tipo de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> y coloque el valor válido en él.</span><span class="sxs-lookup"><span data-stu-id="4c501-310">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="4c501-311">Tipo: <strong>CLSID</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4c501-311">Type: <strong>CLSID</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4c501-312">En la tabla siguiente se enumeran las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-312">The following table lists the constants that are valid with this property.</span></span> <span data-ttu-id="4c501-313">El asterisco \* indica que la constante no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4c501-313">The asterisk \* indicates that the constant is not supported in Windows Vista.</span></span> <span data-ttu-id="4c501-314">(Solo está disponible a través de la interfaz <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> ). El doble asterisco \* \* indica que la constante no se admite en Windows Server 2003 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4c501-314">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) The double asterisk \*\* indicates that the constant is not supported in either Windows Server 2003 or Windows Vista.</span></span> <span data-ttu-id="4c501-315">El símbolo <strong>V</strong> indica que la constante solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-315">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="4c501-316">(Solo está disponible a través de la interfaz <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="4c501-316">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-317">Formato</span><span class="sxs-lookup"><span data-stu-id="4c501-317">Format</span></span></th>
<th><span data-ttu-id="4c501-318">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c501-318">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-319">WiaAudFmt_AIFF</span><span class="sxs-lookup"><span data-stu-id="4c501-319">WiaAudFmt_AIFF</span></span></td>
<td><span data-ttu-id="4c501-320">Formato de audio AIFF</span><span class="sxs-lookup"><span data-stu-id="4c501-320">AIFF audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-321">WiaAudFmt_MP3</span><span class="sxs-lookup"><span data-stu-id="4c501-321">WiaAudFmt_MP3</span></span></td>
<td><span data-ttu-id="4c501-322">Formato de audio MP3</span><span class="sxs-lookup"><span data-stu-id="4c501-322">MP3 audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-323">WiaAudFmt_WAV</span><span class="sxs-lookup"><span data-stu-id="4c501-323">WiaAudFmt_WAV</span></span></td>
<td><span data-ttu-id="4c501-324">Formato de audio WAV</span><span class="sxs-lookup"><span data-stu-id="4c501-324">WAV audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-325">WiaAudFmt_WMA</span><span class="sxs-lookup"><span data-stu-id="4c501-325">WiaAudFmt_WMA</span></span></td>
<td><span data-ttu-id="4c501-326">Formato de audio WMA</span><span class="sxs-lookup"><span data-stu-id="4c501-326">WMA audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-327">WiaImgFmt_ASF \* \*</span><span class="sxs-lookup"><span data-stu-id="4c501-327">WiaImgFmt_ASF\*\*</span></span></td>
<td><span data-ttu-id="4c501-328">Formato de vídeo ASF</span><span class="sxs-lookup"><span data-stu-id="4c501-328">ASF video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-329">WiaImgFmt_AVI \* \*</span><span class="sxs-lookup"><span data-stu-id="4c501-329">WiaImgFmt_AVI\*\*</span></span></td>
<td><span data-ttu-id="4c501-330">Formato de vídeo AVI</span><span class="sxs-lookup"><span data-stu-id="4c501-330">AVI video format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-331">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="4c501-331">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="4c501-332">Mapa de bits de Windows con un archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="4c501-332">Windows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-333">WiaImgFmt_CIFF \*</span><span class="sxs-lookup"><span data-stu-id="4c501-333">WiaImgFmt_CIFF\*</span></span></td>
<td><span data-ttu-id="4c501-334">Formato de archivo de imagen de cámara</span><span class="sxs-lookup"><span data-stu-id="4c501-334">Camera Image File format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-335">WiaImgFmt_DPOF</span><span class="sxs-lookup"><span data-stu-id="4c501-335">WiaImgFmt_DPOF</span></span></td>
<td><span data-ttu-id="4c501-336">Formato de impresión DPOF</span><span class="sxs-lookup"><span data-stu-id="4c501-336">DPOF printing format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-337">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="4c501-337">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="4c501-338">Metarchivo extendido de Windows</span><span class="sxs-lookup"><span data-stu-id="4c501-338">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-339">WiaImgFmt_EXEC</span><span class="sxs-lookup"><span data-stu-id="4c501-339">WiaImgFmt_EXEC</span></span></td>
<td><span data-ttu-id="4c501-340">Archivo ejecutable</span><span class="sxs-lookup"><span data-stu-id="4c501-340">Executable file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-341">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="4c501-341">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="4c501-342">Formato de archivo intercambiable</span><span class="sxs-lookup"><span data-stu-id="4c501-342">Exchangeable File Format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-343">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="4c501-343">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="4c501-344">Formato FlashPix</span><span class="sxs-lookup"><span data-stu-id="4c501-344">FlashPix format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-345">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="4c501-345">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="4c501-346">Formato de imagen GIF</span><span class="sxs-lookup"><span data-stu-id="4c501-346">GIF image format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-347">WiaImgFmt_HTML</span><span class="sxs-lookup"><span data-stu-id="4c501-347">WiaImgFmt_HTML</span></span></td>
<td><span data-ttu-id="4c501-348">Formato HTML</span><span class="sxs-lookup"><span data-stu-id="4c501-348">HTML format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-349">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="4c501-349">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="4c501-350">Formato de archivo de icono de Windows</span><span class="sxs-lookup"><span data-stu-id="4c501-350">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-351">WiaImgFmt_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-351">WiaImgFmt_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-352">El formato Joint-LEVEL Experts Group (JBIG).</span><span class="sxs-lookup"><span data-stu-id="4c501-352">The Joint Bi-level Image Experts Group (JBIG) format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-353">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="4c501-353">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="4c501-354">Formato comprimido JPEG</span><span class="sxs-lookup"><span data-stu-id="4c501-354">JPEG compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-355">WiaImgFmt_JPEG2K</span><span class="sxs-lookup"><span data-stu-id="4c501-355">WiaImgFmt_JPEG2K</span></span></td>
<td><span data-ttu-id="4c501-356">Formato comprimido JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="4c501-356">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-357">WiaImgFmt_JPEG2KX</span><span class="sxs-lookup"><span data-stu-id="4c501-357">WiaImgFmt_JPEG2KX</span></span></td>
<td><span data-ttu-id="4c501-358">Formato comprimido JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="4c501-358">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-359">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="4c501-359">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="4c501-360">Mapa de bits de Windows sin un archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="4c501-360">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-361">WiaImgFmt_PDFA<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-361">WiaImgFmt_PDFA<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-362">Formato PDF/A (ISO/CD 19005-1).</span><span class="sxs-lookup"><span data-stu-id="4c501-362">The PDF/A (ISO/CD 19005-1) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-363">WiaImgFmt_MPG \* \*</span><span class="sxs-lookup"><span data-stu-id="4c501-363">WiaImgFmt_MPG\*\*</span></span></td>
<td><span data-ttu-id="4c501-364">Formato de vídeo MPEG</span><span class="sxs-lookup"><span data-stu-id="4c501-364">MPEG video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-365">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="4c501-365">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="4c501-366">Formato de archivo de Eastman Kodak</span><span class="sxs-lookup"><span data-stu-id="4c501-366">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-367">WiaImgFmt_PICT</span><span class="sxs-lookup"><span data-stu-id="4c501-367">WiaImgFmt_PICT</span></span></td>
<td><span data-ttu-id="4c501-368">Formato de archivo de Apple</span><span class="sxs-lookup"><span data-stu-id="4c501-368">Apple file format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-369">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="4c501-369">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="4c501-370">Formato PNG de W3C</span><span class="sxs-lookup"><span data-stu-id="4c501-370">W3C PNG format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-371">WiaImgFmt_RAW</span><span class="sxs-lookup"><span data-stu-id="4c501-371">WiaImgFmt_RAW</span></span></td>
<td><span data-ttu-id="4c501-372">Formato RAW solo para transferencias de datos</span><span class="sxs-lookup"><span data-stu-id="4c501-372">Raw format for data transfers only</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-373">WiaImgFmt_RAWRGB</span><span class="sxs-lookup"><span data-stu-id="4c501-373">WiaImgFmt_RAWRGB</span></span></td>
<td><span data-ttu-id="4c501-374">Formato RGB sin formato</span><span class="sxs-lookup"><span data-stu-id="4c501-374">Raw RGB format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-375">WiaImgFmt_RTF</span><span class="sxs-lookup"><span data-stu-id="4c501-375">WiaImgFmt_RTF</span></span></td>
<td><span data-ttu-id="4c501-376">Formato de archivo de texto enriquecido</span><span class="sxs-lookup"><span data-stu-id="4c501-376">Rich Text File format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-377">WiaImgFmt_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="4c501-377">WiaImgFmt_SCRIPT</span></span></td>
<td><span data-ttu-id="4c501-378">Archivo de script</span><span class="sxs-lookup"><span data-stu-id="4c501-378">Script file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-379">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="4c501-379">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="4c501-380">Formato TIFF</span><span class="sxs-lookup"><span data-stu-id="4c501-380">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-381">WiaImgFmt_TXT</span><span class="sxs-lookup"><span data-stu-id="4c501-381">WiaImgFmt_TXT</span></span></td>
<td><span data-ttu-id="4c501-382">Archivo de texto</span><span class="sxs-lookup"><span data-stu-id="4c501-382">Text file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-383">WiaImgFmt_UNICODE16</span><span class="sxs-lookup"><span data-stu-id="4c501-383">WiaImgFmt_UNICODE16</span></span></td>
<td><span data-ttu-id="4c501-384">Codificación Unicode de 16 bits</span><span class="sxs-lookup"><span data-stu-id="4c501-384">UNICODE 16-bit encoding</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-385">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="4c501-385">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="4c501-386">Metarchivo de Windows</span><span class="sxs-lookup"><span data-stu-id="4c501-386">Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-387">WiaImgFmt_XML</span><span class="sxs-lookup"><span data-stu-id="4c501-387">WiaImgFmt_XML</span></span></td>
<td><span data-ttu-id="4c501-388">Archivo XML</span><span class="sxs-lookup"><span data-stu-id="4c501-388">XML file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-389">WiaImgFmt_XPS<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-389">WiaImgFmt_XPS<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-390">Formato de paquete XPS</span><span class="sxs-lookup"><span data-stu-id="4c501-390">XPS Package format</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="4c501-391">Cuando esta propiedad es WiaImgFmt_PDFA o WiaImgFmt_XPS y WIA_IPA_COMPRESSION es WIA_COMPRESSION_NONE; después, el último valor significa que el modo de compresión es indefinido y el escáner debe decidir en un modo.</span><span class="sxs-lookup"><span data-stu-id="4c501-391">When this property is either WiaImgFmt_PDFA or WiaImgFmt_XPS, and WIA_IPA_COMPRESSION is WIA_COMPRESSION_NONE; then the latter value means that the compression mode is undefined and the scanner must decide on a mode.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <span data-ttu-id="4c501-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-393">Contiene el nombre completo del elemento (el nombre del elemento junto con la información de la ruta de acceso).</span><span class="sxs-lookup"><span data-stu-id="4c501-393">Contains the full item name (the item name together with path information).</span></span> <span data-ttu-id="4c501-394">El nombre completo del elemento es el mismo que el parámetro <em>bstrFullItemName</em> de la función de utilidad de servicio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> .</span><span class="sxs-lookup"><span data-stu-id="4c501-394">The full item name is the same as the <em>bstrFullItemName</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="4c501-395">Una aplicación Lee esta propiedad para determinar qué elemento está usando actualmente y dónde se encuentra ese elemento en el árbol de elementos.</span><span class="sxs-lookup"><span data-stu-id="4c501-395">An application reads this property to determine which item it is currently using and where that item is located in the item tree.</span></span> <span data-ttu-id="4c501-396">Cada elemento debe tener un nombre único.</span><span class="sxs-lookup"><span data-stu-id="4c501-396">Each item should have a unique name.</span></span> <span data-ttu-id="4c501-397">Normalmente, las aplicaciones usan el nombre completo del elemento para buscar elementos en el árbol de elementos.</span><span class="sxs-lookup"><span data-stu-id="4c501-397">Applications commonly use the full item name to search for items in the item tree.</span></span> <span data-ttu-id="4c501-398">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-398">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-399">Se requiere para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-399">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-400">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-400">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <span data-ttu-id="4c501-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-402">Esta propiedad se reserva para uso futuro y no se implementa en este momento.</span><span class="sxs-lookup"><span data-stu-id="4c501-402">This property is reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="4c501-403">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-403">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <span data-ttu-id="4c501-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-405">Contiene el nombre del perfil ICM necesario para descodificar correctamente la imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-405">Contains the ICM profile name that is needed to properly decode the image.</span></span> <span data-ttu-id="4c501-406">Una aplicación Lee esta propiedad para determinar el perfil ICM que se va a utilizar al procesar la imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-406">An application reads this property to determine the ICM profile to use when processing the image.</span></span> <span data-ttu-id="4c501-407">El servicio WIA crea y mantiene esta propiedad basada en la entrada ICMProfiles en el archivo de instalación del controlador.</span><span class="sxs-lookup"><span data-stu-id="4c501-407">The WIA service creates and maintains this property based on the ICMProfiles entry in the driver installation file.</span></span></p>
<p><span data-ttu-id="4c501-408">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-408">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <span data-ttu-id="4c501-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-410">Solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-410">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="4c501-411">Los elementos de WIA 2,0 se agrupan en categorías que definen cómo se trata o se usa un <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4c501-411">WIA 2.0 items are grouped into categories that define how a <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> is to be treated or used.</span></span> <span data-ttu-id="4c501-412">Por ejemplo, si el elemento representa un alimentador, la aplicación debe esperar que contenga las propiedades necesarias del alimentador de documentos y que funcione como un alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="4c501-412">For example, If the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="4c501-413">Si el elemento representa un archivo terminado, una aplicación WIA 2,0 debe tratarlo de este modo, suponiendo que los datos son estáticos y se encuentran en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-413">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="4c501-414">(Las reglas de cada elemento se definirán en sus documentos de especificación individuales).</span><span class="sxs-lookup"><span data-stu-id="4c501-414">(The rules for each item will be defined in their individual specification documents.)</span></span></p>
<p><span data-ttu-id="4c501-415">Se requiere para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-415">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-416">Tipo: <strong>VT_CLSID</strong>, acceso: solo lectura, valores válidos: <a href="-wia-wia2-itemcategoryguids.md"><strong>GUID de categoría de elemento</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c501-416">Type: <strong>VT_CLSID</strong>, Access: Read Only, Valid values: <a href="-wia-wia2-itemcategoryguids.md"><strong>Item Category GUIDs</strong></a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <span data-ttu-id="4c501-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-418">Contiene las marcas descriptivas de un elemento WIA.</span><span class="sxs-lookup"><span data-stu-id="4c501-418">Contains the descriptive flags for a WIA item.</span></span> <span data-ttu-id="4c501-419">Las marcas de elemento son las mismas que las del parámetro <em>lObjectFlags</em> de la función de utilidad de servicio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> .</span><span class="sxs-lookup"><span data-stu-id="4c501-419">The item flags are the same as those in the <em>lObjectFlags</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="4c501-420">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-420">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-421">Una aplicación Lee esta propiedad para determinar los valores de marca descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="4c501-421">An application reads this property to determine the item's descriptive flag values.</span></span></p>
<p><span data-ttu-id="4c501-422">Tipo: <strong>VT_I4</strong> acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-422">Type: <strong>VT_I4</strong> Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="4c501-423">En la tabla siguiente se incluyen las marcas válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-423">The following table has the flags that are valid with this property.</span></span> <span data-ttu-id="4c501-424">Un asterisco \* indica que la marca no es compatible con Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="4c501-424">An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="4c501-425">(Solo está disponible a través de la interfaz <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> ). Un asterisco doble \* \* indica que la marca no se admite en Windows Server 2003 o Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="4c501-425">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) An double asterisk \*\* indicates that the flag is not supported in either Windows Server 2003 or Windows Vista or later.</span></span> <span data-ttu-id="4c501-426">El símbolo <strong>V</strong> indica que la marca solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-426">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> <span data-ttu-id="4c501-427">(Solo está disponible a través de la interfaz <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="4c501-427">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-428">Marca</span><span class="sxs-lookup"><span data-stu-id="4c501-428">Flag</span></span></th>
<th><span data-ttu-id="4c501-429">Definición</span><span class="sxs-lookup"><span data-stu-id="4c501-429">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-430">WiaItemTypeAnalyze\*</span><span class="sxs-lookup"><span data-stu-id="4c501-430">WiaItemTypeAnalyze\*</span></span></td>
<td><span data-ttu-id="4c501-431">Este elemento admite el método <strong>IWiaItem:: AnalyzeItem</strong> (descrito en la documentación de Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="4c501-431">This item supports the <strong>IWiaItem::AnalyzeItem</strong> method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="4c501-432">Este elemento también admite la generación automática de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="4c501-432">This item also supports automatic child item generation.</span></span> <span data-ttu-id="4c501-433">Esta funcionalidad es útil para la detección de regiones o la descomposición de páginas.</span><span class="sxs-lookup"><span data-stu-id="4c501-433">This capability is useful for region detection or page decomposition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-434">WiaItemTypeAudio</span><span class="sxs-lookup"><span data-stu-id="4c501-434">WiaItemTypeAudio</span></span></td>
<td><span data-ttu-id="4c501-435">Este elemento admite audio.</span><span class="sxs-lookup"><span data-stu-id="4c501-435">This item supports audio.</span></span> <span data-ttu-id="4c501-436">Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFile</strong> .</span><span class="sxs-lookup"><span data-stu-id="4c501-436">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-437">WiaItemTypeBurst\*</span><span class="sxs-lookup"><span data-stu-id="4c501-437">WiaItemTypeBurst\*</span></span></td>
<td><span data-ttu-id="4c501-438">Solo para carpetas.</span><span class="sxs-lookup"><span data-stu-id="4c501-438">For folders only.</span></span> <span data-ttu-id="4c501-439">Esta marca indica que las imágenes de esta carpeta se realizaron en una secuencia de tiempo continua.</span><span class="sxs-lookup"><span data-stu-id="4c501-439">This flag indicates that the images in this folder were taken in a continuous time sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-440">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="4c501-440">WiaItemTypeDeleted</span></span></td>
<td><span data-ttu-id="4c501-441">Este elemento está marcado para su eliminación, este elemento se ha eliminado, este elemento no existe o el contenido de este elemento no es válido.</span><span class="sxs-lookup"><span data-stu-id="4c501-441">This item is marked for deletion, this item has been deleted, this item does not exist, or the contents of this item are invalid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-442">WiaItemTypeDocument<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-442">WiaItemTypeDocument<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-443">Este elemento es un archivo de documento en uno de los formatos de documento que contiene la propiedad <strong>WIA_IPA_FORMAT</strong> .</span><span class="sxs-lookup"><span data-stu-id="4c501-443">This item is a document file in one of the document formats that the <strong>WIA_IPA_FORMAT</strong> property contains.</span></span> <span data-ttu-id="4c501-444">(Estos formatos incluyen los de archivos que no son de imagen, como los archivos. txt,. htm y. doc).</span><span class="sxs-lookup"><span data-stu-id="4c501-444">(These formats include those for nonimage files, such as .txt, .htm, and .doc files.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-445">WiaItemTypeDevice</span><span class="sxs-lookup"><span data-stu-id="4c501-445">WiaItemTypeDevice</span></span></td>
<td><span data-ttu-id="4c501-446">Este elemento representa un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="4c501-446">This item represents a connected device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-447">WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="4c501-447">WiaItemTypeDisconnected</span></span></td>
<td><span data-ttu-id="4c501-448">Este elemento representa un dispositivo desconectado.</span><span class="sxs-lookup"><span data-stu-id="4c501-448">This item represents a disconnected device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-449">WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="4c501-449">WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="4c501-450">El elemento admite las transferencias de archivos.</span><span class="sxs-lookup"><span data-stu-id="4c501-450">The item supports file transfers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-451">WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="4c501-451">WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="4c501-452">El elemento es una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c501-452">The item is a folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-453">WiaItemTypeFree</span><span class="sxs-lookup"><span data-stu-id="4c501-453">WiaItemTypeFree</span></span></td>
<td><span data-ttu-id="4c501-454">El elemento no se ha inicializado o se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="4c501-454">The item is uninitialized or has been deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-455">WiaItemTypeGenerated</span><span class="sxs-lookup"><span data-stu-id="4c501-455">WiaItemTypeGenerated</span></span></td>
<td><span data-ttu-id="4c501-456">Este elemento ha sido generado por una aplicación o por el controlador.</span><span class="sxs-lookup"><span data-stu-id="4c501-456">This item has been generated by an application or by the driver.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-457">WiaItemTypeHasAttachments\*</span><span class="sxs-lookup"><span data-stu-id="4c501-457">WiaItemTypeHasAttachments\*</span></span></td>
<td><span data-ttu-id="4c501-458">Este elemento admite datos adjuntos y actualmente contiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4c501-458">This item supports attachments and currently contains attachments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-459">WiaItemTypeHPanorama\*</span><span class="sxs-lookup"><span data-stu-id="4c501-459">WiaItemTypeHPanorama\*</span></span></td>
<td><span data-ttu-id="4c501-460">Este elemento representa una imagen panorámica horizontal.</span><span class="sxs-lookup"><span data-stu-id="4c501-460">This item represents a horizontal panoramic image.</span></span> <span data-ttu-id="4c501-461">Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFolder</strong> .</span><span class="sxs-lookup"><span data-stu-id="4c501-461">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-462">WiaItemTypeImage</span><span class="sxs-lookup"><span data-stu-id="4c501-462">WiaItemTypeImage</span></span></td>
<td><span data-ttu-id="4c501-463">El elemento es un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-463">The item is an image file.</span></span> <span data-ttu-id="4c501-464">Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFile</strong> .</span><span class="sxs-lookup"><span data-stu-id="4c501-464">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-466">El elemento es un origen de datos programable y sigue un conjunto de reglas de configuración predefinidas, que se basan en <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c501-466">The item is a programmable data source and follows a set of predefined configuration rules, which are based on <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-467">WiaItemTypeRoot<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="4c501-467">WiaItemTypeRoot<strong>V</strong></span></span></td>
<td><span data-ttu-id="4c501-468">Este elemento es el elemento raíz, que es el elemento primario de todos los elementos de característica que admite el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-468">This item is the root item, which is the parent to all the feature items that the device supports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-469">WiaItemTypeStorage</span><span class="sxs-lookup"><span data-stu-id="4c501-469">WiaItemTypeStorage</span></span></td>
<td><span data-ttu-id="4c501-470">Esta marca indica almacenamiento adicional para elementos de carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c501-470">This flag indicates additional storage for folders items.</span></span> <span data-ttu-id="4c501-471">Los controladores WIA especifican sus elementos en términos de imágenes y carpetas.</span><span class="sxs-lookup"><span data-stu-id="4c501-471">WIA drivers specify their items in terms of images and folders.</span></span> <span data-ttu-id="4c501-472">No existen propiedades de WIA que describen las características de un elemento de almacenamiento (por ejemplo, el espacio de almacenamiento restante, la velocidad de escritura o el tipo de medio).</span><span class="sxs-lookup"><span data-stu-id="4c501-472">No WIA properties exist that describe the characteristics of a storage item (such as remaining storage space, write speed, or type of media.</span></span> <span data-ttu-id="4c501-473">Se pueden agregar propiedades específicas del proveedor que exponen esta información.</span><span class="sxs-lookup"><span data-stu-id="4c501-473">Vendor-specific properties that expose this information can be added.</span></span> <span data-ttu-id="4c501-474">Estas propiedades solo son accesibles a las aplicaciones o extensiones que se escriben para reconocerlas.</span><span class="sxs-lookup"><span data-stu-id="4c501-474">These properties are accessible only to applications or extensions that are written to recognize them.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-475">WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="4c501-475">WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="4c501-476">Este elemento se puede usar para transferir datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-476">This item can be used to transfer data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-477">WiaItemTypeTwainCapabilityPassThrough</span><span class="sxs-lookup"><span data-stu-id="4c501-477">WiaItemTypeTwainCapabilityPassThrough</span></span></td>
<td><span data-ttu-id="4c501-478">Este tipo indica que el dispositivo WIA puede recibir datos de capacidad TWAIN del nivel de compatibilidad TWAIN.</span><span class="sxs-lookup"><span data-stu-id="4c501-478">This type indicates that the WIA device is able to receive TWAIN capability data from the TWAIN compatibility layer.</span></span> <span data-ttu-id="4c501-479">Si se establece este tipo, cualquier funcionalidad de TWAIN que no comprenda la capa de compatibilidad de TWAIN se pasará al controlador theWIA.</span><span class="sxs-lookup"><span data-stu-id="4c501-479">If this type is set, any TWAIN capability that is not understood by the TWAIN compatibility layer will be passed to theWIA driver.</span></span> <span data-ttu-id="4c501-480">Esto solo es válido para el elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="4c501-480">This is valid only for the root item.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-481">WiaItemTypeVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="4c501-481">WiaItemTypeVideo\*\*</span></span></td>
<td><span data-ttu-id="4c501-482">Este elemento admite el streaming de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4c501-482">This item supports streaming video.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-483">WiaItemTypeVPanorama\*</span><span class="sxs-lookup"><span data-stu-id="4c501-483">WiaItemTypeVPanorama\*</span></span></td>
<td><span data-ttu-id="4c501-484">Este elemento representa una imagen panorámica vertical.</span><span class="sxs-lookup"><span data-stu-id="4c501-484">This item represents a vertical panoramic image.</span></span> <span data-ttu-id="4c501-485">Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFolder</strong> .</span><span class="sxs-lookup"><span data-stu-id="4c501-485">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="4c501-486">Algunos de estos marcadores son obligatorios u opcionales para los elementos de WIA 2,0, de acuerdo con la categoría del elemento, como se muestra en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="4c501-486">Some of these flags are required or optional for WIA 2.0 items, according to the category of the item, as shown in this table.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-487">Categoría de elemento</span><span class="sxs-lookup"><span data-stu-id="4c501-487">Category of Item</span></span></th>
<th><span data-ttu-id="4c501-488">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4c501-488">Required</span></span></th>
<th><span data-ttu-id="4c501-489">Opcionales</span><span class="sxs-lookup"><span data-stu-id="4c501-489">Optional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-490">WIA_CATEGORY_ROOT</span><span class="sxs-lookup"><span data-stu-id="4c501-490">WIA_CATEGORY_ROOT</span></span></td>
<td><span data-ttu-id="4c501-491">WiaItemTypeRoot WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="4c501-491">WiaItemTypeRoot WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="4c501-492">WiaItemTypeDevice WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="4c501-492">WiaItemTypeDevice WiaItemTypeDisconnected</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-493">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="4c501-493">WIA_CATEGORY_FLATBED</span></span></td>
<td><span data-ttu-id="4c501-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="4c501-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="4c501-495">WiaItemTypeFolder (si se admiten varios elementos de regiones de análisis, esta marca solo es opcional para el elemento raíz WIA_CATEGORY_FLATBED).</span><span class="sxs-lookup"><span data-stu-id="4c501-495">WiaItemTypeFolder (If multiple scan regions items are supported, this flag is optional only for the WIA_CATEGORY_FLATBED root item.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span><span class="sxs-lookup"><span data-stu-id="4c501-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span></span></td>
<td><span data-ttu-id="4c501-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="4c501-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="4c501-498">WiaItemTypeFolder (si los elementos WIA_CATEGORY_FEEDER_FRONT y WIA_CATEGORY_FEEDER_BACK están presentes, esta marca solo es opcional para el elemento raíz WIA_CATEGORY_FEEDER).</span><span class="sxs-lookup"><span data-stu-id="4c501-498">WiaItemTypeFolder (If WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK items are present, then this flag is optional only for the WIA_CATEGORY_FEEDER root item.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-499">WIA_CATEGORY_FILM (raíz)</span><span class="sxs-lookup"><span data-stu-id="4c501-499">WIA_CATEGORY_FILM (root)</span></span></td>
<td><span data-ttu-id="4c501-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="4c501-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="4c501-501">None</span><span class="sxs-lookup"><span data-stu-id="4c501-501">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-502">WIA_CATEGORY_FILM (elementos secundarios)</span><span class="sxs-lookup"><span data-stu-id="4c501-502">WIA_CATEGORY_FILM (children)</span></span></td>
<td><span data-ttu-id="4c501-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="4c501-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="4c501-504">None</span><span class="sxs-lookup"><span data-stu-id="4c501-504">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-505">WIA_CATEGORY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="4c501-505">WIA_CATEGORY_FOLDER</span></span></td>
<td><span data-ttu-id="4c501-506">WiaItemTypeStorage WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="4c501-506">WiaItemTypeStorage WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="4c501-507">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="4c501-507">WiaItemTypeDeleted</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-508">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="4c501-508">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><span data-ttu-id="4c501-509">WiaItemTypeFile WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="4c501-509">WiaItemTypeFile WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="4c501-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="4c501-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <span data-ttu-id="4c501-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-512">Contiene el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="4c501-512">Contains the item name.</span></span> <span data-ttu-id="4c501-513">Una aplicación Lee esta propiedad para determinar qué elemento está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="4c501-513">An application reads this property to determine which item it is currently using.</span></span> <span data-ttu-id="4c501-514">Cada elemento tiene un nombre único.</span><span class="sxs-lookup"><span data-stu-id="4c501-514">Each item has a unique name.</span></span> <span data-ttu-id="4c501-515">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-515">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-516">Se requiere para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-516">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-517">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-517">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <span data-ttu-id="4c501-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-519">Contiene el tamaño actual, en bytes, de los datos asociados al elemento.</span><span class="sxs-lookup"><span data-stu-id="4c501-519">Contains the current size, in bytes, of the data that is associated with the item.</span></span> <span data-ttu-id="4c501-520">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-520">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-521">Contains es el tamaño total de los datos que se transfieren.</span><span class="sxs-lookup"><span data-stu-id="4c501-521">Contains is the total size of the data being transferred.</span></span> <span data-ttu-id="4c501-522">Si este valor es cero, significa que el minicontrolador no tiene información sobre el tamaño exacto de los datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-522">If this value is zero, it means that the minidriver has no information about the exact size of the data.</span></span> <span data-ttu-id="4c501-523">(Esto es habitual para los datos comprimidos). Una aplicación Lee este valor para determinar el tamaño de la adquisición antes de que tenga lugar.</span><span class="sxs-lookup"><span data-stu-id="4c501-523">(This is common for compressed data.) An application reads this value to determine the size of the acquisition before it takes place.</span></span> <span data-ttu-id="4c501-524">El servicio WIA Lee esta propiedad para ayudar en la asignación de memoria para las transferencias de datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-524">The WIA service reads this property to assist in allocating memory for data transfers.</span></span> <span data-ttu-id="4c501-525">Para obtener más información, consulte <a href="https://msdn.microsoft.com/library/ms792198.aspx">transferir datos a una aplicación WIA</a> si la propiedad se establece en cero y TYMED está configurado para una transferencia de archivos, el servicio WIA no asigna ninguna memoria para el minicontrolador WIA.</span><span class="sxs-lookup"><span data-stu-id="4c501-525">For further information, see <a href="https://msdn.microsoft.com/library/ms792198.aspx">Transferring Data to a WIA Application</a> if the property is set to zero and TYMED is configured for a file transfer, the WIA service does not allocate any memory for the WIA minidriver.</span></span></p>
<p><span data-ttu-id="4c501-526">Se requiere para todos los elementos de WIA 2,0 habilitados para transferencia.</span><span class="sxs-lookup"><span data-stu-id="4c501-526">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-527">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-527">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <span data-ttu-id="4c501-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-529">Contiene la hora en que se capturó originalmente la imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-529">Contains the time that the image was originally captured.</span></span> <span data-ttu-id="4c501-530">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-530">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="4c501-531">Esta propiedad se debe notificar como vector de ocho valores de <strong>palabra</strong> en forma de estructura SYSTEMTIME (descrita en la documentación de Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="4c501-531">This property should be reported as a vector of eight <strong>WORD</strong> values in the form of a SYSTEMTIME structure (described in the Platform SDK documentation).</span></span></p>
<p><span data-ttu-id="4c501-532">Opcional para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-532">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-533">Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-533">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong> Access: Read/Write or Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="4c501-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-535">Solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-535">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="4c501-536">Especifica el número de elementos que se almacenan en el elemento de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="4c501-536">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="4c501-537">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-537">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <span data-ttu-id="4c501-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-539">Especifica el tamaño de búfer mínimo que se utiliza en las transferencias de datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-539">Specifies the minimum buffer size that is used in data transfers.</span></span> <span data-ttu-id="4c501-540">Si la transferencia de datos se realiza a través de un mecanismo de devolución de llamada, el valor de la propiedad puede ser tan pequeño como 64 KB.</span><span class="sxs-lookup"><span data-stu-id="4c501-540">If the data transfer is performed through a callback mechanism, the property value can be as small as 64KB.</span></span> <span data-ttu-id="4c501-541">Sin embargo, si la transferencia es a archivo, el valor de la propiedad es el número de bytes que se necesitan para transferir una página de datos a la vez.</span><span class="sxs-lookup"><span data-stu-id="4c501-541">However, if the transfer is to file, the property value is the number of bytes that are needed to transfer one page of data at a time.</span></span> <span data-ttu-id="4c501-542">El minicontrolador crea y mantiene esta propiedad de WIA.</span><span class="sxs-lookup"><span data-stu-id="4c501-542">The minidriver creates and maintains this WIA property.</span></span></p>
<p><span data-ttu-id="4c501-543">Opcional para todos los elementos de WIA 2,0 habilitados para transferencia.</span><span class="sxs-lookup"><span data-stu-id="4c501-543">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-544">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-544">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <span data-ttu-id="4c501-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-546">Contiene el número de líneas contenidas en la imagen (el alto vertical de la imagen en píxeles).</span><span class="sxs-lookup"><span data-stu-id="4c501-546">Contains the number of lines contained in the image (the vertical height of the image in pixels).</span></span> <span data-ttu-id="4c501-547">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-547">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-548">Opcional para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-548">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-549">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-549">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <span data-ttu-id="4c501-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-551">Contiene el número de píxeles en cada línea de la imagen (el ancho de la imagen en píxeles).</span><span class="sxs-lookup"><span data-stu-id="4c501-551">Contains the number of pixels in each line of the image (the width of the image in pixels).</span></span> <span data-ttu-id="4c501-552">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-552">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-553">Opcional para todos los elementos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4c501-553">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-554">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-554">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <span data-ttu-id="4c501-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-556">Esta propiedad no se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-556">This property is not supported in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="4c501-557">Contiene opciones de empaquetado de datos de imagen.</span><span class="sxs-lookup"><span data-stu-id="4c501-557">Contains image data packing options.</span></span> <span data-ttu-id="4c501-558">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-558">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-559">Una aplicación Lee esta propiedad para determinar las opciones de empaquetado de imágenes o establece las opciones de empaquetado de imágenes actuales.</span><span class="sxs-lookup"><span data-stu-id="4c501-559">An application reads this property to determine the image packing options or sets the current image packing options.</span></span></p>
<p><span data-ttu-id="4c501-560">Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="4c501-560">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="4c501-561">Si el dispositivo se puede establecer en un solo valor, cree un WIA_PROP_LIST tipo y coloque el valor válido en él.</span><span class="sxs-lookup"><span data-stu-id="4c501-561">If the device can be set to only a single value, create a WIA_PROP_LIST type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="4c501-562">En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-562">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-563">Value</span><span class="sxs-lookup"><span data-stu-id="4c501-563">Value</span></span></th>
<th><span data-ttu-id="4c501-564">Definición</span><span class="sxs-lookup"><span data-stu-id="4c501-564">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-565">WIA_PACKED_PIXEL</span><span class="sxs-lookup"><span data-stu-id="4c501-565">WIA_PACKED_PIXEL</span></span></td>
<td><span data-ttu-id="4c501-566">Los datos de la imagen están en formato de píxel empaquetado.</span><span class="sxs-lookup"><span data-stu-id="4c501-566">Image data is in packed-pixel format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-567">WIA_PLANAR</span><span class="sxs-lookup"><span data-stu-id="4c501-567">WIA_PLANAR</span></span></td>
<td><span data-ttu-id="4c501-568">Los datos de la imagen están en formato plano.</span><span class="sxs-lookup"><span data-stu-id="4c501-568">Image data is in planar format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <span data-ttu-id="4c501-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-570">Contiene el formato preferido para las imágenes que este minicontrolador transfiere.</span><span class="sxs-lookup"><span data-stu-id="4c501-570">Contains the preferred format for images that this minidriver transfers.</span></span> <span data-ttu-id="4c501-571">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-571">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-572">Se requiere para todos los elementos de WIA 2,0 habilitados para transferencia.</span><span class="sxs-lookup"><span data-stu-id="4c501-572">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-573">Tipo: <strong>CLSID</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-573">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <span data-ttu-id="4c501-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-575">Especifica un CLSID que representa un conjunto de valores de propiedad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-575">Specifies a CLSID that represents a set of device property values.</span></span> <span data-ttu-id="4c501-576">Si un controlador de dispositivo implementa esta característica, las aplicaciones usan esta propiedad para determinar si el dispositivo admite un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="4c501-576">If a device driver implements this feature, applications use this property to determine if the device supports a set of values.</span></span></p>
<p><span data-ttu-id="4c501-577">Tipo: <strong>CLSID</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4c501-577">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4c501-578">En la tabla siguiente se incluyen las 12 constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-578">The following table has the 12 constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-579">Value</span><span class="sxs-lookup"><span data-stu-id="4c501-579">Value</span></span></th>
<th><span data-ttu-id="4c501-580">Definición</span><span class="sxs-lookup"><span data-stu-id="4c501-580">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-581">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="4c501-581">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="4c501-582">Mapa de bits de MicrosoftWindows con un archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="4c501-582">MicrosoftWindows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-583">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="4c501-583">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="4c501-584">Metarchivo extendido de Windows</span><span class="sxs-lookup"><span data-stu-id="4c501-584">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-585">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="4c501-585">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="4c501-586">Formato de archivo intercambiable</span><span class="sxs-lookup"><span data-stu-id="4c501-586">Exchangeable File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-587">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="4c501-587">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="4c501-588">Formato FlashPix</span><span class="sxs-lookup"><span data-stu-id="4c501-588">FlashPix format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-589">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="4c501-589">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="4c501-590">Formato de imagen GIF</span><span class="sxs-lookup"><span data-stu-id="4c501-590">GIF image format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-591">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="4c501-591">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="4c501-592">Formato de archivo de icono de Windows</span><span class="sxs-lookup"><span data-stu-id="4c501-592">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-593">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="4c501-593">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="4c501-594">Formato comprimido JPEG</span><span class="sxs-lookup"><span data-stu-id="4c501-594">JPEG compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-595">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="4c501-595">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="4c501-596">Formato de archivo de Eastman Kodak</span><span class="sxs-lookup"><span data-stu-id="4c501-596">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-597">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="4c501-597">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="4c501-598">Formato PNG de W3C</span><span class="sxs-lookup"><span data-stu-id="4c501-598">W3C PNG format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-599">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="4c501-599">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="4c501-600">Mapa de bits de Windows sin un archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="4c501-600">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-601">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="4c501-601">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="4c501-602">Formato TIFF</span><span class="sxs-lookup"><span data-stu-id="4c501-602">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-603">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="4c501-603">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="4c501-604">Metarchivo de Windows</span><span class="sxs-lookup"><span data-stu-id="4c501-604">Windows metafile</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <span data-ttu-id="4c501-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-606">Solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-606">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="4c501-607">Contiene el número de bits de cada canal.</span><span class="sxs-lookup"><span data-stu-id="4c501-607">Contains the number of bits in each channel.</span></span> <span data-ttu-id="4c501-608">Esta propiedad se debe presentar como un vector de tantos valores de BYTE como canales, donde el primer BYTE corresponde al número de bits del primer canal, el segundo byte al número de bits del segundo canal, etc.</span><span class="sxs-lookup"><span data-stu-id="4c501-608">This property should be reported as a vector of as many BYTE values as there are channels, where the first BYTE corresponds to the number of bits in the first channel, the second byte to the number of bits in the second channel and so on.</span></span> <span data-ttu-id="4c501-609">Debe haber tantas entradas como canales haya en función de WIA_IPA_CHANNELS_PER_PIXEL.</span><span class="sxs-lookup"><span data-stu-id="4c501-609">There need to be as many entries as there are channels according to WIA_IPA_CHANNELS_PER_PIXEL.</span></span> <span data-ttu-id="4c501-610">El controlador establece esa propiedad cuando la aplicación cambia a WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="4c501-610">The driver sets that property when the application switches to WiaImgFmt_RAW.</span></span> <span data-ttu-id="4c501-611">En el caso de los subtipos conocidos, hay tantas entradas como se muestran en la tabla en WIA_IPA_RAW_SUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="4c501-611">For the well-known subtypes, there are as many entries as listed in the table under WIA_IPA_RAW_SUBTYPE.</span></span></p>
<p><span data-ttu-id="4c501-612">Tipo: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-612">Type: <strong>VT_UI1</strong>|<strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <span data-ttu-id="4c501-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-614">Esta propiedad está reservada para un uso futuro y no se implementa en este momento.</span><span class="sxs-lookup"><span data-stu-id="4c501-614">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="4c501-615">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-615">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <span data-ttu-id="4c501-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-617">Especifica si se van a suprimir las páginas de propiedades generales de los elementos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-617">Specifies whether to suppress the general property pages for items on the device.</span></span></p>
<p><span data-ttu-id="4c501-618">Esta propiedad está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-618">This property is available on Windows XP and later.</span></span></p>
<p><span data-ttu-id="4c501-619">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-619">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="4c501-620">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-620">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="4c501-621">El asterisco \* indica que la constante no es válida con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-621">The asterisk \* indicates that the constant is not valid with Windows Vista and later.</span></span> <span data-ttu-id="4c501-622">(Solo está disponible a través de la interfaz <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="4c501-622">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-623">Constante</span><span class="sxs-lookup"><span data-stu-id="4c501-623">Constant</span></span></th>
<th><span data-ttu-id="4c501-624">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c501-624">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL \*</span><span class="sxs-lookup"><span data-stu-id="4c501-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL\*</span></span></td>
<td><span data-ttu-id="4c501-626">Suprime la página de propiedades general Item de una cámara.</span><span class="sxs-lookup"><span data-stu-id="4c501-626">Suppress the general item property page for a camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span><span class="sxs-lookup"><span data-stu-id="4c501-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span></span></td>
<td><span data-ttu-id="4c501-628">Suprime la página de propiedades general Item de un escáner.</span><span class="sxs-lookup"><span data-stu-id="4c501-628">Suppress the general item property page for a scanner.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <span data-ttu-id="4c501-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-630">Esta propiedad contiene la configuración del método de transferencia.</span><span class="sxs-lookup"><span data-stu-id="4c501-630">This property contains the transfer method setting.</span></span> <span data-ttu-id="4c501-631">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-631">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="4c501-632">Una aplicación Lee esta propiedad para determinar el método del minicontrolador de transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="4c501-632">An application reads this property to determine the minidriver's method of data transfer.</span></span></p>
<p><span data-ttu-id="4c501-633">Se requiere para todos los elementos de WIA 2,0 habilitados para transferencia.</span><span class="sxs-lookup"><span data-stu-id="4c501-633">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="4c501-634">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="4c501-634">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="4c501-635">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c501-635">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="4c501-636">El asterisco \* indica constantes que no son válidas con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-636">The asterisk \* indicates constants that are not valid with Windows Vista and later.</span></span> <span data-ttu-id="4c501-637">(Solo están disponibles a través de la interfaz <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="4c501-637">(They are only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c501-638">Tipo de transferencia</span><span class="sxs-lookup"><span data-stu-id="4c501-638">Transfer Type</span></span></th>
<th><span data-ttu-id="4c501-639">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c501-639">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c501-640">TYMED_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="4c501-640">TYMED_CALLBACK\*</span></span></td>
<td><span data-ttu-id="4c501-641">Transferir una imagen a la memoria, en bandas.</span><span class="sxs-lookup"><span data-stu-id="4c501-641">Transfer an image to memory, in bands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-642">TYMED_MULTIPAGE_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="4c501-642">TYMED_MULTIPAGE_CALLBACK\*</span></span></td>
<td><span data-ttu-id="4c501-643">Transferir varias imágenes a la memoria, en bandas.</span><span class="sxs-lookup"><span data-stu-id="4c501-643">Transfer multiple images to memory, in bands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c501-644">TYMED_FILE</span><span class="sxs-lookup"><span data-stu-id="4c501-644">TYMED_FILE</span></span></td>
<td><span data-ttu-id="4c501-645">Transferir una imagen a un archivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-645">Transfer an image to a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c501-646">TYMED_MULTIPAGE_FILE</span><span class="sxs-lookup"><span data-stu-id="4c501-646">TYMED_MULTIPAGE_FILE</span></span></td>
<td><span data-ttu-id="4c501-647">Transferir una imagen a un archivo.</span><span class="sxs-lookup"><span data-stu-id="4c501-647">Transfer an image to a file.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="4c501-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="4c501-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4c501-649">Solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c501-649">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="4c501-650">Especifica el número de bytes que se van a cargar para un elemento.</span><span class="sxs-lookup"><span data-stu-id="4c501-650">Specifies the number of bytes to upload for an item.</span></span></p>
<p><span data-ttu-id="4c501-651">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="4c501-651">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="4c501-652">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c501-652">Requirements</span></span>



| <span data-ttu-id="4c501-653">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c501-653">Requirement</span></span> | <span data-ttu-id="4c501-654">Value</span><span class="sxs-lookup"><span data-stu-id="4c501-654">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4c501-655">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c501-655">Minimum supported client</span></span><br/> | <span data-ttu-id="4c501-656">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4c501-656">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4c501-657">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c501-657">Minimum supported server</span></span><br/> | <span data-ttu-id="4c501-658">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c501-658">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4c501-659">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c501-659">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c501-660"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c501-660"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




