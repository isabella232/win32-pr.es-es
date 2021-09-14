---
description: En este tema se muestra cómo crear un acceso directo para la aplicación, asignarle un AppUserModelID e instalarlo en el pantalla Inicio.
title: Cómo habilitar las notificaciones del sistema del escritorio a través de AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: bd02a0ec6512aa7637f0d6b2b281e1b862e61d3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267924"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a>Cómo habilitar las notificaciones del sistema del escritorio a través de AppUserModelID

En este tema se muestra cómo crear un acceso directo para la aplicación, asignarle un [AppUserModelID](appids.md)e instalarlo en el pantalla Inicio. Se recomienda encarecidamente que lo haga en el instalador Windows en lugar de en el código de la aplicación. Sin un acceso directo válido instalado en el pantalla Inicio o en **Todos** los programas , no se puede generar una notificación del sistema desde una aplicación de escritorio.

> [!Note]  
> Los métodos de ejemplo usados en este tema se toman del ejemplo [del sistema de escritorio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).

 

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   COM

### <a name="prerequisites"></a>Prerrequisitos

-   Bibliotecas
    -   C++: Runtime.object.lib
    -   C \# : Windows. Winmd
-   C: \# Windows de código de API para Microsoft .NET Framework
-   Una versión de Microsoft Visual Studio admite al menos Windows 8

## <a name="instructions"></a>Instructions

### <a name="step-1-prepare-the-shortcut-to-be-created"></a>Paso 1: Preparar el acceso directo que se va a crear

En primer lugar, este ejemplo determina la ruta de acceso de la carpeta de datos de la aplicación del usuario a través de [**la función GetEnvironmentVariable.**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) A continuación, crea la ruta de acceso completa al acceso directo, determina que aún no existe un acceso directo con ese nombre en esa ubicación y pasa esa información a otro método que crea e instala el acceso directo.

Tenga en cuenta que el acceso directo se puede implementar por usuario o por aplicación.


```C++
HRESULT DesktopToastsApp::TryCreateShortcut()
{
    wchar_t shortcutPath[MAX_PATH];
    DWORD charWritten = GetEnvironmentVariable(L"APPDATA", shortcutPath, MAX_PATH);
    HRESULT hr = charWritten > 0 ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        errno_t concatError = wcscat_s(shortcutPath, ARRAYSIZE(shortcutPath), L"\\Microsoft\\Windows\\Start Menu\\Programs\\Desktop Toasts App.lnk");
 
        hr = concatError == 0 ? S_OK : E_INVALIDARG;
        if (SUCCEEDED(hr))
        {
            DWORD attributes = GetFileAttributes(shortcutPath);
            bool fileExists = attributes < 0xFFFFFFF;

            if (!fileExists)
            {
                hr = InstallShortcut(shortcutPath);  // See step 2.
            }
            else
            {
                hr = S_FALSE;
            }
        }
    }
    return hr;
}
```



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a>Paso 2: Crear el acceso directo e instalarlo en el pantalla Inicio

En este ejemplo también se recupera el almacén de propiedades del acceso directo y se establece la propiedad System.AppUserModel.ID [necesaria](../properties/props-system-appusermodel-id.md) de una variable definida previamente, `AppID` .


```C++
HRESULT DesktopToastsApp::InstallShortcut(_In_z_ wchar_t *shortcutPath)
{
    wchar_t exePath[MAX_PATH];
    
    DWORD charWritten = GetModuleFileNameEx(GetCurrentProcess(), nullptr, exePath, ARRAYSIZE(exePath));

    HRESULT hr = charWritten > 0 ? S_OK : E_FAIL;
    
    if (SUCCEEDED(hr))
    {
        ComPtr<IShellLink> shellLink;
        hr = CoCreateInstance(CLSID_ShellLink, nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink));

        if (SUCCEEDED(hr))
        {
            hr = shellLink->SetPath(exePath);
            if (SUCCEEDED(hr))
            {
                hr = shellLink->SetArguments(L"");
                if (SUCCEEDED(hr))
                {
                    ComPtr<IPropertyStore> propertyStore;

                    hr = shellLink.As(&propertyStore);
                    if (SUCCEEDED(hr))
                    {
                        PROPVARIANT appIdPropVar;
                        hr = InitPropVariantFromString(AppId, &appIdPropVar);
                        if (SUCCEEDED(hr))
                        {
                            hr = propertyStore->SetValue(PKEY_AppUserModel_ID, appIdPropVar);
                            if (SUCCEEDED(hr))
                            {
                                hr = propertyStore->Commit();
                                if (SUCCEEDED(hr))
                                {
                                    ComPtr<IPersistFile> persistFile;
                                    hr = shellLink.As(&persistFile);
                                    if (SUCCEEDED(hr))
                                    {
                                        hr = persistFile->Save(shortcutPath, TRUE);
                                    }
                                }
                            }
                            PropVariantClear(&appIdPropVar);
                        }
                    }
                }
            }
        }
    }
    return hr;
}
```



## <a name="remarks"></a>Observaciones

Como alternativa al enfoque que se muestra en este tema, puede usar un marco como Windows Installer XML (WiX) para generar el acceso directo e implementarlo como parte del instalador de Windows. En ese caso, este código debe incluirse en msi en lugar de en el código de la aplicación. Para más información, consulte el archivo de configuración de WiX de ejemplo incluido en el ejemplo Envío de [notificaciones del sistema desde aplicaciones de](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) escritorio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicio rápido: Envío de una notificación del sistema desde el escritorio](quickstart-sending-desktop-toast.md)
</dt> <dt>

[Ejemplo sobre cómo enviar notificaciones del sistema de aplicaciones de escritorio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))
</dt> <dt>

[Id. de modelo de usuario de aplicación (AppUserModelID)](appids.md)
</dt> <dt>

[Cómo: Instalar las herramientas Windows Installer XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))
</dt> <dt>

[Esquema XML del sistema](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Introducción a las notificaciones del sistema](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Inicio rápido: Envío de una notificación del sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Inicio rápido: Envío de una notificación push del sistema](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Directrices y lista de comprobación para notificaciones del sistema](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Cómo agregar imágenes a una plantilla del sistema](/previous-versions/windows/)
</dt> <dt>

[Comprobación de la configuración de notificaciones del sistema](/previous-versions/windows/)
</dt> <dt>

[Cómo elegir y usar una plantilla del sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Cómo controlar la activación desde una notificación del sistema](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Cómo participar en las notificaciones del sistema](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Elección de una plantilla del sistema](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opciones de audio del sistema](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
