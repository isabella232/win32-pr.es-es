---
title: Parámetro de preferencias de teclado
description: El parámetro de preferencias de teclado indica que el usuario se basa en el teclado en lugar del mouse, por lo que las aplicaciones deben mostrar las interfaces de teclado que, de otro modo, podrían ocultarse.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420960"
---
# <a name="keyboard-preference-parameter"></a><span data-ttu-id="6e94b-103">Parámetro de preferencias de teclado</span><span class="sxs-lookup"><span data-stu-id="6e94b-103">Keyboard preference parameter</span></span>

<span data-ttu-id="6e94b-104">El parámetro de preferencias de teclado indica que el usuario se basa en el teclado en lugar del mouse, por lo que las aplicaciones deben mostrar las interfaces de teclado que, de otro modo, podrían ocultarse.</span><span class="sxs-lookup"><span data-stu-id="6e94b-104">The keyboard preference parameter indicates that the user relies on the keyboard instead of the mouse, so applications should display keyboard interfaces that would otherwise be hidden.</span></span>

<span data-ttu-id="6e94b-105">El usuario controla el valor del parámetro de preferencias de teclado mediante el centro de accesibilidad del panel de control u otra aplicación para personalizar el entorno.</span><span class="sxs-lookup"><span data-stu-id="6e94b-105">The user controls the setting of the keyboard preference parameter by using the Ease of Access Center in Control Panel, or another application for customizing the environment.</span></span> <span data-ttu-id="6e94b-106">Las aplicaciones usan las marcas **SPI \_ GETKEYBOARDPREF** y **SPI \_ SETKEYBOARDPREF** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro de preferencias de teclado.</span><span class="sxs-lookup"><span data-stu-id="6e94b-106">Applications use the **SPI\_GETKEYBOARDPREF** and **SPI\_SETKEYBOARDPREF** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the keyboard preference parameter.</span></span>

<span data-ttu-id="6e94b-107">Además, en Windows 2000, los usuarios pueden establecer un parámetro que indique si las teclas de acceso de los menús siempre están subrayadas.</span><span class="sxs-lookup"><span data-stu-id="6e94b-107">Additionally, on Windows 2000, users can set a parameter that indicates whether menu access keys are always underlined.</span></span> <span data-ttu-id="6e94b-108">Las aplicaciones usan las marcas **SPI \_ GETMENUUNDERLINES** y **SPI \_ SETMENUUNDERLINES** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro subrayado del menú.</span><span class="sxs-lookup"><span data-stu-id="6e94b-108">Applications use the **SPI\_GETMENUUNDERLINES** and **SPI\_SETMENUUNDERLINES** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the menu underlines parameter.</span></span>

<span data-ttu-id="6e94b-109">Cuando una aplicación recibe un mensaje de [**\_ SETTINGCHANGE de WM**](/windows/desktop/winmsg/wm-settingchange) para el parámetro de preferencia de teclado o de subrayado de menú, se recomienda que la aplicación llame a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para actualizar la información de ambos parámetros.</span><span class="sxs-lookup"><span data-stu-id="6e94b-109">When an application receives a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message for either the keyboard preference or menu underline parameter, it is recommended that the application call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) to update the information for both parameters.</span></span>

<span data-ttu-id="6e94b-110">Tenga en cuenta que **SPI \_ GETMENUUNDERLINES** es el mismo que **SPI \_ GETKEYBOARDCUES** y **SPI \_ SETMENUUNDERLINES** es igual que **SPI \_ SETKEYBOARDCUES**.</span><span class="sxs-lookup"><span data-stu-id="6e94b-110">Note that **SPI\_GETMENUUNDERLINES** is the same as **SPI\_GETKEYBOARDCUES**, and **SPI\_SETMENUUNDERLINES** is the same as **SPI\_SETKEYBOARDCUES**.</span></span>

 

 