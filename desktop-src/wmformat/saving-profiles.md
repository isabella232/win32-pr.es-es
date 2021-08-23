---
title: Guardar perfiles
description: Guardar perfiles
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows SDK de formato multimedia, guardar perfiles
- Windows SDK de formato multimedia, guardado de perfiles
- profiles,saving
- profiles,IWMProfileManager (interfaz)
- IWMProfileManager, guardar perfiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6befb09d7e0d628462bdd22e1e905c351be58dc077959089883ce3707dc493d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547045"
---
# <a name="saving-profiles"></a>Guardar perfiles

Puede usar el método [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) para guardar el contenido de un objeto de perfil en una cadena con formato XML. No se proporciona ningún método para almacenar la cadena de perfil en un archivo; puede usar las rutinas de E/S de archivo que prefiera.

> [!Note]  
> Nunca debe modificar la cadena de perfil escrita en un archivo. Los cambios que quiera realizar en un perfil se deben realizar mediante programación. El cambio de valores en un archivo .prx puede provocar resultados impredecibles.

 

El ejemplo siguiente es una función para guardar un perfil en un archivo mediante E/S de archivo de estilo C estándar. Para compilar una aplicación que use este ejemplo, debe incluir stdio.h en el proyecto.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




