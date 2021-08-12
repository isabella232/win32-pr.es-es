---
title: Entradas del Registro para el seguimiento del progreso de la instalación
description: Entradas del Registro para el seguimiento del progreso de la instalación
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Reproductor de Windows Media, seguimiento del progreso de la instalación
- Reproductor de Windows Media,seguimiento del progreso de la instalación
- Reproductor de Windows Media, seguimiento del progreso de las instalaciones
- Reproductor de Windows Media,registry
- registro, seguimiento del progreso de la instalación
- registro, seguimiento del progreso de la instalación
- registro, seguimiento del progreso de las instalaciones
- registry,settings for Reproductor de Windows Media
- seguimiento del progreso de la instalación
- instalación del seguimiento del progreso
- seguimiento del progreso de las instalaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7febb9f25a04c5e4358e891f963ab6a8569cfd6facef7e4f2072807bd09e2605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570306"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Entradas del Registro para el seguimiento del progreso de la instalación

El programa de instalación Reproductor de Windows Media 11, setupwm.exe, escribe las siguientes entradas en el Registro para que los programas de instalación puedan realizar un seguimiento del progreso del programa de instalación de Reproductor de Windows Media mientras se \_ ejecuta.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



En la sintaxis del Registro anterior, *value es* un marcador de posición para un valor entero.

Progress \_ CurrentDialog indica qué cuadro de diálogo Reproductor de Windows Media se muestra actualmente. Progress MaxDialog indica el número total de cuadros de \_ diálogo que Windows se mostrarán. Por ejemplo, si Progress \_ CurrentDialog = 2 y Progress MaxDialog = 5, Reproductor de Windows Media muestra actualmente el segundo cuadro de diálogo \_ en una secuencia de cinco.

Progress \_ CurrentInstall y Progress \_ MaxInstall, juntos, indican el porcentaje de finalización del cuadro de diálogo actual. Por ejemplo, si Progress CurrentInstall = 6 y Progress MaxInstall = 25, el cuadro de diálogo actual es \_ \_ 6/25 (es decir, 24 %) completado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del Registro**](registry-settings.md)
</dt> </dl>

 

 




