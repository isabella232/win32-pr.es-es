---
description: Este programa comprueba la presencia y configuración de los componentes principales de MicrosoftTablet PC y Touch Technology.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Ejemplo de información de la plataforma de Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1731fc30e0405b2702bb45d0a9d0556b861ad09994ac683d739da33afe018088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819995"
---
# <a name="tablet-pc-platform-info-sample"></a>Ejemplo de información de la plataforma de Tablet PC

Este programa comprueba la presencia y configuración de los componentes principales de MicrosoftTablet PC y Touch Technology. Determina si los componentes de Tablet PC están habilitados en el sistema operativo, enumerando los nombres y la información de versión de los controles principales y el reconocedor de voz y escritura a mano predeterminado.

La aplicación usa la API getSystemMetrics Windows, pasando SM TABLETPC, para determinar si la aplicación se ejecuta \_ en un tablet PC. SM \_ TABLETPC se define en WinUser.h.

De especial interés es la forma en que la aplicación usa la colección Recognizers para proporcionar información sobre el reconocedor predeterminado. Antes de intentar usar la colección Recognizers y el objeto Recognizer, la aplicación comprueba su creación correcta.

## <a name="components"></a>Componentes

Con el módulo de combinación distribuible, es posible que determinadas partes de la API de la plataforma de Pc de tableta se instalen en versiones que no son de tableta de Vista y Windows XP Professional . La llamada a GetSystemMetrics solo indica que Windows xp Tablet PC Edition está instalado. Una aplicación siempre debe determinar si un componente determinado está disponible. La manera adecuada de determinar si un componente de la API está instalado es intentar crear una instancia de un objeto o control y comprobar que existe antes de intentar usarlo, como se muestra en el ejemplo siguiente.


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



La aplicación busca en la clave del Registro adecuada para averiguar los componentes de voz instalados:


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



La clave se lee mediante RegQueryValueExW.

Por último, el ejemplo determina qué controles están instalados.


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



 

 



