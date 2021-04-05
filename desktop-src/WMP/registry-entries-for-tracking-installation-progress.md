---
title: Entradas del registro para realizar un seguimiento del progreso de la instalación
description: Entradas del registro para realizar un seguimiento del progreso de la instalación
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, seguimiento del progreso de la instalación
- Windows Media Player, seguimiento del progreso de la instalación
- Windows Media Player, seguimiento del progreso de las instalaciones
- Media Player de Windows, registro
- registro, seguimiento del progreso de la instalación
- registro, seguimiento del progreso de la instalación
- registro, seguimiento del progreso de las instalaciones
- registro, configuración para Windows Media Player
- seguimiento del progreso de la instalación
- instalación del seguimiento del progreso
- seguimiento del progreso de las instalaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076354"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Entradas del registro para realizar un seguimiento del progreso de la instalación

El programa de instalación de Windows Media Player 11, setup \_wm.exe, escribe las siguientes entradas en el registro para que los programas de instalación puedan realizar el seguimiento del progreso del programa de instalación de Media Player de Windows mientras se ejecuta.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



En la sintaxis del registro anterior, *valor* es un marcador de posición para un valor entero.

Progress \_ CurrentDialog indica qué cuadro de diálogo Media Player instalación de Windows se está mostrando actualmente. Progress \_ MaxDialog indica el número total de cuadros de diálogo que Windows Media mostrará. Por ejemplo, si Progress \_ CurrentDialog = 2 y Progress \_ MaxDialog = 5, Windows Media Player actualmente muestra el segundo cuadro de diálogo en una secuencia de cinco.

Progress \_ CurrentInstall and Progress \_ MaxInstall, tomado juntos, indican el porcentaje de finalización del diálogo actual. Por ejemplo, si Progress \_ CurrentInstall = 6 and Progress \_ MaxInstall = 25, el cuadro de diálogo actual es 6/25 (es decir, 24%) finaliza.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro**](registry-settings.md)
</dt> </dl>

 

 




