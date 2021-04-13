---
title: Para cargar un perfil del sistema
description: Para cargar un perfil del sistema
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- perfiles, sistema
- perfiles del sistema, cargar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420270"
---
# <a name="to-load-a-system-profile"></a><span data-ttu-id="086d5-105">Para cargar un perfil del sistema</span><span class="sxs-lookup"><span data-stu-id="086d5-105">To Load a System Profile</span></span>

<span data-ttu-id="086d5-106">Para realizar cambios en un perfil del sistema, debe cargarlo en un objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="086d5-106">To make changes to a system profile, you must load it into a profile object.</span></span> <span data-ttu-id="086d5-107">El administrador de perfiles proporciona dos opciones para cargar perfiles del sistema: por identificador y por índice.</span><span class="sxs-lookup"><span data-stu-id="086d5-107">The profile manager provides two options for loading system profiles: by identifier, and by index.</span></span>

<span data-ttu-id="086d5-108">Un identificador de Perfil de sistema es un valor GUID asignado al perfil del sistema cuando se creó.</span><span class="sxs-lookup"><span data-stu-id="086d5-108">A system profile identifier is a GUID value assigned to the system profile when it was created.</span></span> <span data-ttu-id="086d5-109">Para obtener una lista de las constantes de GUID asociadas a los perfiles de sistema de la versión 8, vea [perfiles del sistema](system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="086d5-109">For a list of the GUID constants associated with the version 8 system profiles, see [System Profiles](system-profiles.md).</span></span> <span data-ttu-id="086d5-110">Puede encontrar las constantes de GUID para las versiones anteriores en el archivo de encabezado WMSysPrf. h.</span><span class="sxs-lookup"><span data-stu-id="086d5-110">You can find the GUID constants for previous versions in the header file WMSysPrf.h.</span></span> <span data-ttu-id="086d5-111">Para obtener más información sobre este y otros archivos de encabezado incluidos con el SDK de Windows Media Format, consulte [archivos de biblioteca y configuración del compilador](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="086d5-111">For more information about this and other header files included with the Windows Media Format SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

<span data-ttu-id="086d5-112">En el ejemplo de código siguiente se muestra cómo cargar un perfil del sistema mediante el identificador de perfil del sistema.</span><span class="sxs-lookup"><span data-stu-id="086d5-112">The following example code demonstrates how to load a system profile using the system profile identifier.</span></span> <span data-ttu-id="086d5-113">Para que este código funcione, debe incluir WMSysPrf. h y stdio. h.</span><span class="sxs-lookup"><span data-stu-id="086d5-113">For this code to work, you must include WMSysPrf.h and stdio.h.</span></span> <span data-ttu-id="086d5-114">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="086d5-114">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



<span data-ttu-id="086d5-115">Si no sabe qué perfil desea usar, puede recorrer en iteración todos los perfiles del sistema de una determinada versión mediante los métodos [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) y [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) de la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="086d5-115">If you do not know which profile you want to use, you can iterate through all of the system profiles of a particular version using the [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="086d5-116">Estos métodos solo se ocupan de una versión de los perfiles del sistema a la vez.</span><span class="sxs-lookup"><span data-stu-id="086d5-116">These methods only deal with one version of the system profiles at a time.</span></span> <span data-ttu-id="086d5-117">Para obtener más información acerca de cómo cambiar la versión del perfil del sistema, consulte [para cambiar las versiones del perfil del sistema](to-change-system-profile-versions.md).</span><span class="sxs-lookup"><span data-stu-id="086d5-117">For more information about changing the system profile version, see [To Change System Profile Versions](to-change-system-profile-versions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="086d5-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="086d5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="086d5-119">**Usar perfiles del sistema**</span><span class="sxs-lookup"><span data-stu-id="086d5-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




