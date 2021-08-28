---
title: Para cargar un perfil del sistema
description: Para cargar un perfil del sistema
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- profiles,system
- perfiles del sistema, carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becd98903921b81ce1eaf7d2317659c7760bb99c4e55e07efe336719d5d34ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807485"
---
# <a name="to-load-a-system-profile"></a>Para cargar un perfil del sistema

Para realizar cambios en un perfil del sistema, debe cargarlo en un objeto de perfil. El administrador de perfiles proporciona dos opciones para cargar perfiles del sistema: por identificador y por índice.

Un identificador de perfil del sistema es un valor GUID asignado al perfil del sistema cuando se creó. Para obtener una lista de las constantes GUID asociadas a los perfiles del sistema de la versión 8, vea [Perfiles de sistema](system-profiles.md). Puede encontrar las constantes GUID de versiones anteriores en el archivo de encabezado WMSysPrf.h. Para obtener más información sobre este y otros archivos de encabezado incluidos con Windows SDK de formato multimedia, vea Archivos de biblioteca y compilador [Configuración](library-files-and-compiler-settings.md).

En el código de ejemplo siguiente se muestra cómo cargar un perfil del sistema mediante el identificador de perfil del sistema. Para que este código funcione, debe incluir WMSysPrf.h y stdio.h. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


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



Si no sabe qué perfil desea usar, puede recorrer en iteración todos los perfiles del sistema de una versión determinada mediante los métodos [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) y [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) de la interfaz [**IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) Estos métodos solo tratan con una versión de los perfiles del sistema a la vez. Para obtener más información sobre cómo cambiar la versión del perfil del sistema, vea [Para cambiar las versiones de perfil del sistema](to-change-system-profile-versions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de perfiles del sistema**](using-system-profiles.md)
</dt> </dl>

 

 




