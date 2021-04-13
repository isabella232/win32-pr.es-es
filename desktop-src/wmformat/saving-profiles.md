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
# <a name="saving-profiles"></a>Guardar perfiles

Puede usar el método [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) para guardar el contenido de un objeto de perfil en una cadena con formato XML. No se proporciona ningún método para almacenar la cadena de perfil en un archivo; puede usar las rutinas de e/s de archivo de su elección.

> [!Note]  
> Nunca debe modificar la cadena de perfil escrita en un archivo. Los cambios que desee realizar en un perfil deben realizarse mediante programación. Cambiar los valores en un archivo. prx puede producir resultados imprevisibles.

 

El ejemplo siguiente es una función para guardar un perfil en un archivo mediante la e/s de archivo de estilo C estándar. Para compilar una aplicación que utiliza este ejemplo, debe incluir stdio. h en el proyecto.


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

 

 




