---
title: Para configurar Quality-Based VBR
description: Para configurar Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- flujos, configurar secuencias VBR
- secuencias, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- flujos, configurar VBR basada en la calidad
- velocidad de bits variable (VBR), configurar basado en la calidad
- VBR (velocidad de bits variable), configuración basada en la calidad
- perfiles, configuración de VBR basada en la calidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103995020"
---
# <a name="to-configure-quality-based-vbr"></a><span data-ttu-id="e6cbf-111">Para configurar Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="e6cbf-111">To Configure Quality-Based VBR</span></span>

<span data-ttu-id="e6cbf-112">Puede usar la codificación de velocidad de bits variable (VBR) basada en la calidad en una secuencia para especificar un nivel de calidad que se mantendrá para todo el flujo, independientemente de los requisitos de velocidad de bits que resulten.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-112">You can use quality-based variable bit rate (VBR) encoding on a stream to specify a quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>

<span data-ttu-id="e6cbf-113">En el caso de las secuencias de vídeo VBR basadas en la calidad, debe especificar un nivel de calidad de 1 a 100, con 100 que representa la calidad más alta.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-113">For quality-based VBR video streams, you must specify a quality level from 1 to 100, with 100 representing the highest quality.</span></span> <span data-ttu-id="e6cbf-114">En la actualidad, solo hay 30 valores de calidad discretos.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-114">At present there are only 30 discrete quality settings.</span></span> <span data-ttu-id="e6cbf-115">Los siguientes niveles de calidad son equivalentes a los valores de calidad discretos: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-115">The following quality levels equate to discrete quality settings: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span></span> <span data-ttu-id="e6cbf-116">Los números entre dos valores consecutivos de la lista anterior equivalen a la misma configuración de calidad que el número inferior.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-116">Numbers between two consecutive values in the preceding list equate to the same quality setting as the lower number.</span></span> <span data-ttu-id="e6cbf-117">Por ejemplo, 1 y 4 se enumeran, por lo que 2 y 3 dan como resultado la misma configuración de calidad que 1.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-117">For example, 1 and 4 are listed, so 2 and 3 both result in the same quality setting as 1.</span></span>

<span data-ttu-id="e6cbf-118">En el caso de las secuencias de audio, puede enumerar los modos disponibles y recuperar un objeto de configuración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-118">For audio streams, you can enumerate the available modes and retrieve a stream configuration object.</span></span> <span data-ttu-id="e6cbf-119">Para obtener más información, vea [para enumerar los formatos de códec](to-enumerate-codec-formats.md).</span><span class="sxs-lookup"><span data-stu-id="e6cbf-119">For more information, see [To Enumerate Codec Formats](to-enumerate-codec-formats.md).</span></span>

<span data-ttu-id="e6cbf-120">Al usar el vídeo VBR basado en la calidad, debe establecer el miembro **dwBitrate** de la estructura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) en un valor positivo.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-120">When using quality-based VBR video, you must set the **dwBitrate** member of the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to a positive value.</span></span> <span data-ttu-id="e6cbf-121">El escritor no usa este valor, pero si se pasa cero o un número negativo, se pueden producir errores al escribir.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-121">This value is not used by the writer, but passing zero or a negative number can cause errors when writing.</span></span>

<span data-ttu-id="e6cbf-122">Para configurar una secuencia en un perfil que se va a codificar con VBR basada en la calidad, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-122">To configure a stream in a profile to be encoded with quality-based VBR, perform the following steps.</span></span>

1.  <span data-ttu-id="e6cbf-123">Cree un objeto de administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="e6cbf-123">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="e6cbf-124">Abra un perfil existente al que desee agregar compatibilidad con VBR.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-124">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="e6cbf-125">Para obtener más información acerca de la apertura de perfiles, consulte [trabajar con perfiles](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="e6cbf-125">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="e6cbf-126">Obtenga un objeto de configuración de secuencia para la secuencia que desea usar llamando a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="e6cbf-126">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="e6cbf-127">Obtiene un puntero a la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de la secuencia llamando a **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-127">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="e6cbf-128">Habilite VBR para la secuencia mediante una llamada a [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para la propiedad **\_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="e6cbf-128">Enable VBR for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="e6cbf-129">Establezca el nivel de calidad de la secuencia VBR llamando a **IWMPropertyVault:: SetProperty** para la propiedad **\_ wszVBRQuality** .</span><span class="sxs-lookup"><span data-stu-id="e6cbf-129">Set the quality level for the VBR stream by calling **IWMPropertyVault::SetProperty** for the **g\_wszVBRQuality** property.</span></span>
7.  <span data-ttu-id="e6cbf-130">Establezca **g \_ wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax** en cero con **IWMPropertyVault:: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-130">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
8.  <span data-ttu-id="e6cbf-131">Guarde los cambios realizados en la secuencia mediante una llamada a [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="e6cbf-131">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
9.  <span data-ttu-id="e6cbf-132">Guarde el perfil o páselo al objeto escritor y empiece a escribir.</span><span class="sxs-lookup"><span data-stu-id="e6cbf-132">Save the profile, or pass it to the writer object and start writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6cbf-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6cbf-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6cbf-134">**Configuración de secuencias VBR**</span><span class="sxs-lookup"><span data-stu-id="e6cbf-134">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




