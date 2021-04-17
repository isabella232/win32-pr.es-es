---
description: El conjunto de propiedades protección de copia de DVD proporciona autenticación de la información de protección de copia de los descifrados de hardware o software. Use esta propiedad establecida para evitar la copia no autorizada de DVD-video grabado previamente.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Conjunto de propiedades de protección de copia de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680922"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="f2654-104">Conjunto de propiedades de protección de copia de DVD</span><span class="sxs-lookup"><span data-stu-id="f2654-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="f2654-105">El conjunto de propiedades protección de copia de DVD proporciona autenticación de la información de protección de copia de los descifrados de hardware o software.</span><span class="sxs-lookup"><span data-stu-id="f2654-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="f2654-106">Use esta propiedad establecida para evitar la copia no autorizada de DVD-video grabado previamente.</span><span class="sxs-lookup"><span data-stu-id="f2654-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="f2654-107">Microsoft proporciona software que facilita el proceso de autenticación requerido por el esquema de cifrado, lo que permite que una unidad de DVD-ROM autentique y transfiera claves con un DVD Decrypter.</span><span class="sxs-lookup"><span data-stu-id="f2654-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="f2654-108">Microsoft no tiene planes actuales para enviar un DVD Decrypter y, en su lugar, proporciona código del sistema operativo que actuará como agente para habilitar la autenticación de los descifrados de hardware o software.</span><span class="sxs-lookup"><span data-stu-id="f2654-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="f2654-109">El navegador de DVD inicia y controla el proceso de intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="f2654-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="f2654-110">El minicontrolador de DVD solo tiene que implementar las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="f2654-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="f2654-111">Otros componentes controlan el resto.</span><span class="sxs-lookup"><span data-stu-id="f2654-111">Other components handle the rest.</span></span>

<span data-ttu-id="f2654-112">Cada flujo de entrada de DVD recibirá las propiedades de protección contra copia.</span><span class="sxs-lookup"><span data-stu-id="f2654-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="f2654-113">Esto es así incluso si el mismo hardware controla todos los flujos de DVD.</span><span class="sxs-lookup"><span data-stu-id="f2654-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="f2654-114">La siguiente información presenta las constantes y los tipos de datos necesarios para usar en esta propiedad establecida en llamadas a métodos [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="f2654-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="f2654-115">Proporciona valores para los parámetros **GUID** (*GUIDPROPSET*), ID. de propiedad (*dwPropID*) y tipo de datos de propiedad (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="f2654-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="f2654-116">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="f2654-116">Property Set GUID</span></span> | <span data-ttu-id="f2654-117">\_CopyProt KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="f2654-117">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2654-118">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="f2654-118">Property ID</span></span></th>
<th><span data-ttu-id="f2654-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2654-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2654-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2654-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="f2654-121">Consulta si la salida de vídeo es una definición estándar, vídeo de componente analógico.</span><span class="sxs-lookup"><span data-stu-id="f2654-121">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2654-122">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="f2654-122">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="f2654-123">Esta es una propiedad de solo conjunto.</span><span class="sxs-lookup"><span data-stu-id="f2654-123">This is a set-only property.</span></span> <span data-ttu-id="f2654-124">Esta propiedad establece el nivel de protección de copia analógica del codificador NTSC en el extremo de salida del PIN receptor.</span><span class="sxs-lookup"><span data-stu-id="f2654-124">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="f2654-125">Utiliza <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2654-125">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2654-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="f2654-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="f2654-127">En esta propiedad se admiten las operaciones GET y set.</span><span class="sxs-lookup"><span data-stu-id="f2654-127">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="f2654-128">Una operación Get solicita al descodificador que proporcione su clave de desafío de bus.</span><span class="sxs-lookup"><span data-stu-id="f2654-128">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="f2654-129">Una operación SET proporciona el descodificador con la clave de desafío de bus de la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="f2654-129">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="f2654-130">Los datos pasados en esta propiedad serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2654-130">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2654-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="f2654-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="f2654-132">Se trata de una propiedad de solo obtención.</span><span class="sxs-lookup"><span data-stu-id="f2654-132">This is a get-only property.</span></span> <span data-ttu-id="f2654-133">Esta propiedad solicita que la clave de bus 2 del descodificador se transfiera a la unidad de DVD.</span><span class="sxs-lookup"><span data-stu-id="f2654-133">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="f2654-134">Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2654-134">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2654-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="f2654-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="f2654-136">Propiedad de solo establecimiento.</span><span class="sxs-lookup"><span data-stu-id="f2654-136">Set-only property.</span></span> <span data-ttu-id="f2654-137">Esto proporciona la clave de disco.</span><span class="sxs-lookup"><span data-stu-id="f2654-137">This provides disc key.</span></span> <span data-ttu-id="f2654-138">La clave es una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2654-138">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2654-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="f2654-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="f2654-140">Esta es una propiedad de solo conjunto.</span><span class="sxs-lookup"><span data-stu-id="f2654-140">This is a set-only property.</span></span> <span data-ttu-id="f2654-141">Esta propiedad proporciona la clave 1 del bus de unidad de DVD al descodificador.</span><span class="sxs-lookup"><span data-stu-id="f2654-141">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="f2654-142">Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2654-142">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2654-143">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="f2654-143">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="f2654-144">El código de región solicita la definición de la región en la que el descodificador puede reproducirse tal y como se define en el consorcio de DVD.</span><span class="sxs-lookup"><span data-stu-id="f2654-144">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="f2654-145">Esta región se define como una estructura de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f2654-145">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2654-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="f2654-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="f2654-147">En esta propiedad se admiten get y set.</span><span class="sxs-lookup"><span data-stu-id="f2654-147">Both get and set are supported on this property.</span></span> <span data-ttu-id="f2654-148">Primero se llama a get para determinar si se requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="f2654-148">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="f2654-149">Las propiedades establecidas son indicaciones sobre la fase de negociación de la protección de copia que el filtro está entrando.</span><span class="sxs-lookup"><span data-stu-id="f2654-149">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="f2654-150">Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2654-150">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2654-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="f2654-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="f2654-152">Si esta propiedad es <strong>true</strong>, el explorador de DVD no envía <strong>AM_UseNewCSSKey</strong> muestras antes de negociar la clave de disco.</span><span class="sxs-lookup"><span data-stu-id="f2654-152">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="f2654-153">Vea <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2654-153">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="f2654-154">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f2654-154">Read-only.</span></span> <span data-ttu-id="f2654-155">Los datos de la propiedad son un valor <strong>booleano</strong> .</span><span class="sxs-lookup"><span data-stu-id="f2654-155">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f2654-156">Se aplica a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f2654-156">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2654-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="f2654-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="f2654-158">Esta es una propiedad de solo conjunto.</span><span class="sxs-lookup"><span data-stu-id="f2654-158">This is a set-only property.</span></span> <span data-ttu-id="f2654-159">Esto proporciona la clave de título del contenido actual.</span><span class="sxs-lookup"><span data-stu-id="f2654-159">This provides title key from current content.</span></span> <span data-ttu-id="f2654-160">La clave es una estructura de tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2654-160">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="f2654-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2654-161">Requirements</span></span>



| <span data-ttu-id="f2654-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2654-162">Requirement</span></span> | <span data-ttu-id="f2654-163">Value</span><span class="sxs-lookup"><span data-stu-id="f2654-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2654-164">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2654-164">Header</span></span><br/> | <dl> <span data-ttu-id="f2654-165"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2654-165"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2654-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2654-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2654-167">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="f2654-167">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




