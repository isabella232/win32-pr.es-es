---
title: Para cambiar las versiones de perfil del sistema
description: Para cambiar las versiones de perfil del sistema
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- perfiles, sistema
- perfiles del sistema, versiones
- perfiles del sistema, cambiar versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824e2b1cf4a43cef0e87daa461c6510a6672472d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358696"
---
# <a name="to-change-system-profile-versions"></a><span data-ttu-id="e3d7e-106">Para cambiar las versiones de perfil del sistema</span><span class="sxs-lookup"><span data-stu-id="e3d7e-106">To Change System Profile Versions</span></span>

<span data-ttu-id="e3d7e-107">Siempre que se crea un objeto de administrador de perfiles, se analizan los perfiles del sistema.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-107">Whenever you create a profile manager object, it parses the system profiles.</span></span> <span data-ttu-id="e3d7e-108">Puede recorrer en iteración los perfiles del sistema mediante los métodos [**IWMProfileManager:: GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) y [**IWMProfileManager:: LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) , pero el administrador de perfiles contará y enumerará solo los perfiles de una sola versión cada vez.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-108">You can iterate through the system profiles using the [**IWMProfileManager::GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods, but the profile manager will count and list only the profiles of a single version at a time.</span></span> <span data-ttu-id="e3d7e-109">Si desea utilizar este método de búsqueda de perfiles del sistema, debe asegurarse de que el administrador de perfiles se encarga de la versión que desee.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-109">If you want to use this method of finding system profiles, you need to ensure that the profile manger deals with the version you want.</span></span> <span data-ttu-id="e3d7e-110">Use los métodos de la interfaz [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) para establecer y recuperar la versión de perfil del sistema utilizada por el administrador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-110">Use the methods of the [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) interface to set and retrieve the system profile version used by the profile manager.</span></span>

<span data-ttu-id="e3d7e-111">Las versiones se especifican mediante los miembros del tipo de enumeración de la [**\_ versión WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) .</span><span class="sxs-lookup"><span data-stu-id="e3d7e-111">Versions are specified using the members of the [**WMT\_VERSION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) enumeration type.</span></span> <span data-ttu-id="e3d7e-112">Si establece la versión del perfil del sistema en WMT \_ Ver \_ 9 \_ 0, la llamada se realizará correctamente, pero el número de perfiles del sistema será cero.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-112">If you set the system profile version to WMT\_VER\_9\_0, the call will succeed, but the system profile count will be zero.</span></span> <span data-ttu-id="e3d7e-113">Esto se debe a que ningún perfil del sistema predefinido usa los códecs de la serie Windows Media Audio y vídeo 9.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-113">This is because no predefined system profiles use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="e3d7e-114">Para obtener más información sobre la actualización de perfiles para usar los códecs más recientes, consulte [reutilización de las configuraciones de streaming](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e3d7e-114">For more information about updating profiles to use the newest codecs, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

<span data-ttu-id="e3d7e-115">Si carga un perfil del sistema mediante su identificador GUID, no importa qué versión del perfil del sistema utiliza el administrador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-115">If you load a system profile by its GUID identifier, it does not matter which system profile version the profile manager is using.</span></span> <span data-ttu-id="e3d7e-116">Para obtener más información acerca de la carga de perfiles del sistema, consulte [para cargar un perfil del sistema](to-load-a-system-profile.md).</span><span class="sxs-lookup"><span data-stu-id="e3d7e-116">For more information about loading system profiles, see [To Load a System Profile](to-load-a-system-profile.md).</span></span>

<span data-ttu-id="e3d7e-117">En el ejemplo de código siguiente se muestra cómo establecer y recuperar la versión del perfil del sistema.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-117">The following example code shows how to set and retrieve the system profile version.</span></span> <span data-ttu-id="e3d7e-118">En este ejemplo se usa printf para la salida de la consola y se requiere stdio. h.</span><span class="sxs-lookup"><span data-stu-id="e3d7e-118">This example uses printf for console output and requires stdio.h to be included.</span></span> <span data-ttu-id="e3d7e-119">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="e3d7e-119">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
int main(void)
{
    HRESULT hr = S_OK;

    IWMProfileManager*  pProfileMgr  = NULL;
    IWMProfileManager2* pProfileMgr2 = NULL;

    WMT_VERSION         profileVersion;

    // Initialize COM.
    hr = CoInitialize(NULL);
    if(FAILED(hr))
    {
        printf("Could not initialize COM.");
        return 0;
    }

    // Create a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    if(FAILED(hr))
    {
        printf("Could not create a profile manager object.");
        return 0;
    }

    // Get the IWMProfileManager2 interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManager2, 
                                     (void**) &pProfileMgr2);
    if(FAILED(hr))
    {
        printf("Could not get the IWMProfileManager2 interface.");
        SAFE_RELEASE(pProfileMgr);
        return 0;
    }

    // Release the old interface.
    SAFE_RELEASE(pProfileMgr);

    // Get the current system profile version.
    hr = pProfileMgr2->GetSystemProfileVersion(&profileVersion);
    if(FAILED(hr))
    {
        printf("Could not retrieve profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }
    
    // Display the current version.
    printf("Current version: ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Set the system profile version to 8.
    profileVersion = WMT_VER_8_0;

    hr = pProfileMgr2->SetSystemProfileVersion(profileVersion);
    if(FAILED(hr))
    {
        printf("Could not change profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }

    // Print verification.
    printf("Successfully set version to ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Clean up.
    SAFE_RELEASE(pProfileMgr2);
}
```



## <a name="related-topics"></a><span data-ttu-id="e3d7e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3d7e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3d7e-121">**Usar perfiles del sistema**</span><span class="sxs-lookup"><span data-stu-id="e3d7e-121">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




