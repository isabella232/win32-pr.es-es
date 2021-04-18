---
description: Debido a la falta de reconocedores en las ediciones que no son de Tablet PC de Microsoft Windows XP, no puede usar InkEdit para representar la entrada manuscrita en Windows 2000, Windows Server 2003 y las ediciones que no son de Tablet PC de Windows XP, y no puede usar el control para introducir entradas manuscritas en estos sistemas operativos.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Usar InkEdit en versiones anteriores de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715078"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a><span data-ttu-id="a71a5-103">Usar InkEdit en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="a71a5-103">Using InkEdit on Earlier Versions of Windows</span></span>

<span data-ttu-id="a71a5-104">Debido a la falta de reconocedores en las ediciones que no son de Tablet PC de Microsoft Windows XP, no puede usar [InkEdit](inkedit-control.md) para representar la entrada manuscrita en Windows 2000, windows Server 2003 y las ediciones que no son de Tablet PC de Windows XP, y no puede usar el control para introducir entradas manuscritas en estos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="a71a5-104">Because of the lack of recognizers on non-Tablet PC editions of Microsoft Windows XP, you cannot use [InkEdit](inkedit-control.md) to render ink on Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP, and you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="a71a5-105">La propiedad [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del control se establece en **Disabled** (**IEM \_ deshabilitada** para C++) y el intento de cambiar la propiedad no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="a71a5-105">The control's [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property is set to **Disabled** (**IEM\_Disabled** for C++), and attempting to change the property has no effect.</span></span> <span data-ttu-id="a71a5-106">Puede asignar valores a otras propiedades y copiar y pegar entradas manuscritas en otras aplicaciones, pero no puede usar el control para aceptar gestos o recopilar entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="a71a5-106">You can assign values to other properties and copy and paste ink to other applications, but you cannot use the control to accept gestures or collect ink.</span></span>

 

 



