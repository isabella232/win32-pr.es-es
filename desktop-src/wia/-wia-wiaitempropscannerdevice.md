---
description: Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) tienen valores de propiedad que se almacenan en el registro de Windows.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Constantes de propiedad del dispositivo Scanner (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705680"
---
# <a name="scanner-device-property-constants"></a><span data-ttu-id="0d1a1-103">Constantes de propiedades de dispositivo de escáner</span><span class="sxs-lookup"><span data-stu-id="0d1a1-103">Scanner Device Property Constants</span></span>

<span data-ttu-id="0d1a1-104">Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) tienen valores de propiedad que se almacenan en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-104">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="0d1a1-105">Para obtener más información, consulte [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d1a1-105">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span> <span data-ttu-id="0d1a1-106">Las siguientes constantes de propiedades de dispositivo, con sus cadenas asociadas, son específicas de los escáneres de imágenes digitales.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-106">The following device property constants, with their associated strings, are specific to digital image scanners.</span></span>

<span data-ttu-id="0d1a1-107">El prefijo "WIA \_ DPS \_ " indica una propiedad de dispositivo para los dispositivos de escáner y es la Convención de nomenclatura que se usa en C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-107">The prefix "WIA\_DPS\_" indicates a Device Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="0d1a1-108">Con el fin de crear scripts, estas constantes usan el prefijo "ScannerDevice" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="0d1a1-108">For scripting purposes these constants use the prefix "ScannerDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="0d1a1-109">El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0d1a1-110">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="0d1a1-110">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0d1a1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <span data-ttu-id="0d1a1-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-113">Esta propiedad solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-113">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="0d1a1-114">Contiene un identificador único de instancia de función para un dispositivo de escáner de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-114">Contains a unique function instance identifier for a web services scanner device.</span></span> <span data-ttu-id="0d1a1-115">Este identificador representa el servicio Web en el dispositivo de escáner con el que se está comunicando el mini controlador WIA.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-115">This identifier represents the web service on the scanner device with which the WIA mini-driver is communicating.</span></span> <span data-ttu-id="0d1a1-116">No se deben realizar suposiciones sobre el formato de este identificador.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-116">No assumptions about the form of this identifier should be made.</span></span> <span data-ttu-id="0d1a1-117">El controlador mini de WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-117">The WIA mini-driver creates and maintains this property.</span></span> <br/> <span data-ttu-id="0d1a1-118">Las aplicaciones WIA pueden usar el valor de WIA_DPS_DEVICE_ID para buscar, mediante la API de detección de funciones, el objeto de instancia de función que representa el dispositivo de analizador de servicios web usado en la sesión de WIA 2,0 actual.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-118">WIA applications can use the value of WIA_DPS_DEVICE_ID to find, using the Function Discovery API, the function instance object representing the web services scanner device used in the current WIA 2.0 session.</span></span><br/> <span data-ttu-id="0d1a1-119">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-119">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <span data-ttu-id="0d1a1-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d1a1-121">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-121">Reserved, do not use.</span></span><br/> <span data-ttu-id="0d1a1-122">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-122">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <span data-ttu-id="0d1a1-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d1a1-124">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-124">Reserved, do not use.</span></span><br/> <span data-ttu-id="0d1a1-125">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-125">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <span data-ttu-id="0d1a1-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0d1a1-127">Contiene las capacidades del escáner.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-127">Contains the capabilities of the scanner.</span></span> <span data-ttu-id="0d1a1-128">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-128">The minidriver creates and maintains this property.</span></span> <br/> <span data-ttu-id="0d1a1-129">Una aplicación Lee esta propiedad para determinar si el escáner tiene un alimentador plano, un alimentador de documentos o un dúplex instalado.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-129">An application reads this property to determine whether the scanner has a flatbed, document feeder, or duplexer installed.</span></span> <span data-ttu-id="0d1a1-130">Esta propiedad también se usa para definir aún más las características instaladas.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-130">This property is also used to further define the installed features.</span></span><br/> <span data-ttu-id="0d1a1-131">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-131">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="0d1a1-132">En la tabla siguiente se describen las constantes que solo son válidas con Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-132">The following table describes the constants that are valid with Windows 7 only.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-133">Marcas</span><span class="sxs-lookup"><span data-stu-id="0d1a1-133">Flags</span></span></th>
<th><span data-ttu-id="0d1a1-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-135">AUTO_SOURCE</span><span class="sxs-lookup"><span data-stu-id="0d1a1-135">AUTO_SOURCE</span></span></td>
<td><span data-ttu-id="0d1a1-136">El escáner tiene instalado un controlador de documentos automático.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-136">The scanner has an automatic document handler installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0d1a1-137">En la tabla siguiente se describen las constantes que son válidas solo con Windows 7 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-137">The following table describes the constants that are valid with Windows 7 and Windows Vista only.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-138">Marcas</span><span class="sxs-lookup"><span data-stu-id="0d1a1-138">Flags</span></span></th>
<th><span data-ttu-id="0d1a1-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-140">ADVANCED_DUP</span><span class="sxs-lookup"><span data-stu-id="0d1a1-140">ADVANCED_DUP</span></span></td>
<td><span data-ttu-id="0d1a1-141">El dispositivo admite la configuración avanzada de examen dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-141">The device supports advanced duplex scan configuration.</span></span> <span data-ttu-id="0d1a1-142">Use WIA_IPS_DUPLEX_SETTINGS para cambiar entre el uso de configuraciones de dúplex básica y avanzada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-142">Use WIA_IPS_DUPLEX_SETTINGS to switch between using basic and advanced duplex configurations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-143">DETECT_FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="0d1a1-143">DETECT_FILM_TPA</span></span></td>
<td><span data-ttu-id="0d1a1-144">El escáner puede detectar cuándo está listo para digitalizar el adaptador de película o transparencia.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-144">The scanner can detect when the transparency/film adapter is ready to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-145">DETECT_STOR</span><span class="sxs-lookup"><span data-stu-id="0d1a1-145">DETECT_STOR</span></span></td>
<td><span data-ttu-id="0d1a1-146">El analizador puede detectar cuándo hay documentos en el almacenamiento interno.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-146">The scanner can detect when there are documents in the internal storage.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-147">FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="0d1a1-147">FILM_TPA</span></span></td>
<td><span data-ttu-id="0d1a1-148">El escáner está equipado con un adaptador de exploración de película o transparencia.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-148">The scanner is equipped with a transparency/film scanning adapter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-149">STOR</span><span class="sxs-lookup"><span data-stu-id="0d1a1-149">STOR</span></span></td>
<td><span data-ttu-id="0d1a1-150">El escáner está equipado con un dispositivo de almacenamiento de imágenes interno.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-150">The scanner is equipped with an internal image storage device.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0d1a1-151">En la tabla siguiente se describen las constantes que son válidas con Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-151">The following table describes the constants that are valid with Windows XP or later.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-152">Marcas</span><span class="sxs-lookup"><span data-stu-id="0d1a1-152">Flags</span></span></th>
<th><span data-ttu-id="0d1a1-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-154">DETECT_FEED</span><span class="sxs-lookup"><span data-stu-id="0d1a1-154">DETECT_FEED</span></span></td>
<td><span data-ttu-id="0d1a1-155">El escáner puede detectar un documento en el alimentador.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-155">The scanner can detect a document in the feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-156">DETECT_FLAT</span><span class="sxs-lookup"><span data-stu-id="0d1a1-156">DETECT_FLAT</span></span></td>
<td><span data-ttu-id="0d1a1-157">El escáner puede detectar un documento en la placa de escáner.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-157">The scanner can detect a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-158">DETECT_SCAN</span><span class="sxs-lookup"><span data-stu-id="0d1a1-158">DETECT_SCAN</span></span></td>
<td><span data-ttu-id="0d1a1-159">El escáner solo puede detectar un documento en el alimentador mediante el análisis.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-159">The scanner can detect a document in the feeder only by scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-160">DUPLICA</span><span class="sxs-lookup"><span data-stu-id="0d1a1-160">DUP</span></span></td>
<td><span data-ttu-id="0d1a1-161">El escáner tiene un dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-161">The scanner has a duplexer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-162">FEED</span><span class="sxs-lookup"><span data-stu-id="0d1a1-162">FEED</span></span></td>
<td><span data-ttu-id="0d1a1-163">El escáner tiene instalado un controlador de documentos automático.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-163">The scanner has an automatic document handler installed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-164">PISO</span><span class="sxs-lookup"><span data-stu-id="0d1a1-164">FLAT</span></span></td>
<td><span data-ttu-id="0d1a1-165">El escáner tiene una placa plana.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-165">The scanner has a flatbed platen.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0d1a1-166">En la tabla siguiente se describen las constantes que son válidas solo con Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-166">The following table describes the constants that are valid with Windows XP only.</span></span> <span data-ttu-id="0d1a1-167">Estos valores están en desuso para Windows 7 y Windows Vista, y no deben usarse.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-167">These values have been deprecated for Windows 7 and Windows Vista and should not be used.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-168">Marcas</span><span class="sxs-lookup"><span data-stu-id="0d1a1-168">Flags</span></span></th>
<th><span data-ttu-id="0d1a1-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-170">DETECT_DUP</span><span class="sxs-lookup"><span data-stu-id="0d1a1-170">DETECT_DUP</span></span></td>
<td><span data-ttu-id="0d1a1-171">El analizador puede detectar una solicitud de examen dúplex del usuario.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-171">The scanner can detect a duplex scan request from the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-172">DETECT_DUP_AVAIL</span><span class="sxs-lookup"><span data-stu-id="0d1a1-172">DETECT_DUP_AVAIL</span></span></td>
<td><span data-ttu-id="0d1a1-173">El escáner puede indicar cuándo está instalado el dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-173">The scanner can tell when the duplexer is installed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-174">DETECT_FEED_AVAIL</span><span class="sxs-lookup"><span data-stu-id="0d1a1-174">DETECT_FEED_AVAIL</span></span></td>
<td><span data-ttu-id="0d1a1-175">El escáner puede indicar cuándo está instalado el alimentador de documentos automático.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-175">The scanner can tell when the automatic document feeder is installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <span data-ttu-id="0d1a1-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-177">Esta propiedad no se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-177">This property is not supported in Windows Vista and later.</span></span> <span data-ttu-id="0d1a1-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-179">Contiene el origen y el modo de adquisición del detector actual. El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-179">Contains the current scanner acquisition source and mode.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-180">Una aplicación Lee esta propiedad para determinar el origen de adquisición actual del escáner o para escribir esta propiedad para establecer el origen y el modo del escáner.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-180">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="0d1a1-181">Además, las aplicaciones usan esta propiedad para habilitar y deshabilitar la funcionalidad de dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-181">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="0d1a1-182">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-182">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="0d1a1-183">En la tabla siguiente se incluyen las diez constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-183">The following table has the ten constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-184">Marcas</span><span class="sxs-lookup"><span data-stu-id="0d1a1-184">Flags</span></span></th>
<th><span data-ttu-id="0d1a1-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-186">ALIMENTADOR</span><span class="sxs-lookup"><span data-stu-id="0d1a1-186">FEEDER</span></span></td>
<td><span data-ttu-id="0d1a1-187">Digitalice con el alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-187">Scan using the document feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-188">PLATAFORMA</span><span class="sxs-lookup"><span data-stu-id="0d1a1-188">FLATBED</span></span></td>
<td><span data-ttu-id="0d1a1-189">Digitalice con el escáner plano.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-189">Scan using the flatbed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-190">D</span><span class="sxs-lookup"><span data-stu-id="0d1a1-190">DUPLEX</span></span></td>
<td><span data-ttu-id="0d1a1-191">Digitalice mediante operaciones de dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-191">Scan using duplexer operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-192">AUTO_ADVANCE</span><span class="sxs-lookup"><span data-stu-id="0d1a1-192">AUTO_ADVANCE</span></span></td>
<td><span data-ttu-id="0d1a1-193">Habilita la alimentación automática del documento siguiente después de un examen.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-193">Enables automatic feeding of the next document after a scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-194">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="0d1a1-194">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="0d1a1-195">Busque primero el principio del documento.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-195">Scan the front of the document first.</span></span> <span data-ttu-id="0d1a1-196">Este valor es válido cuando se establece dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-196">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-197">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="0d1a1-197">BACK_FIRST</span></span></td>
<td><span data-ttu-id="0d1a1-198">Digitalice primero la parte posterior del documento.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-198">Scan the back of the document first.</span></span> <span data-ttu-id="0d1a1-199">Este valor es válido cuando se establece dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-199">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-200">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="0d1a1-200">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="0d1a1-201">Examinar solo la parte frontal.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-201">Scan the front only.</span></span> <span data-ttu-id="0d1a1-202">Este valor es válido cuando se establece dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-202">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-203">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="0d1a1-203">BACK_ONLY</span></span></td>
<td><span data-ttu-id="0d1a1-204">Examinar solo la copia.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-204">Scan the back only.</span></span> <span data-ttu-id="0d1a1-205">Este valor es válido cuando se establece dúplex.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-205">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-206">NEXT_PAGE</span><span class="sxs-lookup"><span data-stu-id="0d1a1-206">NEXT_PAGE</span></span></td>
<td><span data-ttu-id="0d1a1-207">Examinar la página siguiente del documento.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-207">Scan the next page of the document.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-208">Alimentación prefuente</span><span class="sxs-lookup"><span data-stu-id="0d1a1-208">PREFEED</span></span></td>
<td><span data-ttu-id="0d1a1-209">Habilita el modo de fuente previa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-209">Enable pre-feed mode.</span></span> <span data-ttu-id="0d1a1-210">Coloca el siguiente documento antes de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-210">Pre-position next document while scanning.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <span data-ttu-id="0d1a1-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-212">Contiene el estado actual del escáner plano, el alimentador de documentos o el dúplex instalado del escáner.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-212">Contains current state of the scanner's installed flatbed, document feeder, or duplexer.</span></span> <span data-ttu-id="0d1a1-213">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-213">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-214">Una aplicación Lee esta propiedad para determinar si el dispositivo de escáner está listo para usarse.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-214">An application reads this property to determine whether the scanner device is ready to be used.</span></span> <span data-ttu-id="0d1a1-215">Esta es una manera ideal de comprobar si el papel está en el alimentador antes de adquirir una imagen.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-215">This is an ideal way to check whether paper is in the feeder prior to acquiring an image.</span></span></p>
<p><span data-ttu-id="0d1a1-216">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-216">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-217">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad. Un asterisco \* indica que la marca no es compatible con Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-217">The following table has the constants that are valid with this property.An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="0d1a1-218">El símbolo <strong>V</strong> indica que la marca solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-218">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-219">Marcas</span><span class="sxs-lookup"><span data-stu-id="0d1a1-219">Flags</span></span></th>
<th><span data-ttu-id="0d1a1-220">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-220">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-221">FEED_READY</span><span class="sxs-lookup"><span data-stu-id="0d1a1-221">FEED_READY</span></span></td>
<td><span data-ttu-id="0d1a1-222">El plano está listo para su uso.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-222">The flatbed is ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-223">FLAT_READY</span><span class="sxs-lookup"><span data-stu-id="0d1a1-223">FLAT_READY</span></span></td>
<td><span data-ttu-id="0d1a1-224">El escáner tiene un documento en la placa de escáner.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-224">The scanner has a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-225">DUP_READY</span><span class="sxs-lookup"><span data-stu-id="0d1a1-225">DUP_READY</span></span></td>
<td><span data-ttu-id="0d1a1-226">El dúplex está habilitado y listo para usarse.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-226">The duplexer is enabled and ready to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-227">FLAT_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="0d1a1-227">FLAT_COVER_UP</span></span></td>
<td><span data-ttu-id="0d1a1-228">La cubierta plana está activa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-228">The flat bed cover is up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-229">PATH_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="0d1a1-229">PATH_COVER_UP</span></span></td>
<td><span data-ttu-id="0d1a1-230">La ruta de papel está actualizada y impide el funcionamiento correcto.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-230">The paper path is covered up and is preventing proper operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-231">PAPER_JAM</span><span class="sxs-lookup"><span data-stu-id="0d1a1-231">PAPER_JAM</span></span></td>
<td><span data-ttu-id="0d1a1-232">Se atasca un documento en el alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-232">A document is jammed in the document feeder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-233">FILM_TPA_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-233">FILM_TPA_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="0d1a1-234">El adaptador de transparencia está instalado y listo para su uso.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-234">The transparency adapter is installed and ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-235">STORAGE_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-235">STORAGE_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="0d1a1-236">El dispositivo de almacenamiento interno está listo.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-236">The internal storage device is ready.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-237">STORAGE_FULL<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-237">STORAGE_FULL<strong>V</strong></span></span></td>
<td><span data-ttu-id="0d1a1-238">El almacenamiento está lleno, no se pueden realizar operaciones de carga.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-238">The storage is full, no upload operations possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-239">MULTIPLE_FEED<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-239">MULTIPLE_FEED<strong>V</strong></span></span></td>
<td><span data-ttu-id="0d1a1-240">Se produjo una condición de fuente múltiple (normalmente con una PAPER_JAM).</span><span class="sxs-lookup"><span data-stu-id="0d1a1-240">A multiple feed condition occurred (usually with a PAPER_JAM).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-241">DEVICE_ATTENTION<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-241">DEVICE_ATTENTION<strong>V</strong></span></span></td>
<td><span data-ttu-id="0d1a1-242">Hay un error que requiere la intervención del usuario en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-242">There is an error that requires user intervention on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-243">LAMP_ERR<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-243">LAMP_ERR<strong>V</strong></span></span></td>
<td><span data-ttu-id="0d1a1-244">El escáner no está listo debido a un problema de luz.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-244">The scanner is not ready due to a lamp problem.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <span data-ttu-id="0d1a1-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-246">Contiene todos los caracteres válidos que una aplicación puede utilizar para crear cadenas de aprobador válidas.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-246">Contains all the valid characters that an application can use to create valid endorser strings.</span></span> <span data-ttu-id="0d1a1-247">Un aprobador es una impresora instalada en un escáner que imprime un mensaje de texto en cada página examinada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-247">An endorser is a printer installed on a scanner that imprints a text message on every page scanned.</span></span> <span data-ttu-id="0d1a1-248">El minicontrolador debe validar el valor de la propiedad <strong>WIA_DPS_ENDORSER_STRING</strong> con el juego de caracteres válido en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-248">The minidriver should validate the setting of the <strong>WIA_DPS_ENDORSER_STRING</strong> property against the valid character set in this property.</span></span> <span data-ttu-id="0d1a1-249">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-249">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-250">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-250">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <span data-ttu-id="0d1a1-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-252">Contiene una cadena que se va a aprobar (en otras palabras, impresa) en cada página que el minicontrolador explora.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-252">Contains a string that is to be endorsed (in other words, printed) on each page that the minidriver scans.</span></span> <span data-ttu-id="0d1a1-253">Una aplicación establece esta propiedad utilizando el juego de caracteres válido que se muestra en la propiedad <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d1a1-253">An application sets this property using the valid character set that is reported in the <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> property.</span></span> <span data-ttu-id="0d1a1-254">El minicontrolador debe aprobar los documentos solo si se establece una cadena en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-254">The minidriver should endorse documents only if a string is set in this property.</span></span> <span data-ttu-id="0d1a1-255">Una cadena vacía significa que la funcionalidad del aprobador está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-255">An empty string means that the endorser functionality is disabled.</span></span></p>
<p><span data-ttu-id="0d1a1-256">Dado que es responsabilidad del controlador interpretar la cadena del aprobador, el controlador puede usar caracteres especiales en <strong>WIA_DPS_ENDORSER_STRING</strong>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-256">Because it is the driver's responsibility to interpret the endorser string, your driver can use special characters in <strong>WIA_DPS_ENDORSER_STRING</strong>.</span></span> <span data-ttu-id="0d1a1-257">Sin embargo, solo las aplicaciones entienden estos caracteres.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-257">However, only your applications would understand these characters.</span></span></p>
<p><span data-ttu-id="0d1a1-258">Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-258">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-259">Un controlador que admita la propiedad <strong>WIA_DPS_ENDORSER_STRING</strong> debe admitir la siguiente lista de tokens.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-259">A driver supporting the <strong>WIA_DPS_ENDORSER_STRING</strong> property must support the following list of tokens.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-260">Token</span><span class="sxs-lookup"><span data-stu-id="0d1a1-260">Token</span></span></th>
<th><span data-ttu-id="0d1a1-261">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-262">$DATE $</span><span class="sxs-lookup"><span data-stu-id="0d1a1-262">$DATE$</span></span></td>
<td><span data-ttu-id="0d1a1-263">La fecha en el formato AAAA/MM/DD.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-263">The date in the form YYYY/MM/DD.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-264">$DAY $</span><span class="sxs-lookup"><span data-stu-id="0d1a1-264">$DAY$</span></span></td>
<td><span data-ttu-id="0d1a1-265">El día del formulario DD.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-265">The day in the form DD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-266">$MONTH $</span><span class="sxs-lookup"><span data-stu-id="0d1a1-266">$MONTH$</span></span></td>
<td><span data-ttu-id="0d1a1-267">Mes del año en el formato MM.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-267">The month of the year in the form MM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-268">$PAGE _COUNT $</span><span class="sxs-lookup"><span data-stu-id="0d1a1-268">$PAGE_COUNT$</span></span></td>
<td><span data-ttu-id="0d1a1-269">Número de páginas transferidas.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-269">The number of pages transferred.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-270">$TIME $</span><span class="sxs-lookup"><span data-stu-id="0d1a1-270">$TIME$</span></span></td>
<td><span data-ttu-id="0d1a1-271">La hora del día con el formato HH: MM: SS.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-271">The time of day in the form HH:MM:SS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-272">$YEAR $</span><span class="sxs-lookup"><span data-stu-id="0d1a1-272">$YEAR$</span></span></td>
<td><span data-ttu-id="0d1a1-273">El año del formulario YYYY.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-273">The year in the form YYYY.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <span data-ttu-id="0d1a1-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-275">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-275">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="0d1a1-276">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <span data-ttu-id="0d1a1-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-278">Esta propiedad solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-278">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-279">Contiene la dirección SOAP de un dispositivo de analizador de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-279">Contains the SOAP address of a web services scanner device.</span></span> <span data-ttu-id="0d1a1-280">El controlador mini de WIA 2,0 crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-280">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-281">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-281">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <span data-ttu-id="0d1a1-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-283">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-283">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-284">Contiene el registro, o la alineación horizontal, de los documentos colocados en el plano.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-284">Contains the registration, or horizontal alignment, for documents placed on the flatbed.</span></span> <span data-ttu-id="0d1a1-285">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-285">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-286">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-286">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-287">En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-287">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-288">Constante</span><span class="sxs-lookup"><span data-stu-id="0d1a1-288">Constant</span></span></th>
<th><span data-ttu-id="0d1a1-289">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-290">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="0d1a1-290">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="0d1a1-291">El papel está justificado a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-291">The paper is left justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-292">CENTRADO</span><span class="sxs-lookup"><span data-stu-id="0d1a1-292">CENTERED</span></span></td>
<td><span data-ttu-id="0d1a1-293">El papel está centrado.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-293">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-294">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="0d1a1-294">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="0d1a1-295">El papel está justificado a la derecha.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-295">The paper is right justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0d1a1-296"><strong>Vea también</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-296"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="0d1a1-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <span data-ttu-id="0d1a1-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-299">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-299">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="0d1a1-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-301">Especifica el ancho máximo, en milésimas de pulgada, que se analiza en el eje horizontal (X) de la placa de un escáner plano en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-301">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="0d1a1-302">Esta propiedad también se aplica a los alimentadores de documentos automáticos que mueven las hojas a la placa de un escáner plano para su digitalización.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-302">This property also applies to automatic document feeders that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="0d1a1-303">Esta propiedad es obligatoria para los escáneres que tienen una placa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-303">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="0d1a1-304">En su lugar, otros tipos de escáner implementarán la propiedad <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d1a1-304">Other scanner types will instead implement the <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="0d1a1-305">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-305">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="0d1a1-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-307">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-307">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="0d1a1-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-309">Especifica el ancho máximo, en milésimas de pulgada, que se examina en el eje horizontal (X) de un escáner de alimentación de mano o de papel en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-309">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="0d1a1-310">Esta propiedad también se aplica a los alimentadores de documentos automáticos que examinan sin mover hojas a la plancha de un escáner plano.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-310">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="0d1a1-311">Esta propiedad es obligatoria para los escáneres de alimentación de hojas, de avance y de alimentación.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-311">This property is mandatory for sheet-fed, scroll-fed, and hand-held scanners.</span></span></p>
<p><span data-ttu-id="0d1a1-312">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <span data-ttu-id="0d1a1-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-314">Contiene el tiempo máximo para examinar una sola página con la configuración de propiedades actual, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-314">Contains the maximum time to scan a single page with the current property settings, in milliseconds.</span></span> <span data-ttu-id="0d1a1-315">Una aplicación Lee esta propiedad para estimar el tiempo que se tardará en digitalizar una página.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-315">An application reads this property to estimate the time it will take to scan a page.</span></span> <span data-ttu-id="0d1a1-316">Esto resulta útil a la hora de determinar las condiciones de un dispositivo que ha dejado de responder.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-316">This is helpful when determining the conditions of a device that has stopped responding.</span></span> <span data-ttu-id="0d1a1-317">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-317">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="0d1a1-318">Esta propiedad es necesaria para todos los escáneres.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-318">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="0d1a1-319">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-319">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="0d1a1-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-321">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-321">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="0d1a1-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-323">Contiene las dimensiones horizontales físicas de la página más pequeña que el alimentador de documentos del escáner puede escanear, en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-323">Contains the physical horizontal dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="0d1a1-324">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-324">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-325">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-325">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-326"><strong>Vea también</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-326"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="0d1a1-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="0d1a1-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-329">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-329">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="0d1a1-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-331">Contiene las dimensiones físicas verticales de la página más pequeña que el alimentador de documentos del escáner puede escanear, en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-331">Contains the physical vertical dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="0d1a1-332">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-332">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-333">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-333">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-334"><strong>Vea también</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-334"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="0d1a1-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <span data-ttu-id="0d1a1-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-337">Esta propiedad no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-337">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="0d1a1-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-339">Resolución óptica horizontal.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-339">Horizontal Optical Resolution.</span></span> <span data-ttu-id="0d1a1-340">Resolución óptica horizontal más alta admitida en PPP.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-340">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="0d1a1-341">Esta propiedad es un valor único.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-341">This property is a single value.</span></span> <span data-ttu-id="0d1a1-342">Esta no es una lista de todas las resoluciones que puede generar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-342">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="0d1a1-343">En su lugar, se trata de la resolución de los medios ópticos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-343">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="0d1a1-344">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-344">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="0d1a1-345">Esta propiedad es necesaria para todos los escáneres.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-345">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="0d1a1-346">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-346">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <span data-ttu-id="0d1a1-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-348">Esta propiedad no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-348">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="0d1a1-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-350">Resolución óptica vertical.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-350">Vertical Optical Resolution.</span></span> <span data-ttu-id="0d1a1-351">Resolución óptica vertical más alta admitida en PPP.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-351">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="0d1a1-352">Esta propiedad es un valor único.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-352">This property is a single value.</span></span> <span data-ttu-id="0d1a1-353">Esta no es una lista de todas las resoluciones que genera el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-353">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="0d1a1-354">En su lugar, se trata de la resolución de los medios ópticos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-354">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="0d1a1-355">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-355">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="0d1a1-356">Esta propiedad es necesaria para todos los escáneres.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-356">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="0d1a1-357">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-357">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <span data-ttu-id="0d1a1-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-359">Contiene la configuración de orientación actual. El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-359">Contains the current orientation setting.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-360">Una aplicación establece la propiedad <strong>WIA_DPS_ORIENTATION</strong> para definir la orientación original de una página o imagen que se va a adquirir.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-360">An application sets the <strong>WIA_DPS_ORIENTATION</strong> property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="0d1a1-361">Para obtener información sobre cómo usar WIA_DPS_ORIENTATION, vea <strong>WIA_DPS_PAGE_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-361">For information on how to use WIA_DPS_ORIENTATION, see <strong>WIA_DPS_PAGE_SIZE</strong></span></span></p>
<p><span data-ttu-id="0d1a1-362">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-362">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0d1a1-363">En la tabla siguiente se muestran las cuatro constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-363">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-364">Value</span><span class="sxs-lookup"><span data-stu-id="0d1a1-364">Value</span></span></th>
<th><span data-ttu-id="0d1a1-365">La DEFINT</span><span class="sxs-lookup"><span data-stu-id="0d1a1-365">Defination</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-366">HORIZ</span><span class="sxs-lookup"><span data-stu-id="0d1a1-366">LANDSCAPE</span></span></td>
<td><span data-ttu-id="0d1a1-367">rotación de 90 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-367">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-368">VERTICAL</span><span class="sxs-lookup"><span data-stu-id="0d1a1-368">PORTRAIT</span></span></td>
<td><span data-ttu-id="0d1a1-369">0 grados.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-369">0 degrees.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-370">ROT180</span><span class="sxs-lookup"><span data-stu-id="0d1a1-370">ROT180</span></span></td>
<td><span data-ttu-id="0d1a1-371">rotación de 180 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-371">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-372">ROT270</span><span class="sxs-lookup"><span data-stu-id="0d1a1-372">ROT270</span></span></td>
<td><span data-ttu-id="0d1a1-373">rotación de 270 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-373">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0d1a1-374"><strong>Vea también</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-374"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="0d1a1-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <span data-ttu-id="0d1a1-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-377">Color que se usa para rellenar cuando no hay suficientes datos de imagen para rellenar un búfer solicitado.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-377">Color used to pad when there is not enough image data to fill a requested buffer.</span></span> <span data-ttu-id="0d1a1-378">Esta propiedad se implementa para los escáneres que rellenan el búfer.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-378">This property is implemented for scanners that pad the buffer.</span></span> <span data-ttu-id="0d1a1-379">Esta propiedad es opcional para todos los escáneres.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-379">This property is optional for all scanners.</span></span> <span data-ttu-id="0d1a1-380">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-380">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-381">Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Access: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-381">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-382">El formato de la información de color es <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-382">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <span data-ttu-id="0d1a1-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-384">Esta propiedad no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-384">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="0d1a1-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-386">Contiene el alto, en milésimas de pulgada, de la página seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-386">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="0d1a1-387">El minicontrolador crea y mantiene la propiedad <strong>WIA_DPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d1a1-387">The minidriver creates and maintains the <strong>WIA_DPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="0d1a1-388">Una aplicación Lee esta propiedad para determinar las dimensiones físicas de la página que se está examinando.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-388">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="0d1a1-389">Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad informa del alto de la página cuya propiedad <strong>WIA_DPS_PAGE_SIZE</strong> está establecida en WIA_PAGE_CUSTOM (que es un valor de la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="0d1a1-389">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_DPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="0d1a1-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> debe estar sincronizada con <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que indica el alto, en píxeles, de la página que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> must be in sync with <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="0d1a1-391">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <span data-ttu-id="0d1a1-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-393">Esta propiedad no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-393">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="0d1a1-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-395">Contiene el tamaño de la página seleccionada actualmente para su examen.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-395">Contains the size of the page that is currently selected to be scanned.</span></span> <span data-ttu-id="0d1a1-396">Para seleccionar las dimensiones de la página que se va a examinar, una aplicación establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-396">To select the dimensions of the page to scan, an application sets this property.</span></span> <span data-ttu-id="0d1a1-397">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-397">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-398">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-398">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0d1a1-399">En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-399">The following table has the three constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-400">Value</span><span class="sxs-lookup"><span data-stu-id="0d1a1-400">Value</span></span></th>
<th><span data-ttu-id="0d1a1-401">Definición</span><span class="sxs-lookup"><span data-stu-id="0d1a1-401">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-402">WIA_PAGE_A4</span><span class="sxs-lookup"><span data-stu-id="0d1a1-402">WIA_PAGE_A4</span></span></td>
<td><span data-ttu-id="0d1a1-403">8267 X 11692 (orientación vertical)</span><span class="sxs-lookup"><span data-stu-id="0d1a1-403">8267 X 11692 (PORTRAIT orientation)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-404">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="0d1a1-404">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="0d1a1-405">Definido por los valores de las propiedades <strong>WIA_DPS_PAGE_HEIGHT</strong> y <strong>WIA_DPS_PAGE_WIDTH</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-405">Defined by the values of the <strong>WIA_DPS_PAGE_HEIGHT</strong> and <strong>WIA_DPS_PAGE_WIDTH</strong> properties</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-406">WIA_PAGE_LETTER</span><span class="sxs-lookup"><span data-stu-id="0d1a1-406">WIA_PAGE_LETTER</span></span></td>
<td><span data-ttu-id="0d1a1-407">8500 X 11000 (orientación vertical)</span><span class="sxs-lookup"><span data-stu-id="0d1a1-407">8500 X 11000 (PORTRAIT orientation)</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0d1a1-408">El valor de la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> determina la orientación de la página seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-408">The value of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="0d1a1-409">Las propiedades <strong>WIA_DPS_PAGE_WIDTH</strong> y <strong>WIA_DPS_PAGE_HEIGHT</strong> notifican las dimensiones de la página, en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-409">The <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="0d1a1-410">Tenga en cuenta que estas propiedades deben estar en acuerdo con <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong>, que contienen las dimensiones de la página en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-410">Note that these properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span> <span data-ttu-id="0d1a1-411">Los valores válidos de tipo WIA_PROP_LIST deben depender de valores válidos de la propiedad <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d1a1-411">Valid values of type WIA_PROP_LIST should depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="0d1a1-412">Si el dispositivo no puede examinar documentos orientados horizontalmente con un valor de WIA_PAGE_A4, WIA_PAGE_A4 no debe aparecer en la lista de valores válidos para la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> cuando <strong>WIA_IPS_ORIENTATION</strong> está establecida en LANSCAPE.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-412">If the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 should not appear in the list of valid values for the <strong>WIA_DPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANSCAPE.</span></span></p>
<p><span data-ttu-id="0d1a1-413">Si una aplicación establece <strong>WIA_DPS_PAGE_SIZE</strong> en cualquier valor distinto de WIA_PAGE_CUSTOM, el minicontrolador debe ajustar los valores de <strong>WIA_DPS_PAGE_WIDTH</strong> y <strong>WIA_DPS_PAGE_HEIGHT</strong> a las dimensiones de la página en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-413">If an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to any value other than WIA_PAGE_CUSTOM, the minidriver should adjust the values of <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="0d1a1-414">También debe ajustar los valores de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> y <strong>WIA_IPS_YEXTENT</strong> a las dimensiones de la página en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-414">It should also adjust the values of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="0d1a1-415">Si una configuración de extensión (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> o <strong>WIA_IPS_YEXTENT</strong>) se cambia a un valor que no coincide con la configuración de tamaño de página actual, el minicontrolador debe cambiar el valor de la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> a WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-415">If an extent setting (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page-size setting, the minidriver should change the value of the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="0d1a1-416">El minicontrolador también debe modificar <strong>WIA_DPS_PAGE_WIDTH</strong> o <strong>WIA_DPS_PAGE_HEIGHT</strong> de acuerdo con la nueva configuración de extensión.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-416">The minidriver should also modify <strong>WIA_DPS_PAGE_WIDTH</strong> or <strong>WIA_DPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="0d1a1-417">Si <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> se establece en LANSCAPE, se volteará la configuración de la extensión &quot; . &quot; Por ejemplo, si una aplicación establece <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_A4, el minicontrolador debe establecer <strong>WIA_DPS_PAGE_WIDTH</strong> en 11692 y <strong>WIA_DPS_PAGE_HEIGHT</strong> en 8267.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-417">If <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> is set to LANSCAPE, the extent settings will be &quot;flipped.&quot; For example, if an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver should set <strong>WIA_DPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_DPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="0d1a1-418">(El minicontrolador también debe establecer <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong> en consecuencia). Tenga en cuenta que si <strong>WIA_DPS_PAGE_SIZE</strong> está establecido en WIA_PAGE_CUSTOM, el valor de orientación no se utiliza para determinar las dimensiones de extensión de la página que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-418">(The minidriver should also set <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.) Note that if <strong>WIA_DPS_PAGE_SIZE</strong> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span></p>
<p><span data-ttu-id="0d1a1-419">El minicontrolador es responsable de garantizar que la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> está en acuerdo con el área de selección actual.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-419">The minidriver is responsible for ensuring that the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property is in agreement with the current selection area.</span></span> <span data-ttu-id="0d1a1-420">Si una aplicación cambia el valor de <strong>WIA_IPS_ORIENTATION</strong> a uno que no es válido para el tamaño de página seleccionado actualmente, el minicontrolador debe cambiar el valor de <strong>WIA_DPS_PAGE_SIZE</strong> a un tamaño de página compatible con el nuevo valor de orientación.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-420">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_DPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="0d1a1-421">Si una aplicación establece la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_CUSTOM, el área de selección actual no se ve afectada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-421">If an application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="0d1a1-422">El minicontrolador WIA debe obtener el diseño de la imagen actual, a partir de la configuración actual de las propiedades <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> y <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d1a1-422">The WIA minidriver should obtain the current image layout, starting from the current settings of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="0d1a1-423">Si la configuración de tamaño de página da como resultado un área de selección que está fuera de la cama del escáner, el minicontrolador debe ajustar automáticamente los valores de las propiedades <strong>WIA_IPS_XPOS</strong> y <strong>WIA_IPS_YPOS</strong> a valores válidos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-423">If the page-size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="0d1a1-424">Si las propiedades <strong>WIA_DPS_PAGE_SIZE</strong> y <strong>WIA_IPS_ORIENTATION</strong> se establecen al mismo tiempo y no son válidas cuando se aplican en combinación, el minicontrolador debe generar un error en la configuración de la aplicación devolviendo un error en <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-424">If the <strong>WIA_DPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span> <span data-ttu-id="0d1a1-425">.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-425">.</span></span></p>
<p><span data-ttu-id="0d1a1-426">En los cuatro ejemplos siguientes se muestran distintos escenarios de <strong>WIA_DPS_PAGE_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d1a1-426">The following four examples show different <strong>WIA_DPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="0d1a1-427">El controlador informa de la configuración.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-427">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="0d1a1-428">Una aplicación establece la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-428">An application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="0d1a1-429">Una aplicación establece la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> en LANSCAPE.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-429">An application sets the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property to LANSCAPE.</span></span></li>
<li><span data-ttu-id="0d1a1-430">Una aplicación cambia la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> a un valor menor.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-430">An application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="0d1a1-431"><strong>Ejemplo 1: el minicontrolador informa de la configuración</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-431"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="0d1a1-432">En el ejemplo siguiente, el minicontrolador establece un área de selección personalizada antes de que una aplicación establezca las propiedades de WIA.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-432">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="0d1a1-433">En este caso, el área de selección representa todo el plano.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-433">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="0d1a1-434"><strong>Ejemplo 2: una aplicación establece la</strong> <strong></strong><strong>propiedad WIA_DPS_PAGE_SIZE en WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="0d1a1-434"><strong>Example 2: An application sets the</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="0d1a1-435"><strong>Ejemplo 3: una aplicación establece la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>propiedad WIA_IPS_ORIENTATION en LANSCAPE</strong>  </span><span class="sxs-lookup"><span data-stu-id="0d1a1-435"><strong>Example 3: An application sets the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>property to LANSCAPE</strong></span></span></p>
<p><span data-ttu-id="0d1a1-436">La cama física debe ser capaz de adquirir una página que estaba originalmente en orientación horizontal.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-436">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="0d1a1-437"><strong>Ejemplo 4: una aplicación cambia la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>propiedad WIA_IPS_XEXTENT a un valor más pequeño</strong>  </span><span class="sxs-lookup"><span data-stu-id="0d1a1-437"><strong>Example 4: An application changes the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="0d1a1-438">En el ejemplo siguiente, una aplicación cambia la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> a 1000.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-438">In the following example, an application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to 1000.</span></span> <span data-ttu-id="0d1a1-439">El minicontrolador debe asumir que el nuevo valor incluido en <strong>WIA_IPS_XEXTENT</strong> ya no es válido para la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> y, por tanto, debe cambiar <strong>WIA_DPS_PAGE_SIZE</strong> a WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-439">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_DPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="0d1a1-440">El minicontrolador también debe ajustar <strong>WIA_DPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-440">The minidriver must also adjust <strong>WIA_DPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <span data-ttu-id="0d1a1-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-442">Esta propiedad no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-442">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="0d1a1-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-444">Contiene el ancho de la página actual seleccionada, en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-444">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="0d1a1-445">Una aplicación Lee esta propiedad para determinar las dimensiones físicas de la página que se está examinando.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-445">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="0d1a1-446">Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad informa del ancho de la página cuya propiedad <strong>WIA_DPS_PAGE_SIZE</strong> está establecida en WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-446">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="0d1a1-447"><strong>WIA_DPS_PAGE_WIDTH</strong> debe estar sincronizado con el valor de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que notifica el ancho, en píxeles, de la página que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-447"><strong>WIA_DPS_PAGE_WIDTH</strong> must be in sync with the value of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="0d1a1-448">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-448">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-449">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-449">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <span data-ttu-id="0d1a1-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-451">Esta propiedad no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-451">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="0d1a1-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-453">Contiene el número actual de páginas que se van a adquirir de un alimentador de documentos automático.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-453">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="0d1a1-454">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-454">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-455">Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (cero a través del número máximo de páginas que puede contener el alimentador de documentos)</span><span class="sxs-lookup"><span data-stu-id="0d1a1-455">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero through the maximum number of pages that the document feeder can hold)</span></span></p>
<p><span data-ttu-id="0d1a1-456">Una aplicación Lee esta propiedad para determinar la capacidad de página del alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-456">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="0d1a1-457">La aplicación también establece esta propiedad en el número de páginas que va a examinar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-457">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-458">Si el modo dúplex está habilitado (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> está establecido en alimentador | DÚPLEX), <strong>WIA_DPS_PAGES</strong> sigue siendo igual al número de páginas que se van a examinar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-458">If duplex mode is enabled (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-459">Una hoja de papel contendrá automáticamente dos páginas si está habilitada la opción dúplex, incluso si la parte posterior de la página está en blanco.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-459">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="0d1a1-460">Al establecer <strong>WIA_DPS_PAGES</strong> en 1, un escáner procesa uno de los lados de la página.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-460">Setting <strong>WIA_DPS_PAGES</strong> to 1 causes a scanner to process one of the sides of the page.</span></span> <span data-ttu-id="0d1a1-461">Se recomienda que, si un escáner no puede examinar solo un lado de una página en modo dúplex, el <strong>WIA_DPS_PAGES</strong> valor válido para el miembro Inc de la estructura WIA_PROPERTY_INFO debe cambiarse a 2.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-461">It is recommended that if a scanner is unable to scan only one side of a page while in duplex mode, the <strong>WIA_DPS_PAGES</strong> valid value for the Inc member of the WIA_PROPERTY_INFO structure should be changed to 2.</span></span> <span data-ttu-id="0d1a1-462">Este valor indica a la aplicación que debe solicitar páginas en múltiplos de dos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-462">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="0d1a1-463">Un valor de cero significa que <em>todas</em> las páginas que están cargadas actualmente en el alimentador de documentos se van a examinar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-463">A value of zero means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <span data-ttu-id="0d1a1-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-465">Especifica el color de la plancha en la parte posterior de la hoja que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-465">Specifies the color of the platen in back of the sheet to be scanned.</span></span> <span data-ttu-id="0d1a1-466">Esta propiedad es opcional para los escáneres que tienen una placa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-466">This property is optional for scanners that have a platen.</span></span> <span data-ttu-id="0d1a1-467">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-467">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-468">Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Access: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-468">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-469">El formato de la información de color es <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-469">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <span data-ttu-id="0d1a1-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-471">Esta propiedad no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-471">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="0d1a1-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-473">Indica el modo de vista previa de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-473">Indicates the preview mode for a device.</span></span> <span data-ttu-id="0d1a1-474">Una aplicación establece esta propiedad para colocar el dispositivo en modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-474">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="0d1a1-475">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-475">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0d1a1-476">En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-476">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-477">Value</span><span class="sxs-lookup"><span data-stu-id="0d1a1-477">Value</span></span></th>
<th><span data-ttu-id="0d1a1-478">Definición</span><span class="sxs-lookup"><span data-stu-id="0d1a1-478">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-479">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="0d1a1-479">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="0d1a1-480">La aplicación realizará un análisis final.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-480">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-481">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="0d1a1-481">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="0d1a1-482">La aplicación realizará un examen de vista previa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-482">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <span data-ttu-id="0d1a1-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0d1a1-484">Contiene un valor que indica si el analizador almacenará en caché las páginas en un búfer del escáner antes de enviarlas a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-484">Contains a value that indicates whether the scanner will cache pages in a scanner buffer before sending them to the application.</span></span></p>
<p><span data-ttu-id="0d1a1-485">Un valor de cero deshabilita el examen hacia tarde y no se recorren las páginas.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-485">A value of zero disables scan ahead and no pages will be scanned ahead.</span></span> <span data-ttu-id="0d1a1-486">Al realizar transferencias de datos normales en el elemento de examen previo almacenado en búfer, se recuperan las páginas almacenadas en búfer.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-486">Doing normal data transfers on the buffered scan-ahead item retrieves the buffered pages.</span></span> <span data-ttu-id="0d1a1-487">No se pueden cambiar las propiedades de WIA durante una operación de exploración.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-487">WIA properties cannot be changed during a scan-ahead operation.</span></span> <span data-ttu-id="0d1a1-488">Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-488">This property is optional.</span></span></p>
<p><span data-ttu-id="0d1a1-489">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de cero al número máximo de páginas que puede contener el alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-489">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <span data-ttu-id="0d1a1-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-491">Esta propiedad solo es compatible con Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-491">This property is supported only by Windows 7 and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-492">Indica el origen de entrada (plano, alimentador de documentos automático o adaptador de digitalización de fil) del que se va a realizar el análisis, o la ubicación de almacenamiento desde la que se van a transferir los datos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-492">Indicates the input source (flatbed, automatic document feeder, or fil-scanning adapter) to scan from, or the storage location to transfer data from.</span></span></p>
<p><span data-ttu-id="0d1a1-493">Un evento de examen notifica a la aplicación que el usuario ha iniciado un examen, pero el evento no proporciona el nombre del elemento WIA que representa el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-493">A scan event notifies the application that the user has initiated a scan, but the event does not supply the name of the WIA item that represents the input source.</span></span> <span data-ttu-id="0d1a1-494">El controlador de eventos de la aplicación puede consultar la propiedad WIA_DPS_SCAN_AVAILABLE_ITEM del elemento raíz para obtener el nombre del elemento de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-494">The application's event handler can query the root item's WIA_DPS_SCAN_AVAILABLE_ITEM property to get the name of the input source item.</span></span></p>
<p><span data-ttu-id="0d1a1-495">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de cero al número máximo de páginas que puede contener el alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-495">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <span data-ttu-id="0d1a1-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-497">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-497">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-498">Contiene el identificador de servicio de un dispositivo de escáner de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-498">Contains the Service ID of a Web Services scanner device.</span></span> <span data-ttu-id="0d1a1-499">El controlador mini de WIA 2,0 crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-499">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-500">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-500">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <span data-ttu-id="0d1a1-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-502">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-502">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="0d1a1-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-504">Contiene el registro, la alineación y la detección de bordes, para los documentos que se colocan en el plano.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-504">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="0d1a1-505">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-505">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="0d1a1-506">Esta propiedad indica cómo se coloca horizontalmente la hoja en el encabezado de digitalización de un escáner de mano o de alimentación de hojas.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-506">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="0d1a1-507">La propiedad se usa para predecir dónde se coloca un documento en el encabezado del examen.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-507">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="0d1a1-508">En el caso de los escáneres que admiten más de un encabezado de examen, esta propiedad es relativa al encabezado de examen superior.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-508">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="0d1a1-509">Esta propiedad es obligatoria para los escáneres de alimentación de hojas, de desplazamiento y de mano.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-509">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="0d1a1-510">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-510">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-511">En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-511">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-512">Constante</span><span class="sxs-lookup"><span data-stu-id="0d1a1-512">Constant</span></span></th>
<th><span data-ttu-id="0d1a1-513">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-513">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-514">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="0d1a1-514">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="0d1a1-515">La hoja se coloca a la izquierda con respecto al encabezado de digitalización.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-515">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-516">CENTRADO</span><span class="sxs-lookup"><span data-stu-id="0d1a1-516">CENTERED</span></span></td>
<td><span data-ttu-id="0d1a1-517">La hoja está centrada en el encabezado de la digitalización.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-517">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-518">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="0d1a1-518">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="0d1a1-519">La hoja se coloca a la derecha con respecto al encabezado de digitalización.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-519">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <span data-ttu-id="0d1a1-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-521">Esta propiedad no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-521">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="0d1a1-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-523">Indica si un elemento necesita un control de vista previa para el usuario.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-523">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="0d1a1-524">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-524">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-525">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-525">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-526">En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-526">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-527">Constante</span><span class="sxs-lookup"><span data-stu-id="0d1a1-527">Constant</span></span></th>
<th><span data-ttu-id="0d1a1-528">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-528">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-529">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="0d1a1-529">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="0d1a1-530">Mostrar un control de vista previa al usuario, ya que este dispositivo puede realizar una vista previa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-530">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="0d1a1-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="0d1a1-532">No muestre un control de vista previa al usuario, ya que este dispositivo no puede realizar una vista previa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-532">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <span data-ttu-id="0d1a1-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-534">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-534">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-535">Lo usa el servicio WIA para informar al controlador de la cuenta de usuario sobre el nombre de la cuenta de usuario (incluido el nombre de dominio de red cuando proceda) de la sesión en la que se está ejecutando la aplicación WIA actual.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-535">Used by the WIA service to inform the mini-driver about the user account name (including the network domain name when applicable) of the session in which the current WIA application is running.</span></span></p>
<p><span data-ttu-id="0d1a1-536">Se trata de una propiedad de elemento raíz, administrada por el servicio WIA.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-536">This is a root item property, managed by the WIA service.</span></span></p>
<p><span data-ttu-id="0d1a1-537">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-537">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <span data-ttu-id="0d1a1-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-539">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-539">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-540">Contiene el registro, o la alineación vertical y la detección de bordes, para los documentos colocados en el plano.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-540">Contains the registration, or vertical alignment and edge detection, for documents placed on the flatbed.</span></span> <span data-ttu-id="0d1a1-541">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-541">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0d1a1-542">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-542">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0d1a1-543">En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-543">The following table has the three constants that are valid with this property..</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d1a1-544">Constante</span><span class="sxs-lookup"><span data-stu-id="0d1a1-544">Constant</span></span></th>
<th><span data-ttu-id="0d1a1-545">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d1a1-545">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d1a1-546">TOP_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="0d1a1-546">TOP_JUSTIFIED</span></span></td>
<td><span data-ttu-id="0d1a1-547">El papel está justificado en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-547">The paper is top justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d1a1-548">CENTRADO</span><span class="sxs-lookup"><span data-stu-id="0d1a1-548">CENTERED</span></span></td>
<td><span data-ttu-id="0d1a1-549">El papel está centrado.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-549">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d1a1-550">BOTTOM_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="0d1a1-550">BOTTOM_JUSTIFIED</span></span></td>
<td><span data-ttu-id="0d1a1-551">El papel está justificado en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-551">The paper is bottom justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0d1a1-552"><strong>Vea también</strong>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-552"><strong>See Also</strong>.</span></span></p>
<p><span data-ttu-id="0d1a1-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="0d1a1-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <span data-ttu-id="0d1a1-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-555">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-555">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="0d1a1-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-557">Especifica el alto máximo, en milésimas de pulgada, que se examina en el eje vertical (Y) de la placa de un escáner plano en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-557">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="0d1a1-558">Esta propiedad también se aplica a los alimentadores de documentos automáticos, que mueven las hojas a la placa de un escáner plano para su digitalización.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-558">This property also applies to automatic document feeders, that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="0d1a1-559">Esta propiedad es obligatoria para los escáneres que tienen una placa.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-559">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="0d1a1-560">En su lugar, otros tipos de escáner implementarán la propiedad <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d1a1-560">Other scanner types will instead implement the <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="0d1a1-561">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="0d1a1-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0d1a1-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0d1a1-563">Esta propiedad no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-563">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="0d1a1-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0d1a1-565">Especifica el alto máximo, en milésimas de pulgada, que se examina en el eje vertical (Y) de un escáner de alimentación de mano o de papel en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-565">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="0d1a1-566">Esta propiedad también se aplica a los alimentadores de documentos automáticos que examinan sin mover hojas a la plancha de un escáner plano.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-566">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="0d1a1-567">Esta propiedad es obligatoria para los escáneres alimentados por hojas.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-567">This property is mandatory for sheet-fed scanners.</span></span> <span data-ttu-id="0d1a1-568">Los escáneres de avance y de alimentación manual no deben implementar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0d1a1-568">Scroll-fed and hand-held scanners should not implement this property.</span></span></p>
<p><span data-ttu-id="0d1a1-569">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0d1a1-569">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="0d1a1-570">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d1a1-570">Requirements</span></span>



| <span data-ttu-id="0d1a1-571">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d1a1-571">Requirement</span></span> | <span data-ttu-id="0d1a1-572">Value</span><span class="sxs-lookup"><span data-stu-id="0d1a1-572">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1a1-573">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d1a1-573">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1a1-574">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0d1a1-574">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0d1a1-575">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d1a1-575">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1a1-576">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d1a1-576">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d1a1-577">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d1a1-577">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1a1-578"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d1a1-578"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
