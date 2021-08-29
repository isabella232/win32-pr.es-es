---
title: Crear perfiles
description: Crear perfiles
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows SDK de formato multimedia, perfiles
- profiles,creating
- profiles,IWMProfileManager (interfaz)
- IWMProfileManager, crear perfiles
- profiles,FUNCIÓN WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19dda9d5eb486227d78c735b497a265d9ffcdf6888531227b0d27d8375482c6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840155"
---
# <a name="creating-profiles"></a>Crear perfiles

En muchos casos, querrá crear un perfil vacío para configurarlo según sus necesidades. En otros casos, es más fácil editar un perfil existente, como un perfil del sistema. Para obtener más información sobre el uso de perfiles del sistema, vea [Using System Profiles](using-system-profiles.md).

La creación de un perfil vacío, listo para configurarlo, requiere un objeto de administrador de perfiles. Para obtener la [**interfaz IWMProfileManager de**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) un objeto de administrador de perfiles, llame a la [**función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)

Para crear un perfil vacío, llame a [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile). Cuando se crea un perfil vacío, lo único que se especifica es la versión del SDK de Windows Formato multimedia con el que cumple el perfil. A menos que tenga una necesidad específica de usar una versión anterior, siempre debe usar la versión más reciente. La versión determina la estructura del perfil; las versiones anteriores no admiten algunas propiedades.

En el código de ejemplo siguiente se muestra cómo crear un nuevo perfil. Para compilar este código en la aplicación, incluya stdio.h. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMProfile (interfaz)**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




