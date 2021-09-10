---
title: Comportamiento predeterminado de los controladores
description: Comportamiento predeterminado de los controladores
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371606"
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

 

 