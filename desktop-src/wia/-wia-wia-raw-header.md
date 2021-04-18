---
description: La \_ estructura de \_ encabezado sin formato de WIA define una imagen en el formato de datos sin procesar de un dispositivo y permite a las aplicaciones usar el formato RAW en las transferencias de adquisición de imágenes de Windows (WIA).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: WIA_RAW_HEADER estructura (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715174"
---
# <a name="wia_raw_header-structure"></a><span data-ttu-id="1cff5-103">\_Estructura de encabezado sin formato de WIA \_</span><span class="sxs-lookup"><span data-stu-id="1cff5-103">WIA\_RAW\_HEADER structure</span></span>

<span data-ttu-id="1cff5-104">La estructura de **\_ \_ encabezado sin formato de WIA** define una imagen en el formato de datos sin procesar de un dispositivo y permite a las aplicaciones usar el formato RAW en las transferencias de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="1cff5-104">The **WIA\_RAW\_HEADER** structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cff5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cff5-105">Syntax</span></span>


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a><span data-ttu-id="1cff5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1cff5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1cff5-107">**Tag**</span><span class="sxs-lookup"><span data-stu-id="1cff5-107">**Tag**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-109">Nombre del formato.</span><span class="sxs-lookup"><span data-stu-id="1cff5-109">The name of the format.</span></span> <span data-ttu-id="1cff5-110">Debe ser el literal ' WRAW ' (cuatro caracteres ASCII de un solo byte).</span><span class="sxs-lookup"><span data-stu-id="1cff5-110">This must be the literal 'WRAW' (four single byte ASCII characters).</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-111">**Versión**</span><span class="sxs-lookup"><span data-stu-id="1cff5-111">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-112">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-112">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-113">Versión del formato sin formato.</span><span class="sxs-lookup"><span data-stu-id="1cff5-113">The version of the RAW format.</span></span> <span data-ttu-id="1cff5-114">Use siempre 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="1cff5-114">Always use 0x00010000.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-115">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="1cff5-115">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-117">Bytes totales válidos en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="1cff5-117">The total valid bytes in the header.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-118">**XRes**</span><span class="sxs-lookup"><span data-stu-id="1cff5-118">**XRes**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-119">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-120">Resolución horizontal en puntos por pulgada.</span><span class="sxs-lookup"><span data-stu-id="1cff5-120">The horizontal resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-121">**YRes**</span><span class="sxs-lookup"><span data-stu-id="1cff5-121">**YRes**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-123">Resolución vertical en puntos por pulgada.</span><span class="sxs-lookup"><span data-stu-id="1cff5-123">The vertical resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-124">**XExtent**</span><span class="sxs-lookup"><span data-stu-id="1cff5-124">**XExtent**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-125">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-125">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-126">Ancho de la imagen en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1cff5-126">The width of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-127">**YExtent**</span><span class="sxs-lookup"><span data-stu-id="1cff5-127">**YExtent**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-128">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-128">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-129">Alto de la imagen en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1cff5-129">The height of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-130">**BytesPerLine**</span><span class="sxs-lookup"><span data-stu-id="1cff5-130">**BytesPerLine**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-131">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-132">El número de bytes en una línea de una imagen sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="1cff5-132">The number of bytes in a line of an uncompressed image.</span></span> <span data-ttu-id="1cff5-133">Use 0 cuando se compriman los datos para indicar que se desconoce el número de bytes por línea.</span><span class="sxs-lookup"><span data-stu-id="1cff5-133">Use 0 when the data is compressed to signal that the number of bytes per line is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-134">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="1cff5-134">**BitsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-135">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-135">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-136">Número total de bits por píxel para todos los canales de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1cff5-136">The total number of bits per pixel for all the pixel's channels.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-137">**ChannelsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="1cff5-137">**ChannelsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-138">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-139">Número de canales de color de un píxel.</span><span class="sxs-lookup"><span data-stu-id="1cff5-139">The number of color channels in a pixel.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-140">**DataType**</span><span class="sxs-lookup"><span data-stu-id="1cff5-140">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-141">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-141">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-142">\_ \_ Tipo de la imagen del IPA de WIA.</span><span class="sxs-lookup"><span data-stu-id="1cff5-142">The WIA\_IPA\_DATATYPE of the image.</span></span> <span data-ttu-id="1cff5-143">Puesto que \_ \_ el formato de IPA de WIA se establece en WiaImgFmt \_ raw, se trata de una lista de valores permitidos entre los que la aplicación elige.</span><span class="sxs-lookup"><span data-stu-id="1cff5-143">Since WIA\_IPA\_FORMAT is set to WiaImgFmt\_RAW, this is a list of allowed values from which the application picks.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-144">**BitsPerChannel \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="1cff5-144">**BitsPerChannel\[8\]**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-145">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="1cff5-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-146">Número de bits de un canal, hasta un máximo de 8.</span><span class="sxs-lookup"><span data-stu-id="1cff5-146">The number of bits in a channel, up to a maximum of 8.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-147">**Compresión**</span><span class="sxs-lookup"><span data-stu-id="1cff5-147">**Compression**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-148">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-148">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-149">Un \_ \_ valor de compresión de IPA de WIA que especifica el tipo de compresión utilizado, si existe.</span><span class="sxs-lookup"><span data-stu-id="1cff5-149">A WIA\_IPA\_COMPRESSION value specifying the type of compression used, if any.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-150">**PhotometricInterp**</span><span class="sxs-lookup"><span data-stu-id="1cff5-150">**PhotometricInterp**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-151">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-151">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-152">Un \_ \_ valor INTERP de fotométrico del IPA \_ de WIA que especifica la interpretación fotométrica de la imagen.</span><span class="sxs-lookup"><span data-stu-id="1cff5-152">A WIA\_IPA\_PHOTOMETRIC\_INTERP value specifying the photometric interpretation of the image.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-153">**LineOrder**</span><span class="sxs-lookup"><span data-stu-id="1cff5-153">**LineOrder**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-154">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-154">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-155">Valor que representa el orden de la línea de la imagen.</span><span class="sxs-lookup"><span data-stu-id="1cff5-155">A value representing the image line order.</span></span> <span data-ttu-id="1cff5-156">Siempre es el orden de las \_ líneas \_ de WIA \_ de arriba abajo o el \_ \_ \_ orden de las líneas de la parte \_ \_ inferior \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1cff5-156">This is always either WIA\_LINE\_ORDER\_TOP\_TO\_BOTTOM or WIA\_LINE\_ORDER\_BOTTOM\_TO\_TOP.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-157">**RawDataOffset**</span><span class="sxs-lookup"><span data-stu-id="1cff5-157">**RawDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-158">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-158">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-159">Posición de los datos de imagen sin procesar en bytes, empezando por la posición donde finaliza el encabezado o la posición donde finaliza la paleta.</span><span class="sxs-lookup"><span data-stu-id="1cff5-159">The position of the raw image data in bytes, starting from position where the header ends or the position where the palette ends.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-160">**RawDataSize**</span><span class="sxs-lookup"><span data-stu-id="1cff5-160">**RawDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-161">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-161">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-162">Tamaño, en bytes, de los datos de imagen sin procesar.</span><span class="sxs-lookup"><span data-stu-id="1cff5-162">The size, in bytes, of the raw image data.</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-163">**PaletteOffset**</span><span class="sxs-lookup"><span data-stu-id="1cff5-163">**PaletteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-164">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-165">Posición de la paleta en bytes, empezando por la posición donde finaliza el encabezado o la posición donde finalizan los datos.</span><span class="sxs-lookup"><span data-stu-id="1cff5-165">The position of the palette in bytes, starting from the position where the header ends or the position where the data ends.</span></span> <span data-ttu-id="1cff5-166">(Este valor es 0, si no hay ninguna paleta).</span><span class="sxs-lookup"><span data-stu-id="1cff5-166">(This value is 0, if there is no palette.)</span></span>

</dd> <dt>

<span data-ttu-id="1cff5-167">**PaletteSize**</span><span class="sxs-lookup"><span data-stu-id="1cff5-167">**PaletteSize**</span></span>
</dt> <dd>

<span data-ttu-id="1cff5-168">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cff5-168">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1cff5-169">Tamaño, en bytes, de la tabla Palette.</span><span class="sxs-lookup"><span data-stu-id="1cff5-169">The size, in bytes, of the palette table.</span></span> <span data-ttu-id="1cff5-170">(Es 0 si no hay ninguna paleta).</span><span class="sxs-lookup"><span data-stu-id="1cff5-170">(This is 0, if there is no palette.)</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cff5-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cff5-171">Remarks</span></span>

<span data-ttu-id="1cff5-172">Dado que este no es un formato de archivo, use una cadena vacía para la propiedad de extensión de archivo del IPA de WIA \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1cff5-172">Because this is not a file format, use an empty string for the WIA\_IPA\_FILE\_EXTENSION property.</span></span>

<span data-ttu-id="1cff5-173">La paleta y los datos pueden aparecer en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="1cff5-173">The palette and the data can come in either order.</span></span>

<span data-ttu-id="1cff5-174">**RawDataSize** no incluye el encabezado o la paleta.</span><span class="sxs-lookup"><span data-stu-id="1cff5-174">**RawDataSize** does not include either the header or the palette.</span></span> <span data-ttu-id="1cff5-175">Utilice este campo para comprobar que la transferencia de la imagen se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1cff5-175">Use this field to verify that the transfer of the image has been successful.</span></span>

<span data-ttu-id="1cff5-176">**PaletteSize** es bytes, no el número de entradas de la paleta.</span><span class="sxs-lookup"><span data-stu-id="1cff5-176">**PaletteSize** is bytes, not the number of entries in the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cff5-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cff5-177">Requirements</span></span>



| <span data-ttu-id="1cff5-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cff5-178">Requirement</span></span> | <span data-ttu-id="1cff5-179">Value</span><span class="sxs-lookup"><span data-stu-id="1cff5-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1cff5-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cff5-180">Minimum supported client</span></span><br/> | <span data-ttu-id="1cff5-181">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1cff5-181">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1cff5-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cff5-182">Minimum supported server</span></span><br/> | <span data-ttu-id="1cff5-183">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cff5-183">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1cff5-184">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cff5-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cff5-185"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cff5-185"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




