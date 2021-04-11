---
title: Usar tipos de exclusión mutua personalizados
description: Usar tipos de exclusión mutua personalizados
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- exclusión mutua, interfaz IWMMutualExclusion
- exclusión mutua, tipos personalizados
- perfiles, tipos de exclusión mutua personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149084"
---
# <a name="using-custom-mutual-exclusion-types"></a><span data-ttu-id="2cf8f-107">Usar tipos de exclusión mutua personalizados</span><span class="sxs-lookup"><span data-stu-id="2cf8f-107">Using Custom Mutual Exclusion Types</span></span>

<span data-ttu-id="2cf8f-108">Puede usar objetos de exclusión mutua en un perfil para satisfacer las necesidades de escenarios personalizados.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-108">You can use mutual exclusion objects in a profile to meet the needs of custom scenarios.</span></span> <span data-ttu-id="2cf8f-109">Al pasar el valor de GUID \_ WMMUTEX \_ Unknown a [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), se informa al objeto de exclusión mutua de que se está usando un escenario personalizado.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-109">By passing the GUID value CLSID\_WMMUTEX\_Unknown to [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), you inform the mutual exclusion object that you are using a custom scenario.</span></span>

<span data-ttu-id="2cf8f-110">Debe controlar manualmente la selección de flujos cuando lee un archivo con un valor de exclusión mutua personalizado.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-110">You must manually control stream selection when you read a file with a custom mutual exclusion value.</span></span> <span data-ttu-id="2cf8f-111">El objeto de lector usará la primera secuencia que agregue a la exclusión mutua como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-111">The reader object will use the first stream you add to the mutual exclusion as the default.</span></span>

<span data-ttu-id="2cf8f-112">Use los pasos siguientes para crear un objeto de exclusión mutua personalizado y agregarlo a un perfil:</span><span class="sxs-lookup"><span data-stu-id="2cf8f-112">Use the following steps to create a custom mutual exclusion object and add it to a profile:</span></span>

1.  <span data-ttu-id="2cf8f-113">Cree un administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="2cf8f-113">Create a profile manager by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="2cf8f-114">Comience con un perfil existente o cree uno totalmente nuevo.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-114">Either start with an existing profile, or create an entirely new one.</span></span>
    -   <span data-ttu-id="2cf8f-115">Si usa un perfil existente, llame a uno de los métodos Load de la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="2cf8f-115">If you are using an existing profile, call one of the load methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="2cf8f-116">Después, vaya al paso 4.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-116">Then skip to step 4.</span></span>
    -   <span data-ttu-id="2cf8f-117">Si va a crear un perfil completamente nuevo, llame a [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="2cf8f-117">If you are creating an entirely new profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span>
3.  <span data-ttu-id="2cf8f-118">Agregue secuencias al nuevo perfil llamando a [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span><span class="sxs-lookup"><span data-stu-id="2cf8f-118">Add streams to the new profile by calling [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span></span> <span data-ttu-id="2cf8f-119">Configure las secuencias según sea necesario mediante los métodos de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="2cf8f-119">Configure the streams as needed using the methods of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span> <span data-ttu-id="2cf8f-120">También puede llamar a **QueryInterface** para tener acceso a otras interfaces en el objeto de configuración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-120">You can also call **QueryInterface** to access other interfaces in the stream configuration object.</span></span>

    <span data-ttu-id="2cf8f-121">**CreateNewStream** solo crea un objeto de configuración de flujo y no afecta al perfil.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-121">**CreateNewStream** creates only a stream configuration object, and does not affect the profile.</span></span> <span data-ttu-id="2cf8f-122">Después de configurar correctamente un flujo, debe llamar a [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para agregar la secuencia al perfil.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-122">After a stream is configured properly, you must call [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add the stream to the profile.</span></span>

4.  <span data-ttu-id="2cf8f-123">Cree un objeto de exclusión mutua mediante una llamada a [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="2cf8f-123">Create a mutual exclusion object by calling [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span></span>
5.  <span data-ttu-id="2cf8f-124">Agregue las secuencias deseadas al objeto de exclusión mutua mediante una llamada a [**IWMStreamList:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponible directamente desde [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), que hereda de [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span><span class="sxs-lookup"><span data-stu-id="2cf8f-124">Add the desired streams to the mutual exclusion object by calling [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (available directly from [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), which inherits from [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span></span>
6.  <span data-ttu-id="2cf8f-125">Establezca el tipo de exclusión mutua en personalizado mediante una llamada a [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="2cf8f-125">Set the type of mutual exclusion to custom by calling [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span> <span data-ttu-id="2cf8f-126">Pase el CLSID \_ WMMUTEX \_ desconocido como el GUID de tipo.</span><span class="sxs-lookup"><span data-stu-id="2cf8f-126">Pass the CLSID\_WMMUTEX\_Unknown as the type GUID.</span></span>
7.  <span data-ttu-id="2cf8f-127">Agregue el objeto de exclusión mutua configurado al perfil mediante una llamada a [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="2cf8f-127">Add the configured mutual exclusion object to the profile by calling [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cf8f-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cf8f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cf8f-129">**Interfaz IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="2cf8f-129">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="2cf8f-130">**Interfaz IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="2cf8f-130">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="2cf8f-131">**Interfaz IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="2cf8f-131">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="2cf8f-132">**Interfaz IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="2cf8f-132">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="2cf8f-133">**Interfaz IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="2cf8f-133">**IWMStreamList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[<span data-ttu-id="2cf8f-134">**Usar exclusión mutua**</span><span class="sxs-lookup"><span data-stu-id="2cf8f-134">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="2cf8f-135">**WMCreateProfileManager**</span><span class="sxs-lookup"><span data-stu-id="2cf8f-135">**WMCreateProfileManager**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




