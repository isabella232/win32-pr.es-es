---
title: Crear perfiles
description: Crear perfiles
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media Format SDK, perfiles
- perfiles, crear
- perfiles, interfaz IWMProfileManager
- IWMProfileManager, creación de perfiles
- perfiles, función WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077287"
---
# <a name="creating-profiles"></a><span data-ttu-id="4257b-109">Crear perfiles</span><span class="sxs-lookup"><span data-stu-id="4257b-109">Creating Profiles</span></span>

<span data-ttu-id="4257b-110">En muchos casos, querrá crear un perfil vacío para configurar según sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="4257b-110">In many cases, you will want to create an empty profile to configure for your needs.</span></span> <span data-ttu-id="4257b-111">En otros casos, es más fácil editar un perfil existente, como un perfil del sistema.</span><span class="sxs-lookup"><span data-stu-id="4257b-111">In other cases it is easier to edit an existing profile, like a system profile.</span></span> <span data-ttu-id="4257b-112">Para obtener más información sobre el uso de perfiles del sistema, vea [usar perfiles del sistema](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="4257b-112">For more information about using system profiles, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="4257b-113">La creación de un perfil vacío, listo para su configuración, requiere un objeto de administrador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="4257b-113">Creating an empty profile, ready for you to configure, requires a profile manager object.</span></span> <span data-ttu-id="4257b-114">Para obtener la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de un objeto de administrador de perfiles, llame a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="4257b-114">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>

<span data-ttu-id="4257b-115">Para crear un perfil vacío, llame a [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="4257b-115">To create an empty profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span> <span data-ttu-id="4257b-116">Cuando se crea un perfil vacío, lo único que se especifica es la versión del SDK de Windows Media Format con el que cumple el perfil.</span><span class="sxs-lookup"><span data-stu-id="4257b-116">When you create an empty profile, the only thing you specify is the version of the Windows Media Format SDK with which the profile complies.</span></span> <span data-ttu-id="4257b-117">A menos que tenga una necesidad específica de usar una versión anterior, debe usar siempre la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="4257b-117">Unless you have a specific need to use a previous version, you should always use the latest version.</span></span> <span data-ttu-id="4257b-118">La versión dicta la estructura del perfil; las versiones anteriores no eran compatibles con algunas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4257b-118">The version dictates the structure of the profile; previous versions did not support some properties.</span></span>

<span data-ttu-id="4257b-119">En el ejemplo de código siguiente se muestra cómo crear un nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="4257b-119">The following example code shows how to create a new profile.</span></span> <span data-ttu-id="4257b-120">Para compilar este código en la aplicación, incluya stdio. h.</span><span class="sxs-lookup"><span data-stu-id="4257b-120">To compile this code in your application, include stdio.h.</span></span> <span data-ttu-id="4257b-121">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="4257b-121">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="4257b-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4257b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4257b-123">**Interfaz IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="4257b-123">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="4257b-124">**Interfaz IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="4257b-124">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="4257b-125">**Trabajar con perfiles**</span><span class="sxs-lookup"><span data-stu-id="4257b-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




