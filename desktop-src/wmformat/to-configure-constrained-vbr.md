---
title: Para configurar una VBR restringida
description: Para configurar una VBR restringida
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- flujos, configurar secuencias VBR
- secuencias, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- flujos, configurar VBR restringida
- velocidad de bits variable (VBR), configurar restricciones
- VBR (velocidad de bits variable), configurar restricciones
- perfiles, configuración de VBR restringida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077440"
---
# <a name="to-configure-constrained-vbr"></a><span data-ttu-id="c69f7-111">Para configurar una VBR restringida</span><span class="sxs-lookup"><span data-stu-id="c69f7-111">To Configure Constrained VBR</span></span>

<span data-ttu-id="c69f7-112">Puede usar la codificación de velocidad de bits variable (VBR) restringida en una secuencia para especificar una velocidad de bits promedio que se mantendrá en el contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="c69f7-112">You can use constrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="c69f7-113">También se especifica la velocidad de bits máxima de la secuencia y la ventana de búfer máxima requerida.</span><span class="sxs-lookup"><span data-stu-id="c69f7-113">You also specify the maximum bit rate of the stream and the maximum required buffer window.</span></span>

<span data-ttu-id="c69f7-114">No se puede saber cuál será la velocidad de bits media de una secuencia VBR restringida antes de la codificación, pero se puede usar una estimación aproximada.</span><span class="sxs-lookup"><span data-stu-id="c69f7-114">You cannot know what the average bit rate will be for a constrained VBR stream before encoding, but you can use a rough estimate.</span></span> <span data-ttu-id="c69f7-115">Como norma general, la velocidad de bits máxima que especifique terminará siendo de dos a tres veces la velocidad de bits promedio.</span><span class="sxs-lookup"><span data-stu-id="c69f7-115">As a general rule, the maximum bit rate you specify will end up being two to three times the average bit rate.</span></span>

<span data-ttu-id="c69f7-116">La VBR restringida debe usarse junto con la codificación de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="c69f7-116">Constrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="c69f7-117">La codificación de dos pasos no está establecida en el perfil.</span><span class="sxs-lookup"><span data-stu-id="c69f7-117">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="c69f7-118">Debe configurar el escritor para realizar un paso de preprocesamiento antes de escribir la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c69f7-118">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="c69f7-119">Para obtener más información sobre el uso de la codificación de dos pasos, consulte uso de la [codificación de Two-Pass](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="c69f7-119">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="c69f7-120">Para configurar una secuencia en un perfil para usar la codificación VBR restringida, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c69f7-120">To configure a stream in a profile to use constrained VBR encoding, perform the following steps.</span></span>

1.  <span data-ttu-id="c69f7-121">Cree un objeto de administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="c69f7-121">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="c69f7-122">Abra un perfil existente al que desee agregar compatibilidad con VBR.</span><span class="sxs-lookup"><span data-stu-id="c69f7-122">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="c69f7-123">Para obtener más información acerca de la apertura de perfiles, consulte [trabajar con perfiles](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c69f7-123">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="c69f7-124">Obtenga un objeto de configuración de secuencia para la secuencia que desea usar llamando a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="c69f7-124">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="c69f7-125">Obtiene un puntero a la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de la secuencia llamando a **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c69f7-125">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="c69f7-126">Habilite la codificación VBR para la secuencia llamando a [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para la **propiedad \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="c69f7-126">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="c69f7-127">Use llamadas a **IWMPropertyVault:: SetProperty** para establecer los valores máximos deseados para las propiedades **g \_ wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax** .</span><span class="sxs-lookup"><span data-stu-id="c69f7-127">Use calls to **IWMPropertyVault::SetProperty** to set the desired maximum values for the **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** properties.</span></span>
7.  <span data-ttu-id="c69f7-128">Guarde los cambios realizados en la secuencia mediante una llamada a [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="c69f7-128">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="c69f7-129">Guarde el perfil o páselo al objeto escritor.</span><span class="sxs-lookup"><span data-stu-id="c69f7-129">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="c69f7-130">Configure el escritor para realizar un paso de preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="c69f7-130">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c69f7-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c69f7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c69f7-132">**Configuración de secuencias VBR**</span><span class="sxs-lookup"><span data-stu-id="c69f7-132">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




