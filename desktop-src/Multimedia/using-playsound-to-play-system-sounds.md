---
title: Usar PlaySound para reproducir sonidos del sistema
description: Usar PlaySound para reproducir sonidos del sistema
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- audio de onda, función PlaySound
- audio de onda, reproducir sonidos del sistema
- audio de onda, eventos de sonido
- Función PlaySound, reproducir sonidos del sistema
- Función PlaySound, eventos de sonido
- 'reproducir ondas de onda: sonidos del sistema de audio'
- eventos de sonido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904600"
---
# <a name="using-playsound-to-play-system-sounds"></a>Usar PlaySound para reproducir sonidos del sistema

La función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) también reproducirá sonidos a los que se hace referencia mediante un KeyName en el registro. Los usuarios pueden asignar sus propios sonidos a las alertas y advertencias del sistema, o bien a las acciones del usuario, como un clic del botón del mouse. Los sonidos que están asociados a las alertas y advertencias del sistema se denominan *eventos de sonido*.

Para reproducir un evento de sonido, llame a **PlaySound** con el parámetro *pszSound* que apunta a una cadena que contiene el nombre de la entrada del registro que identifica el sonido. Por ejemplo, para reproducir el sonido asociado a la entrada "MouseClick" y esperar a que se complete el sonido antes de volver, use la siguiente instrucción:


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



Si la entrada del registro especificada o el archivo de audio de forma de onda que identifica no existe, o si el archivo no cabe en la memoria disponible, **PlaySound** reproduce el sonido predeterminado del sistema.

Los eventos de sonido que están predefinidos por el sistema pueden variar con la plataforma. La lista siguiente proporciona los eventos de sonido que se definen para todas las implementaciones de la API Win32:

-   SystemAsterisk
-   SystemExclamation
-   SystemExit
-   SystemHand
-   SystemQuestion
-   SystemStart

Si una aplicación registra sus propios eventos de sonido, el usuario puede configurar el evento de sonido mediante la interfaz estándar del panel de control. La aplicación debe registrar el evento de sonido mediante las funciones de registro estándar. para obtener más información, vea [Registry](../sysinfo/registry.md). Las entradas pertenecen a la misma posición en la jerarquía del registro que el resto de los eventos de sonido. Esta posición varía según la implementación de Win32. El valor de datos adecuado también varía con la implementación de.

La función [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) siempre busca en el registro un KeyName que coincida con *lpszSound* antes de intentar cargar un archivo con este nombre. La función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) acepta marcas que especifican la ubicación del sonido.

 

 