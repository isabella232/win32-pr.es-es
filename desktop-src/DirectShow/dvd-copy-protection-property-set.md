---
description: El conjunto de propiedades de protección de copia de DVD proporciona autenticación de la información de protección de copia de descifradores de hardware o software. Use esta propiedad establecida para evitar la copia no autorizada de DVD-Video grabado previamente.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Conjunto de propiedades de protección de copia de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909483"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="f3714-104">Conjunto de propiedades de protección de copia de DVD</span><span class="sxs-lookup"><span data-stu-id="f3714-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="f3714-105">El conjunto de propiedades protección de copia de DVD proporciona autenticación de la información de protección de copia de descifradores de hardware o software.</span><span class="sxs-lookup"><span data-stu-id="f3714-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="f3714-106">Use esta propiedad establecida para evitar la copia no autorizada de DVD-Video grabado previamente.</span><span class="sxs-lookup"><span data-stu-id="f3714-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="f3714-107">Microsoft proporciona software que facilita el proceso de autenticación requerido por el esquema de cifrado, lo que permite que una unidad DE DVD-ROM autentique y transfiera claves con un descifrador de DVD.</span><span class="sxs-lookup"><span data-stu-id="f3714-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="f3714-108">Microsoft no tiene planes actuales para enviar un descifrador de DVD y, en su lugar, proporciona código de sistema operativo que actuará como agente para habilitar la autenticación de descifradores de hardware o software.</span><span class="sxs-lookup"><span data-stu-id="f3714-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="f3714-109">El navegador de DVD inicia y controla el proceso de intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="f3714-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="f3714-110">El minidriver de DVD solo necesita implementar las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3714-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="f3714-111">Otros componentes controlan el resto.</span><span class="sxs-lookup"><span data-stu-id="f3714-111">Other components handle the rest.</span></span>

<span data-ttu-id="f3714-112">Cada flujo de entrada de DVD recibirá las propiedades de protección de copia.</span><span class="sxs-lookup"><span data-stu-id="f3714-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="f3714-113">Esto es así incluso si el mismo hardware controla todas las secuencias de DVD.</span><span class="sxs-lookup"><span data-stu-id="f3714-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="f3714-114">En la siguiente información se presentan las constantes y los tipos de datos necesarios que se usarán para este conjunto de propiedades en las llamadas a [**los métodos IKsPropertySet.**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="f3714-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="f3714-115">Proporciona valores para los parámetros **GUID** (*guidPropSet*), property ID (*dwPropID*) y property data type (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="f3714-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="f3714-116">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="f3714-116">Label</span></span> | <span data-ttu-id="f3714-117">Value</span><span class="sxs-lookup"><span data-stu-id="f3714-117">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="f3714-118">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="f3714-118">Property Set GUID</span></span> | <span data-ttu-id="f3714-119">CopyProt de \_ AM KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="f3714-119">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3714-120">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="f3714-120">Property ID</span></span></th>
<th><span data-ttu-id="f3714-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3714-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3714-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3714-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="f3714-123">Consulta si la salida del vídeo es vídeo de componentes análogos de definición estándar.</span><span class="sxs-lookup"><span data-stu-id="f3714-123">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3714-124">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="f3714-124">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="f3714-125">Se trata de una propiedad de solo conjunto.</span><span class="sxs-lookup"><span data-stu-id="f3714-125">This is a set-only property.</span></span> <span data-ttu-id="f3714-126">Esta propiedad establece el nivel de protección de copia análoga para el codificador ENCODER en el extremo de salida del pin receptor.</span><span class="sxs-lookup"><span data-stu-id="f3714-126">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="f3714-127">Usa <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f3714-127">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3714-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="f3714-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="f3714-129">En esta propiedad se admiten las operaciones get y set.</span><span class="sxs-lookup"><span data-stu-id="f3714-129">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="f3714-130">Una operación get solicita al descodificador que proporcione su clave de desafío de bus.</span><span class="sxs-lookup"><span data-stu-id="f3714-130">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="f3714-131">Una operación set proporciona al descodificador la clave de desafío de bus de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="f3714-131">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="f3714-132">Los datos pasados en esta propiedad serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f3714-132">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3714-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="f3714-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="f3714-134">Se trata de una propiedad get-only.</span><span class="sxs-lookup"><span data-stu-id="f3714-134">This is a get-only property.</span></span> <span data-ttu-id="f3714-135">Esta propiedad solicita que la clave de bus 2 del descodificador se transfiera a la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="f3714-135">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="f3714-136">Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f3714-136">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3714-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="f3714-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="f3714-138">Propiedad de solo establecimiento.</span><span class="sxs-lookup"><span data-stu-id="f3714-138">Set-only property.</span></span> <span data-ttu-id="f3714-139">Esto proporciona la tecla de disco.</span><span class="sxs-lookup"><span data-stu-id="f3714-139">This provides disc key.</span></span> <span data-ttu-id="f3714-140">La clave es una estructura de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>tipo</strong></a>AM_DVDCOPY_DISCKEY .</span><span class="sxs-lookup"><span data-stu-id="f3714-140">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3714-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="f3714-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="f3714-142">Se trata de una propiedad de solo conjunto.</span><span class="sxs-lookup"><span data-stu-id="f3714-142">This is a set-only property.</span></span> <span data-ttu-id="f3714-143">Esta propiedad proporciona la clave 1 del bus de unidad de DVD al descodificador.</span><span class="sxs-lookup"><span data-stu-id="f3714-143">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="f3714-144">Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f3714-144">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3714-145">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="f3714-145">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="f3714-146">El código de región solicita la definición de región en la que el descodificador puede reproducirse según lo definido por el consorcio de DVD.</span><span class="sxs-lookup"><span data-stu-id="f3714-146">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="f3714-147">Esta región se define como una <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> estructura.</span><span class="sxs-lookup"><span data-stu-id="f3714-147">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3714-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="f3714-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="f3714-149">Tanto get como set se admiten en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f3714-149">Both get and set are supported on this property.</span></span> <span data-ttu-id="f3714-150">Se llama primero a Get para determinar si se requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="f3714-150">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="f3714-151">Las propiedades del conjunto son indicaciones sobre la fase de negociación de la protección de copia que entra el filtro.</span><span class="sxs-lookup"><span data-stu-id="f3714-151">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="f3714-152">Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f3714-152">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3714-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="f3714-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="f3714-154">Si esta propiedad es <strong>TRUE</strong>, el navegador de DVD no envía <strong>AM_UseNewCSSKey</strong> ejemplos antes de negociar la clave de disco.</span><span class="sxs-lookup"><span data-stu-id="f3714-154">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="f3714-155">Vea <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f3714-155">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="f3714-156">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f3714-156">Read-only.</span></span> <span data-ttu-id="f3714-157">Los datos de propiedad son <strong>un valor BOOL.</strong></span><span class="sxs-lookup"><span data-stu-id="f3714-157">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3714-158">Se aplica a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f3714-158">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3714-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="f3714-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="f3714-160">Se trata de una propiedad de solo conjunto.</span><span class="sxs-lookup"><span data-stu-id="f3714-160">This is a set-only property.</span></span> <span data-ttu-id="f3714-161">Esto proporciona la clave de título del contenido actual.</span><span class="sxs-lookup"><span data-stu-id="f3714-161">This provides title key from current content.</span></span> <span data-ttu-id="f3714-162">La clave es una estructura de tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f3714-162">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="f3714-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3714-163">Requirements</span></span>



| <span data-ttu-id="f3714-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3714-164">Requirement</span></span> | <span data-ttu-id="f3714-165">Value</span><span class="sxs-lookup"><span data-stu-id="f3714-165">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3714-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3714-166">Header</span></span><br/> | <dl> <span data-ttu-id="f3714-167"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="f3714-167"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3714-168">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f3714-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3714-169">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="f3714-169">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




