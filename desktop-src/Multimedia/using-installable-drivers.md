---
title: Usar controladores instalables
description: Usar controladores instalables
ms.assetid: 23680369-92f9-4558-aa95-f2f44734cece
keywords:
- Windows multimedia, controladores instalables
- multimedia, controladores instalables
- Controladores instalables, acerca de
- DriverProc función)
- Controladores instalables, función DriverProc
- Controladores instalables, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd8573e017eb8bee9b8f1e6054fdd529b724335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358817"
---
# <a name="using-installable-drivers"></a><span data-ttu-id="0e6cf-109">Usar controladores instalables</span><span class="sxs-lookup"><span data-stu-id="0e6cf-109">Using Installable Drivers</span></span>

<span data-ttu-id="0e6cf-110">Puede usar controladores instalables para proporcionar a las aplicaciones o archivos dll una manera estándar de acceder a un dispositivo o un conjunto de rutinas útiles.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-110">You use installable drivers to give applications or DLLs a standard way to access a device or a set of useful routines.</span></span> <span data-ttu-id="0e6cf-111">En las secciones siguientes se muestra cómo crear un controlador instalable mediante una función [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) y cómo abrir un controlador instalable y dirigirlo para llevar a cabo tareas útiles.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-111">The following sections show how to create an installable driver by using a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function and how to open an installable driver and direct it to carry out useful tasks.</span></span>

 

 