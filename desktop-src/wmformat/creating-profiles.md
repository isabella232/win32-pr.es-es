---
title: Crear perfiles
description: Crear perfiles
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows SDK de formato multimedia, perfiles
- profiles,creating
- profiles,IWMProfileManager (interfaz)
- IWMProfileManager, crear perfiles
- profiles,función WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570248"
---
# <a name="creating-profiles"></a>Crear perfiles

En muchos casos, querrá crear un perfil vacío para configurarlo para sus necesidades. En otros casos, es más fácil editar un perfil existente, como un perfil del sistema. Para obtener más información sobre el uso de perfiles de sistema, vea [Using System Profiles](using-system-profiles.md).

La creación de un perfil vacío, listo para configurarlo, requiere un objeto de administrador de perfiles. Para obtener la [**interfaz IWMProfileManager de**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) un objeto de administrador de perfiles, llame a la [**función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)

Para crear un perfil vacío, llame a [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile). Cuando se crea un perfil vacío, lo único que se especifica es la versión del SDK de formato multimedia de Windows con el que se cumple el perfil. A menos que tenga una necesidad específica de usar una versión anterior, siempre debe usar la versión más reciente. La versión determina la estructura del perfil; las versiones anteriores no admiten algunas propiedades.

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

 

 




