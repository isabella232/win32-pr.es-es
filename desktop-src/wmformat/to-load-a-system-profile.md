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
# <a name="to-load-a-system-profile"></a>Para cargar un perfil del sistema

Para realizar cambios en un perfil del sistema, debe cargarlo en un objeto de perfil. El administrador de perfiles proporciona dos opciones para cargar perfiles del sistema: por identificador y por índice.

Un identificador de Perfil de sistema es un valor GUID asignado al perfil del sistema cuando se creó. Para obtener una lista de las constantes de GUID asociadas a los perfiles de sistema de la versión 8, vea [perfiles del sistema](system-profiles.md). Puede encontrar las constantes de GUID para las versiones anteriores en el archivo de encabezado WMSysPrf. h. Para obtener más información sobre este y otros archivos de encabezado incluidos con el SDK de Windows Media Format, consulte [archivos de biblioteca y configuración del compilador](library-files-and-compiler-settings.md).

En el ejemplo de código siguiente se muestra cómo cargar un perfil del sistema mediante el identificador de perfil del sistema. Para que este código funcione, debe incluir WMSysPrf. h y stdio. h. Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).


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



Si no sabe qué perfil desea usar, puede recorrer en iteración todos los perfiles del sistema de una determinada versión mediante los métodos [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) y [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) de la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Estos métodos solo se ocupan de una versión de los perfiles del sistema a la vez. Para obtener más información acerca de cómo cambiar la versión del perfil del sistema, consulte [para cambiar las versiones del perfil del sistema](to-change-system-profile-versions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar perfiles del sistema**](using-system-profiles.md)
</dt> </dl>

 

 




