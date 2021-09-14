---
title: Uso de Play Sound para reproducir sonidos del sistema
description: Uso de Play Sound para reproducir sonidos del sistema
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- audio de forma de onda, función Play Sound
- audio de onda, reproducir sonidos del sistema
- audio de sonido, eventos de sonido
- Función Play Sound, reproducir sonidos del sistema
- Función Play Sound, eventos de sonido
- reproducir sonidos del sistema de audio de forma de onda
- eventos de sonido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071744"
---
# <a name="using-playsound-to-play-system-sounds"></a>Uso de Play Sound para reproducir sonidos del sistema

La [**función Play Sound**](/previous-versions//dd743680(v=vs.85)) también reproducirá los sonidos a los que hace referencia un nombre de clave en el registro. Los usuarios pueden asignar sus propios sonidos a alertas y advertencias del sistema, o a acciones del usuario, como un clic del botón del mouse. Los sonidos asociados a las alertas y advertencias del sistema se denominan *eventos de sonido.*

Para reproducir un evento de sonido, llame a **Play Sound** con el parámetro *psz Sound* que apunta a una cadena que contiene el nombre de la entrada del Registro que identifica el sonido. Por ejemplo, para reproducir el sonido asociado a la entrada "MouseClick" y esperar a que el sonido se complete antes de volver, use la siguiente instrucción:


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



Si la entrada del Registro especificada o el archivo de audio de forma de onda que identifica no existe, o si el archivo no cabe en la memoria disponible, **Play Sound** reproduce el sonido del sistema predeterminado.

Los eventos de sonido predefinidos por el sistema pueden variar con la plataforma. La lista siguiente proporciona los eventos de sonido que se definen para todas las implementaciones de la API win32:

-   SystemAsterisk
-   SystemExclamation
-   SystemExit
-   SystemHand
-   SystemQuestion
-   SystemStart

Si una aplicación registra sus propios eventos de sonido, el usuario puede configurar el evento de sonido mediante la interfaz Panel de control estándar. La aplicación debe registrar el evento de sonido mediante las funciones del Registro estándar. Para obtener más información, vea [Registro](../sysinfo/registry.md). Las entradas pertenecen a la misma posición en la jerarquía del Registro que el resto de los eventos de sonido. Esta posición varía con la implementación de Win32. El valor de datos adecuado también varía con la implementación.

La [**función sndPlay Sound**](/previous-versions//dd798676(v=vs.85)) siempre busca en el Registro un nombre de clave que coincida con *lpsz Sound* antes de intentar cargar un archivo con este nombre. La [**función Play Sound**](/previous-versions//dd743680(v=vs.85)) acepta marcas que especifican la ubicación del sonido.

 

 