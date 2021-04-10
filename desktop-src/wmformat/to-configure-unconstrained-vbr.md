---
title: Para configurar una VBR sin restricciones
description: Para configurar una VBR sin restricciones
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- flujos, configurar secuencias VBR
- secuencias, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- flujos, configurar VBR sin restricciones
- velocidad de bits variable (VBR), configurar sin restricciones
- VBR (velocidad de bits variable), configurar sin restricciones
- perfiles, configuración de VBR sin restricciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149123"
---
# <a name="to-configure-unconstrained-vbr"></a><span data-ttu-id="92a43-111">Para configurar una VBR sin restricciones</span><span class="sxs-lookup"><span data-stu-id="92a43-111">To Configure Unconstrained VBR</span></span>

<span data-ttu-id="92a43-112">Puede usar la codificación de velocidad de bits variable (VBR) sin restricciones en una secuencia para especificar una velocidad de bits promedio que se mantendrá en el contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="92a43-112">You can use unconstrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="92a43-113">La VBR sin restricciones difiere de los CBR normales en que la desviación en la velocidad de bits a lo largo del flujo puede ser mayor.</span><span class="sxs-lookup"><span data-stu-id="92a43-113">Unconstrained VBR differs from normal CBR in that the variance in bit rate throughout the stream can be greater.</span></span>

<span data-ttu-id="92a43-114">La velocidad de bits de la secuencia, establecida con [**IWMStreamConfig:: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), se usa como la velocidad de bits promedio deseada.</span><span class="sxs-lookup"><span data-stu-id="92a43-114">The bit rate of the stream, set with [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), is used as the desired average bit rate.</span></span> <span data-ttu-id="92a43-115">Cuando se complete la codificación de la secuencia, puede usar [**IWMPropertyVault:: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) para recuperar dos propiedades adicionales: **g \_ wszVBRPeak** y **g \_ wszBufferAverage**.</span><span class="sxs-lookup"><span data-stu-id="92a43-115">When encoding of the stream is complete, you can use [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) to retrieve two additional properties: **g\_wszVBRPeak** and **g\_wszBufferAverage**.</span></span> <span data-ttu-id="92a43-116">Estas propiedades describen la velocidad de bits máxima del contenido codificado y la ventana de búfer promedio del contenido, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="92a43-116">These properties describe the peak bit rate of the encoded content and the average buffer window of the content, respectively.</span></span>

<span data-ttu-id="92a43-117">La VBR sin restricciones debe utilizarse junto con la codificación de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="92a43-117">Unconstrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="92a43-118">La codificación de dos pasos no está establecida en el perfil.</span><span class="sxs-lookup"><span data-stu-id="92a43-118">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="92a43-119">Debe configurar el escritor para realizar un paso de preprocesamiento antes de escribir la secuencia.</span><span class="sxs-lookup"><span data-stu-id="92a43-119">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="92a43-120">Para obtener más información sobre el uso de la codificación de dos pasos, consulte uso de la [codificación de Two-Pass](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="92a43-120">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="92a43-121">Para configurar una secuencia en un perfil que se va a codificar con VBR sin restricciones, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="92a43-121">To configure a stream in a profile to be encoded with unconstrained VBR, perform the following steps:</span></span>

1.  <span data-ttu-id="92a43-122">Cree un objeto de administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="92a43-122">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="92a43-123">Abra un perfil existente al que desee agregar compatibilidad con VBR.</span><span class="sxs-lookup"><span data-stu-id="92a43-123">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="92a43-124">Para obtener más información acerca de la apertura de perfiles, consulte [trabajar con perfiles](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="92a43-124">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="92a43-125">Obtenga un objeto de configuración de secuencia para la secuencia que desea usar llamando a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="92a43-125">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="92a43-126">Obtiene un puntero a la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de la secuencia llamando a **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="92a43-126">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="92a43-127">Habilite la codificación VBR para la secuencia llamando a [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para la **propiedad \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="92a43-127">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="92a43-128">Establezca **g \_ wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax** en cero con **IWMPropertyVault:: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="92a43-128">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
7.  <span data-ttu-id="92a43-129">Guarde los cambios realizados en la secuencia mediante una llamada a [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="92a43-129">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="92a43-130">Guarde el perfil o páselo al objeto escritor.</span><span class="sxs-lookup"><span data-stu-id="92a43-130">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="92a43-131">Configure el escritor para realizar un paso de preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="92a43-131">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92a43-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92a43-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92a43-133">**Configuración de secuencias VBR**</span><span class="sxs-lookup"><span data-stu-id="92a43-133">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




