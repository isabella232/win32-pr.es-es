---
description: Este programa comprueba la presencia y configuración de los componentes de MicrosoftTablet PC y Touch Technology Core.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Ejemplo de información de plataforma de Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d815f21233b1edcc90d456df68b3736c170a5fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697659"
---
# <a name="tablet-pc-platform-info-sample"></a><span data-ttu-id="1a70c-103">Ejemplo de información de plataforma de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="1a70c-103">Tablet PC Platform Info Sample</span></span>

<span data-ttu-id="1a70c-104">Este programa comprueba la presencia y configuración de los componentes de MicrosoftTablet PC y Touch Technology Core.</span><span class="sxs-lookup"><span data-stu-id="1a70c-104">This program checks the presence and configuration of the MicrosoftTablet PC and Touch Technology core components.</span></span> <span data-ttu-id="1a70c-105">Determina si los componentes de Tablet PC están habilitados en el sistema operativo, enumera los nombres y la información de versión de los controles principales y el reconocedor de escritura a mano y voz predeterminados.</span><span class="sxs-lookup"><span data-stu-id="1a70c-105">It determines whether Tablet PC components are enabled in the operating system, listing names and version information for core controls and the default handwriting and speech recognizer.</span></span>

<span data-ttu-id="1a70c-106">La aplicación usa la API de Windows GetSystemMetrics, pasando SM \_ TABLETPC, para determinar si la aplicación se ejecuta en un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="1a70c-106">The application uses the GetSystemMetrics Windows API, passing in SM\_TABLETPC, to determine whether the application running on a Tablet PC.</span></span> <span data-ttu-id="1a70c-107">SM \_ TABLETPC se define en WinUser. h.</span><span class="sxs-lookup"><span data-stu-id="1a70c-107">SM\_TABLETPC is defined in WinUser.h.</span></span>

<span data-ttu-id="1a70c-108">De especial interés es el modo en que la aplicación utiliza la colección de reconocedores para proporcionar información sobre el reconocedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1a70c-108">Of particular interest is the way the application uses the Recognizers collection to provide information about the default recognizer.</span></span> <span data-ttu-id="1a70c-109">Antes de intentar utilizar la colección de reconocedores y el objeto de reconocedor, la aplicación comprueba si se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a70c-109">Before attempting to use the Recognizers collection and Recognizer object, the application tests for their successful creation.</span></span>

## <a name="components"></a><span data-ttu-id="1a70c-110">Componentes</span><span class="sxs-lookup"><span data-stu-id="1a70c-110">Components</span></span>

<span data-ttu-id="1a70c-111">Con el módulo de fusión mediante combinación redistribuible, algunas partes de la API de la plataforma de Tablet PC se pueden instalar en versiones que no son de tabletas de vista y Windows XP Professional.</span><span class="sxs-lookup"><span data-stu-id="1a70c-111">Using the re-distributable merge module, certain parts of the Tablet PC Platform API may be installed on non-Tablet versions of Vista and Windows XP Professional .</span></span> <span data-ttu-id="1a70c-112">La llamada a GetSystemMetrics solo indica que está instalado Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="1a70c-112">The GetSystemMetrics call only indicates that Windows XP Tablet PC Edition is installed.</span></span> <span data-ttu-id="1a70c-113">Una aplicación siempre debe determinar si un componente determinado está disponible.</span><span class="sxs-lookup"><span data-stu-id="1a70c-113">An application should always determine if a given component is available.</span></span> <span data-ttu-id="1a70c-114">La manera adecuada de determinar si un componente de la API está instalada es intentar crear una instancia de un objeto o un control y comprobar que existe antes de intentar usarlo, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="1a70c-114">The proper way to determine if a component of the API is installed is to attempt to create an instance of an object or control and check that it exists before attempting to use it, as shown in the following example.</span></span>


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



<span data-ttu-id="1a70c-115">La aplicación detecta los componentes de voz instalados mediante la búsqueda en la clave del registro adecuada:</span><span class="sxs-lookup"><span data-stu-id="1a70c-115">The application finds out about the installed speech components by looking in the appropriate registry key:</span></span>


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



<span data-ttu-id="1a70c-116">La clave se lee mediante RegQueryValueExW.</span><span class="sxs-lookup"><span data-stu-id="1a70c-116">The key is read using RegQueryValueExW.</span></span>

<span data-ttu-id="1a70c-117">Finalmente, el ejemplo averigua qué controles están instalados.</span><span class="sxs-lookup"><span data-stu-id="1a70c-117">Finally, the sample finds out which controls are installed.</span></span>


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



