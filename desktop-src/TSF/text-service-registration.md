---
title: Registro del servicio de texto
description: Además de las entradas del registro del servidor COM en proceso estándar, un servicio de texto debe registrarse en el marco de trabajo de servicios de texto (TSF) para que pueda estar disponible para su uso con una aplicación.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Text Services Framework (TSF), registro
- TSF (marco de trabajo de servicios de texto), registro
- servicios de texto, registro
- Marco de trabajo de servicios de texto (TSF), perfiles de idioma
- TSF (marco de trabajo de servicios de texto), perfiles de idioma
- servicios de texto, perfiles de idioma
- Text Services Framework (TSF), categorías
- TSF (marco de trabajo de servicios de texto), categorías
- servicios de texto, categorías
- registrando servicios de texto
- registrando perfiles de idioma
- registrar categorías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487975"
---
# <a name="text-service-registration"></a><span data-ttu-id="9ef60-115">Registro del servicio de texto</span><span class="sxs-lookup"><span data-stu-id="9ef60-115">Text Service Registration</span></span>

<span data-ttu-id="9ef60-116">Además de las entradas del registro del servidor COM en proceso estándar, un servicio de texto debe registrarse en el marco de trabajo de servicios de texto (TSF) para que pueda estar disponible para su uso con una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ef60-116">In addition to the standard COM in-proc server registry entries, a text service must register itself with the Text Services Framework (TSF) so that it can be available for use with an application.</span></span> <span data-ttu-id="9ef60-117">TSF proporciona la interfaz [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) y [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) para simplificar el proceso de registro.</span><span class="sxs-lookup"><span data-stu-id="9ef60-117">TSF supplies the [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) and [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) interface to simplify the registration process.</span></span>

<span data-ttu-id="9ef60-118">Los proveedores de servicios de texto también deben proporcionar firmas digitales con sus ejecutables binarios.</span><span class="sxs-lookup"><span data-stu-id="9ef60-118">Text service providers should also provide digital signatures with their binary executables.</span></span> <span data-ttu-id="9ef60-119">Vea [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ef60-119">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="registering-the-text-service"></a><span data-ttu-id="9ef60-120">Registrar el servicio de texto</span><span class="sxs-lookup"><span data-stu-id="9ef60-120">Registering the Text Service</span></span>

<span data-ttu-id="9ef60-121">Un servicio de texto se registra a sí mismo con TSF mediante una llamada a [ITfInputProcessorProfiles:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) con el identificador de clase del servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="9ef60-121">A text service registers itself with TSF by calling [ITfInputProcessorProfiles::Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) with the class identifier of the text service.</span></span> <span data-ttu-id="9ef60-122">Una instancia de la interfaz **ITfInputProcessorProfiles** se obtiene llamando a **COCREATEINSTANCE** con el CLSID \_ TF \_ InputProcessorProfiles.</span><span class="sxs-lookup"><span data-stu-id="9ef60-122">An instance of the **ITfInputProcessorProfiles** interface is obtained by calling **CoCreateInstance** with CLSID\_TF\_InputProcessorProfiles.</span></span>

<span data-ttu-id="9ef60-123">En el ejemplo siguiente se muestra cómo crear un objeto **ITfInputProcessorProfiles** y registrar el servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="9ef60-123">The following example demonstrates how to create an **ITfInputProcessorProfiles** object and register the text service.</span></span>


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[<span data-ttu-id="9ef60-124">ITfInputProcessorProfiles:: unregister</span><span class="sxs-lookup"><span data-stu-id="9ef60-124">ITfInputProcessorProfiles::Unregister</span></span>](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a><span data-ttu-id="9ef60-125">Registrando perfiles de idioma</span><span class="sxs-lookup"><span data-stu-id="9ef60-125">Registering Language Profiles</span></span>

<span data-ttu-id="9ef60-126">Un servicio de texto solo está disponible cuando una aplicación tiene el foco y se selecciona el idioma adecuado en la barra de idioma.</span><span class="sxs-lookup"><span data-stu-id="9ef60-126">A text service is only available when an application has the focus and the proper language is selected in the language bar.</span></span> <span data-ttu-id="9ef60-127">Para facilitar esto, TSF requiere que un servicio de texto se registre en todos los idiomas que admite.</span><span class="sxs-lookup"><span data-stu-id="9ef60-127">To facilitate this, TSF requires that a text service register itself for all of the languages that it supports.</span></span> <span data-ttu-id="9ef60-128">El servicio de texto registra sus perfiles de lenguaje mediante una llamada a [ITfInputProcessorProfiles:: AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) con el identificador de clase de servicio de texto, ese identificador de idioma del perfil y un **GUID** definido por el servicio de texto que identifica el perfil de idioma.</span><span class="sxs-lookup"><span data-stu-id="9ef60-128">The text service registers its language profiles by calling [ITfInputProcessorProfiles::AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) with the text service class identifier, that language identifier of the profile, and a text service defined **GUID** that identifies the language profile.</span></span>

<span data-ttu-id="9ef60-129">Un perfil de idioma se puede quitar llamando a [ITfInputProcessorProfiles:: RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span><span class="sxs-lookup"><span data-stu-id="9ef60-129">A language profile can be removed by calling [ITfInputProcessorProfiles::RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span></span> <span data-ttu-id="9ef60-130">**ITfInputProcessorProfiles:: unregister** quita todos los perfiles de lenguaje para el servicio de texto; Cuando se desinstala un servicio de texto, requiere la eliminación de los perfiles de idioma individuales.</span><span class="sxs-lookup"><span data-stu-id="9ef60-130">**ITfInputProcessorProfiles::Unregister** removes all language profiles for the text service; when a text service is uninstalled, it does require removal of the individual language profiles.</span></span>

## <a name="registering-categories"></a><span data-ttu-id="9ef60-131">Registrar categorías</span><span class="sxs-lookup"><span data-stu-id="9ef60-131">Registering Categories</span></span>

<span data-ttu-id="9ef60-132">Un servicio de texto también debe registrar la categoría a la que se aplica el servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="9ef60-132">A text service must also register the category that the text service applies to.</span></span> <span data-ttu-id="9ef60-133">Por ejemplo, si el servicio de texto proporciona información de atributos de visualización, debe registrarse como un proveedor de atributos para mostrar llamando a [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con el identificador de clase del servicio de texto para el primer parámetro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER para el segundo parámetro y el identificador de clase del servicio de texto de nuevo para el tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="9ef60-133">For example, if the text service supplies display attribute information, it must register itself as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span> <span data-ttu-id="9ef60-134">Las categorías posibles se enumeran en [valores de categoría predefinidos](predefined-category-values.md).</span><span class="sxs-lookup"><span data-stu-id="9ef60-134">The possible categories are listed under [Predefined Category Values](predefined-category-values.md).</span></span>

<span data-ttu-id="9ef60-135">Quite las categorías previamente registradas llamando a [ITfCategoryMgr:: UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span><span class="sxs-lookup"><span data-stu-id="9ef60-135">Remove previously registered categories by calling [ITfCategoryMgr::UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span></span> <span data-ttu-id="9ef60-136">ITfInputProcessorProfiles:: unregister quita todas las categorías para el servicio de texto; Cuando se desinstala un servicio de texto, debe quitar las categorías individuales.</span><span class="sxs-lookup"><span data-stu-id="9ef60-136">ITfInputProcessorProfiles::Unregister removes all categories for the text service; when a text service is uninstalled, it must remove the individual categories.</span></span>

 

 