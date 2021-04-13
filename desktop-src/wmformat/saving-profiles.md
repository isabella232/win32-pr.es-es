---
title: Guardar perfiles
description: Guardar perfiles
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- SDK de Windows Media Format, guardar perfiles
- SDK de Windows Media Format, almacenamiento de perfiles
- perfiles, guardar
- perfiles, interfaz IWMProfileManager
- IWMProfileManager, guardar perfiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276b002f0b7f98de2e84f2c27a4f52bde25726bb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420240"
---
# <a name="saving-profiles"></a><span data-ttu-id="99d11-108">Guardar perfiles</span><span class="sxs-lookup"><span data-stu-id="99d11-108">Saving Profiles</span></span>

<span data-ttu-id="99d11-109">Puede usar el método [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) para guardar el contenido de un objeto de perfil en una cadena con formato XML.</span><span class="sxs-lookup"><span data-stu-id="99d11-109">You can use the [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) method to save the contents of a profile object to a string formatted with XML.</span></span> <span data-ttu-id="99d11-110">No se proporciona ningún método para almacenar la cadena de perfil en un archivo; puede usar las rutinas de e/s de archivo de su elección.</span><span class="sxs-lookup"><span data-stu-id="99d11-110">No methods are provided to store the profile string to a file; you can use the file I/O routines of your choice.</span></span>

> [!Note]  
> <span data-ttu-id="99d11-111">Nunca debe modificar la cadena de perfil escrita en un archivo.</span><span class="sxs-lookup"><span data-stu-id="99d11-111">You should never alter the profile string written to a file.</span></span> <span data-ttu-id="99d11-112">Los cambios que desee realizar en un perfil deben realizarse mediante programación.</span><span class="sxs-lookup"><span data-stu-id="99d11-112">Any changes you want to make to a profile should be made programmatically.</span></span> <span data-ttu-id="99d11-113">Cambiar los valores en un archivo. prx puede producir resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="99d11-113">Changing values in a .prx file can cause unpredictable results.</span></span>

 

<span data-ttu-id="99d11-114">El ejemplo siguiente es una función para guardar un perfil en un archivo mediante la e/s de archivo de estilo C estándar.</span><span class="sxs-lookup"><span data-stu-id="99d11-114">The following example is a function to save a profile to a file using standard C-style file I/O.</span></span> <span data-ttu-id="99d11-115">Para compilar una aplicación que utiliza este ejemplo, debe incluir stdio. h en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="99d11-115">To compile an application that uses this example, you must include stdio.h in your project.</span></span>


```C++
HRESULT ProfileToFile(IWMProfileManager* pProfileMgr, 
                      IWMProfile* pProfile)
{
    HRESULT hr = S_OK;

    FILE*   pFile;
    
    WCHAR*  pwszProfileString = NULL;
    DWORD   cchProfileString = 0;

    // Save the profile to a string.
    // First, retrieve the size of the string required.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  NULL, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not get the profile string size.");
        return hr;
    }

    // Allocate memory to hold the string.
    pwszProfileString = new WCHAR[cchProfileString];

    if(pwszProfileString == NULL)
    {
        printf("Could not allocate memory for the profile string.");
        return E_OUTOFMEMORY;
    }

    // Retrieve the string.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  pwszProfileString, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not save the profile string.");
        return hr;
    }

    // Create the output file.
    pFile = fopen("MyProfile.prx", "w");

    // Write the profile string to the file.
    fprintf(pFile, "%S\n", pwszProfileString);

    // Close the file.
    fclose(pFile);

    delete[] pwszProfileString;

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="99d11-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99d11-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d11-117">**Trabajar con perfiles**</span><span class="sxs-lookup"><span data-stu-id="99d11-117">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




