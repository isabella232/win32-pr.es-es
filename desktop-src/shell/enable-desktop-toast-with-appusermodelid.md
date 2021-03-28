---
description: En este tema se muestra cómo crear un acceso directo para la aplicación, asignarla a un AppUserModelID e instalarla en la pantalla Inicio.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985087"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a><span data-ttu-id="50ea2-103">Cómo habilitar las notificaciones del sistema del escritorio a través de AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="50ea2-103">How to enable desktop toast notifications through an AppUserModelID</span></span>

<span data-ttu-id="50ea2-104">En este tema se muestra cómo crear un acceso directo para la aplicación, asignarla a un [AppUserModelID](appids.md)e instalarla en la pantalla Inicio.</span><span class="sxs-lookup"><span data-stu-id="50ea2-104">This topic shows you how to create a shortcut for your app, assign it an [AppUserModelID](appids.md), and install it in the Start screen.</span></span> <span data-ttu-id="50ea2-105">Le recomendamos encarecidamente que lo haga en el Windows Installer en lugar de en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50ea2-105">We strongly recommend that you do this in the Windows Installer rather than in your app's code.</span></span> <span data-ttu-id="50ea2-106">Sin un acceso directo válido instalado en la pantalla Inicio o en **todos los programas**, no se puede generar una notificación del sistema desde una aplicación de escritorio.</span><span class="sxs-lookup"><span data-stu-id="50ea2-106">Without a valid shortcut installed in the Start screen or in **All Programs**, you cannot raise a toast notification from a desktop app.</span></span>

> [!Note]  
> <span data-ttu-id="50ea2-107">Los métodos de ejemplo que se usan en este tema se toman del [ejemplo del sistema de notificación del escritorio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span><span class="sxs-lookup"><span data-stu-id="50ea2-107">The example methods used in this topic are taken from the [Desktop toast sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="50ea2-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="50ea2-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="50ea2-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="50ea2-109">Technologies</span></span>

-   <span data-ttu-id="50ea2-110">COM</span><span class="sxs-lookup"><span data-stu-id="50ea2-110">COM</span></span>

### <a name="prerequisites"></a><span data-ttu-id="50ea2-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="50ea2-111">Prerequisites</span></span>

-   <span data-ttu-id="50ea2-112">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="50ea2-112">Libraries</span></span>
    -   <span data-ttu-id="50ea2-113">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="50ea2-113">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="50ea2-114">C \# : Windows. Winmd</span><span class="sxs-lookup"><span data-stu-id="50ea2-114">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="50ea2-115">C \# : paquete de código de la API de Windows para Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="50ea2-115">C\#: Windows API Code Pack for Microsoft .NET Framework</span></span>
-   <span data-ttu-id="50ea2-116">Una versión de Microsoft Visual Studio que admita al menos Windows 8</span><span class="sxs-lookup"><span data-stu-id="50ea2-116">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="50ea2-117">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="50ea2-117">Instructions</span></span>

### <a name="step-1-prepare-the-shortcut-to-be-created"></a><span data-ttu-id="50ea2-118">Paso 1: preparar el acceso directo que se va a crear</span><span class="sxs-lookup"><span data-stu-id="50ea2-118">Step 1: Prepare the shortcut to be created</span></span>

<span data-ttu-id="50ea2-119">En primer lugar, este ejemplo determina la ruta de acceso de la carpeta de datos de la aplicación del usuario a través de la función [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) .</span><span class="sxs-lookup"><span data-stu-id="50ea2-119">This example first determines the path of the user's app data folder through the [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) function.</span></span> <span data-ttu-id="50ea2-120">A continuación, crea la ruta de acceso completa al acceso directo, determina que ya no existe un acceso directo a ese nombre en esa ubicación y pasa esa información a otro método que crea e instala el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="50ea2-120">It then composes the full path to the shortcut, determines that a shortcut of that name does not already exist at that location, and passes that information to another method which creates and installs the shortcut.</span></span>

<span data-ttu-id="50ea2-121">Tenga en cuenta que el acceso directo se puede implementar por usuario o por aplicación.</span><span class="sxs-lookup"><span data-stu-id="50ea2-121">Note that the shortcut can be deployed per-user or per-app.</span></span>


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



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a><span data-ttu-id="50ea2-122">Paso 2: crear el acceso directo e instalarlo en la pantalla Inicio</span><span class="sxs-lookup"><span data-stu-id="50ea2-122">Step 2: Create the shortcut and install it in the Start screen</span></span>

<span data-ttu-id="50ea2-123">En este ejemplo también se recupera el almacén de propiedades del método abreviado y se establece la propiedad [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) requerida a partir de una variable definida anteriormente, `AppID` .</span><span class="sxs-lookup"><span data-stu-id="50ea2-123">This example also retrieves the shortcut's property store and sets the required [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property from a previously defined variable, `AppID`.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="50ea2-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50ea2-124">Remarks</span></span>

<span data-ttu-id="50ea2-125">Como alternativa al enfoque que se muestra en este tema, puede usar un marco de trabajo como Windows Installer XML (WiX) para generar el acceso directo e implementarlo como parte de la Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="50ea2-125">As an alternative to the approach shown in this topic, you can use a framework such as the Windows Installer XML (WiX) to generate the shortcut and deploy it as part of the Windows Installer.</span></span> <span data-ttu-id="50ea2-126">En ese caso, este código debe incluirse en el MSI en lugar de en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50ea2-126">In that case, this code should be included in the MSI rather than in the app's code.</span></span> <span data-ttu-id="50ea2-127">Para obtener más información, vea el archivo de configuración de WiX de ejemplo incluido en el ejemplo de [envío de notificaciones del sistema de aplicaciones de escritorio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) .</span><span class="sxs-lookup"><span data-stu-id="50ea2-127">For more information, see the sample WiX configuration file included with the [Sending toast notifications from desktop apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50ea2-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50ea2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50ea2-129">Inicio rápido: envío de una notificación del sistema desde el escritorio</span><span class="sxs-lookup"><span data-stu-id="50ea2-129">Quickstart: Sending a toast notification from the desktop</span></span>](quickstart-sending-desktop-toast.md)
</dt> <dt>

<span data-ttu-id="50ea2-130">[Ejemplo sobre cómo enviar notificaciones del sistema de aplicaciones de escritorio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="50ea2-130">[Sending toast notifications from desktop apps sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span></span>
</dt> <dt>

[<span data-ttu-id="50ea2-131">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="50ea2-131">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> <dt>

<span data-ttu-id="50ea2-132">[Cómo: instalar las herramientas de Windows Installer XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-132">[How to: Install the Windows Installer XML (WiX) Tools](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="50ea2-133">Esquema XML del sistema de notificación</span><span class="sxs-lookup"><span data-stu-id="50ea2-133">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="50ea2-134">[Introducción a las notificaciones del sistema](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-134">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="50ea2-135">[Inicio rápido: envío de una notificación del sistema](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-135">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="50ea2-136">[Inicio rápido: envío de una notificación de notificaciones de envío](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-136">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="50ea2-137">Directrices y lista de comprobación para las notificaciones del sistema</span><span class="sxs-lookup"><span data-stu-id="50ea2-137">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[<span data-ttu-id="50ea2-138">Cómo agregar imágenes a una plantilla de notificación del sistema</span><span class="sxs-lookup"><span data-stu-id="50ea2-138">How to add images to a toast template</span></span>](/previous-versions/windows/)
</dt> <dt>

[<span data-ttu-id="50ea2-139">Comprobación de la configuración de notificaciones del sistema</span><span class="sxs-lookup"><span data-stu-id="50ea2-139">How to check toast notification settings</span></span>](/previous-versions/windows/)
</dt> <dt>

<span data-ttu-id="50ea2-140">[Cómo elegir y usar una plantilla de notificación del sistema](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-140">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="50ea2-141">[Cómo controlar la activación desde una notificación del sistema](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-141">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="50ea2-142">[Cómo participar en las notificaciones del sistema](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-142">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="50ea2-143">[Elección de una plantilla de notificación del sistema](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-143">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="50ea2-144">[Opciones de audio del sistema](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="50ea2-144">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
