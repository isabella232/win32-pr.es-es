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
# <a name="tablet-pc-platform-info-sample"></a>Ejemplo de información de plataforma de Tablet PC

Este programa comprueba la presencia y configuración de los componentes de MicrosoftTablet PC y Touch Technology Core. Determina si los componentes de Tablet PC están habilitados en el sistema operativo, enumera los nombres y la información de versión de los controles principales y el reconocedor de escritura a mano y voz predeterminados.

La aplicación usa la API de Windows GetSystemMetrics, pasando SM \_ TABLETPC, para determinar si la aplicación se ejecuta en un Tablet PC. SM \_ TABLETPC se define en WinUser. h.

De especial interés es el modo en que la aplicación utiliza la colección de reconocedores para proporcionar información sobre el reconocedor predeterminado. Antes de intentar utilizar la colección de reconocedores y el objeto de reconocedor, la aplicación comprueba si se ha creado correctamente.

## <a name="components"></a>Componentes

Con el módulo de fusión mediante combinación redistribuible, algunas partes de la API de la plataforma de Tablet PC se pueden instalar en versiones que no son de tabletas de vista y Windows XP Professional. La llamada a GetSystemMetrics solo indica que está instalado Windows XP Tablet PC Edition. Una aplicación siempre debe determinar si un componente determinado está disponible. La manera adecuada de determinar si un componente de la API está instalada es intentar crear una instancia de un objeto o un control y comprobar que existe antes de intentar usarlo, como se muestra en el ejemplo siguiente.


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



La aplicación detecta los componentes de voz instalados mediante la búsqueda en la clave del registro adecuada:


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



La clave se lee mediante RegQueryValueExW.

Finalmente, el ejemplo averigua qué controles están instalados.


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



 

 



