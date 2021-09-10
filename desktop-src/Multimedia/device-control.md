---
title: Control de dispositivos (Windows Multimedia)
description: Control de dispositivos
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371611"
---
# <a name="device-control-windows-multimedia"></a>Control de dispositivos (Windows Multimedia)

Para controlar un dispositivo MCI, abra el dispositivo, envíele los comandos necesarios y, a continuación, cierre el dispositivo. Los comandos pueden ser muy similares, incluso para dispositivos MCI completamente diferentes. Por ejemplo, la siguiente serie de comandos MCI reproduce la sexta pista de un CD de audio mediante la [**función mciSendString:**](/previous-versions//dd757161(v=vs.85))


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



En el ejemplo siguiente se muestra una serie similar de comandos MCI que reproducen las primeras 10 000 muestras de un archivo de audio de forma de onda:


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



En estos ejemplos se muestran algunos hechos interesantes sobre los comandos de MCI:

-   Los mismos comandos básicos [**(abrir,**](open.md) [**establecer,**](set.md) [**reproducir**](play.md) [**y**](close.md)cerrar) se usan con los dispositivos de audio de CD y audio de forma de onda. Los mismos comandos MCI se usan con todos los dispositivos MCI.
-   El comando open para el dispositivo de audio de forma de onda incluye una especificación de nombre de archivo. El dispositivo de audio de forma de onda es un dispositivo compuesto *(uno* asociado a un archivo de datos), mientras que el dispositivo de audio de CD es un dispositivo *simple* (uno sin un archivo de datos asociado).
-   El comando set especifica los formatos de hora en cada caso, pero la marca de formato de tiempo para el dispositivo de audio de CD especifica el formato tracks/minutes/seconds/frames (TMSF), mientras que el formato de hora usado con el dispositivo de audio de forma de onda especifica "ejemplos".
-   Las variables usadas con las marcas "from" y "to" son adecuadas para el formato de hora correspondiente. Por ejemplo, para el dispositivo de audio de CD, las variables especifican un intervalo de pistas, pero para el dispositivo de audio de forma de onda, las variables especifican un intervalo de muestras.

 

 
