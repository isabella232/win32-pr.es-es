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
# <a name="registry-entries-for-tracking-installation-progress"></a><span data-ttu-id="b6fb8-114">Entradas del registro para realizar un seguimiento del progreso de la instalación</span><span class="sxs-lookup"><span data-stu-id="b6fb8-114">Registry Entries for Tracking Installation Progress</span></span>

<span data-ttu-id="b6fb8-115">El programa de instalación de Windows Media Player 11, setup \_wm.exe, escribe las siguientes entradas en el registro para que los programas de instalación puedan realizar el seguimiento del progreso del programa de instalación de Media Player de Windows mientras se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="b6fb8-115">The Windows Media Player 11 setup program, setup\_wm.exe, writes the following entries in the registry so that installation programs can track the progress of the Windows Media Player setup program as it runs.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



<span data-ttu-id="b6fb8-116">En la sintaxis del registro anterior, *valor* es un marcador de posición para un valor entero.</span><span class="sxs-lookup"><span data-stu-id="b6fb8-116">In the preceding registry syntax, *value* is a placeholder for an integer value.</span></span>

<span data-ttu-id="b6fb8-117">Progress \_ CurrentDialog indica qué cuadro de diálogo Media Player instalación de Windows se está mostrando actualmente.</span><span class="sxs-lookup"><span data-stu-id="b6fb8-117">Progress\_CurrentDialog indicates which dialog box Windows Media Player setup is currently displaying.</span></span> <span data-ttu-id="b6fb8-118">Progress \_ MaxDialog indica el número total de cuadros de diálogo que Windows Media mostrará.</span><span class="sxs-lookup"><span data-stu-id="b6fb8-118">Progress\_MaxDialog indicates the total number of dialog boxes that Windows Media will display.</span></span> <span data-ttu-id="b6fb8-119">Por ejemplo, si Progress \_ CurrentDialog = 2 y Progress \_ MaxDialog = 5, Windows Media Player actualmente muestra el segundo cuadro de diálogo en una secuencia de cinco.</span><span class="sxs-lookup"><span data-stu-id="b6fb8-119">For example, if Progress\_CurrentDialog = 2 and Progress\_MaxDialog = 5, Windows Media Player is currently displaying the second dialog box in a sequence of five.</span></span>

<span data-ttu-id="b6fb8-120">Progress \_ CurrentInstall and Progress \_ MaxInstall, tomado juntos, indican el porcentaje de finalización del diálogo actual.</span><span class="sxs-lookup"><span data-stu-id="b6fb8-120">Progress\_CurrentInstall and Progress\_MaxInstall, taken together, indicate the percent of completion of the current dialog.</span></span> <span data-ttu-id="b6fb8-121">Por ejemplo, si Progress \_ CurrentInstall = 6 and Progress \_ MaxInstall = 25, el cuadro de diálogo actual es 6/25 (es decir, 24%) finaliza.</span><span class="sxs-lookup"><span data-stu-id="b6fb8-121">For example, if Progress\_CurrentInstall = 6 and Progress\_MaxInstall = 25, the current dialog is 6/25 (that is, 24%) complete.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6fb8-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6fb8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6fb8-123">**Configuración del registro**</span><span class="sxs-lookup"><span data-stu-id="b6fb8-123">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




