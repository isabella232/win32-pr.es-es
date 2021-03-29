---
title: Comportamiento predeterminado de los controladores
description: Comportamiento predeterminado de los controladores
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791073"
---
# <a name="default-behavior-of-drivers"></a>Comportamiento predeterminado de los controladores

En muchas situaciones, las especificaciones del comando MCI definen los valores predeterminados y el comportamiento de los controladores de un tipo de dispositivo determinado. Dado que los dispositivos multimedia pueden tener una amplia gama de características (y limitaciones), puede haber áreas de comportamiento sin definir. Además, los controladores pueden controlar las excepciones de manera diferente, en función de las capacidades del dispositivo.

Por ejemplo, considere los siguientes comandos que se envían a un controlador de audio de una onda mediante la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



El comando [**Record**](record.md) devuelve un valor "parámetro fuera del intervalo" y detiene la reproducción iniciada por el comando [**Play**](play.md) anterior. Podría esperar que el controlador validara el comando de registro antes de detener la reproducción, pero el controlador detiene primero la reproducción.

 

 