---
title: Control de dispositivo (Windows multimedia)
description: Control de dispositivos
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078749"
---
# <a name="device-control-windows-multimedia"></a>Control de dispositivo (Windows multimedia)

Para controlar un dispositivo MCI, abra el dispositivo, envíele los comandos necesarios y, a continuación, cierre el dispositivo. Los comandos pueden ser muy similares, incluso para dispositivos MCI completamente diferentes. Por ejemplo, la siguiente serie de comandos de MCI reproduce la sexta pista de un CD de audio mediante la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



En el ejemplo siguiente se muestra una serie similar de comandos MCI que desempeñan los primeros 10.000 ejemplos de un archivo de audio de forma de onda:


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



En estos ejemplos se muestran algunos aspectos interesantes sobre los comandos de MCI:

-   Los mismos comandos básicos ([**abrir**](open.md), [**establecer**](set.md), [**reproducir**](play.md)y [**cerrar**](close.md)) se usan con dispositivos de audio de CD y de onda. Se usan los mismos comandos MCI con todos los dispositivos MCI.
-   El comando abrir para el dispositivo de audio de onda de onda incluye una especificación de nombre de archivo. El dispositivo de audio de forma de onda es un *dispositivo compuesto* (uno asociado a un archivo de datos), mientras que el dispositivo de audio de CD es un *dispositivo sencillo* (uno sin un archivo de datos asociado).
-   El comando set especifica los formatos de hora en cada caso, pero la marca de formato de hora para el dispositivo de audio de CD especifica el formato de pista/minutos/segundos/fotogramas (TMSF), mientras que el formato de hora usado con el dispositivo de audio de forma de onda especifica "Samples".
-   Las variables que se usan con las marcas "from" y "to" son adecuadas para el formato de hora correspondiente. Por ejemplo, para el dispositivo de audio de CD, las variables especifican un intervalo de pistas, pero para el dispositivo de audio de onda, las variables especifican un intervalo de muestras.

 

 
