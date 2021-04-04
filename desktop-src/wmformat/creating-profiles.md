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
# <a name="creating-profiles"></a>Crear perfiles

En muchos casos, querrá crear un perfil vacío para configurar según sus necesidades. En otros casos, es más fácil editar un perfil existente, como un perfil del sistema. Para obtener más información sobre el uso de perfiles del sistema, vea [usar perfiles del sistema](using-system-profiles.md).

La creación de un perfil vacío, listo para su configuración, requiere un objeto de administrador de perfiles. Para obtener la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de un objeto de administrador de perfiles, llame a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .

Para crear un perfil vacío, llame a [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile). Cuando se crea un perfil vacío, lo único que se especifica es la versión del SDK de Windows Media Format con el que cumple el perfil. A menos que tenga una necesidad específica de usar una versión anterior, debe usar siempre la versión más reciente. La versión dicta la estructura del perfil; las versiones anteriores no eran compatibles con algunas propiedades.

En el ejemplo de código siguiente se muestra cómo crear un nuevo perfil. Para compilar este código en la aplicación, incluya stdio. h. Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).


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

[**Interfaz IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interfaz IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




