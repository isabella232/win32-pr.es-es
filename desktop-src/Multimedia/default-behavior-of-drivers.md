---
title: Comportamiento predeterminado de los controladores
description: Comportamiento predeterminado de los controladores
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61312010759ddd1bf152f0e51f7605bda1954329096913b61dac14a671908f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144528"
---
# <a name="default-behavior-of-drivers"></a>Comportamiento predeterminado de los controladores

En muchas situaciones, las especificaciones del comando MCI definen los valores predeterminados y el comportamiento de los controladores de un tipo de dispositivo determinado. Dado que los dispositivos multimedia pueden tener una amplia gama de características (y limitaciones), puede haber áreas de comportamiento no definidas. Además, los controladores pueden controlar las excepciones de forma diferente, en función de las funcionalidades del dispositivo.

Por ejemplo, considere los siguientes comandos enviados a un controlador de audio de forma de onda mediante la [**función mciSendString:**](/previous-versions//dd757161(v=vs.85))


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



El [**comando record**](record.md) devuelve un valor "Parameter out of range" (Parámetro fuera del intervalo) y detiene la reproducción iniciada por el comando de [**reproducción**](play.md) anterior. Es posible que se espere que el controlador valide el comando de registro antes de detener la reproducción, pero el controlador detiene primero la reproducción.

 

 