---
title: Para cambiar las versiones del perfil del sistema
description: Para cambiar las versiones del perfil del sistema
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- profiles,system
- perfiles del sistema, versiones
- perfiles del sistema, cambiar versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824e2b1cf4a43cef0e87daa461c6510a6672472d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359902"
---
# <a name="to-change-system-profile-versions"></a>Para cambiar las versiones del perfil del sistema

Cada vez que se crea un objeto de administrador de perfiles, analiza los perfiles del sistema. Puede recorrer en iteración los perfiles del sistema mediante los métodos [**IWMProfileManager::GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**IWMProfileManager::LoadSystemProfile,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) pero el administrador de perfiles solo contará y enumerará los perfiles de una sola versión a la vez. Si desea usar este método de búsqueda de perfiles del sistema, debe asegurarse de que el administrador de perfiles se ocupa de la versión que desee. Use los métodos de la [**interfaz IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) para establecer y recuperar la versión del perfil del sistema que usa el administrador de perfiles.

Las versiones se especifican mediante los miembros del tipo de [**enumeración WMT \_ VERSION.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) Si establece la versión del perfil del sistema en WMT \_ VER \_ 9 0, la llamada se realizará correctamente, pero el recuento de perfiles del sistema \_ será cero. Esto se debe a que ningún perfil del sistema predefinido usa los códecs Windows media audio y vídeo de la serie 9. Para obtener más información sobre cómo actualizar perfiles para usar los códecs más nuevos, vea [Volver a usar configuraciones de flujo.](reusing-stream-configurations.md)

Si carga un perfil del sistema por su identificador GUID, no importa la versión del perfil del sistema que use el administrador de perfiles. Para obtener más información sobre cómo cargar perfiles del sistema, vea [Para cargar un perfil de sistema.](to-load-a-system-profile.md)

En el código de ejemplo siguiente se muestra cómo establecer y recuperar la versión del perfil del sistema. En este ejemplo se usa printf para la salida de la consola y se requiere que se incluya stdio.h. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de perfiles del sistema**](using-system-profiles.md)
</dt> </dl>

 

 




