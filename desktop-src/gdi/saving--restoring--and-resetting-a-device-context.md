---
description: 'Las siguientes funciones permiten a una aplicación guardar, restaurar y restablecer un contexto de dispositivo: SaveDC, RestoreDC y ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Guardar, restaurar y restablecer un contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985555"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a><span data-ttu-id="e39af-103">Guardar, restaurar y restablecer un contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e39af-103">Saving, Restoring, and Resetting a Device Context</span></span>

<span data-ttu-id="e39af-104">Las siguientes funciones permiten a una aplicación guardar, restaurar y restablecer un contexto de dispositivo: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)y [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span><span class="sxs-lookup"><span data-stu-id="e39af-104">The following functions enable an application to save, restore, and reset a device context: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc), and [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span></span> <span data-ttu-id="e39af-105">La función SaveDC registra en una pila de GDI especial los objetos gráficos del controlador de dominio actual y sus atributos, y los modos gráficos.</span><span class="sxs-lookup"><span data-stu-id="e39af-105">The SaveDC function records on a special GDI stack the current DC's graphic objects and their attributes, and graphic modes.</span></span> <span data-ttu-id="e39af-106">Una aplicación de dibujo puede llamar a esta función antes de que un usuario empiece a dibujar y guardar el estado original de la aplicación proporcionando una pizarra limpia para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e39af-106">A drawing application can call this function before a user begins drawing and save the application's original state providing a clean slate for the user.</span></span> <span data-ttu-id="e39af-107">Para volver a este estado original, la aplicación llama a la función RestoreDC.</span><span class="sxs-lookup"><span data-stu-id="e39af-107">To return to this original state, the application calls the RestoreDC function.</span></span>

<span data-ttu-id="e39af-108">Se proporciona [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) para restablecer los datos de DC de la impresora.</span><span class="sxs-lookup"><span data-stu-id="e39af-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) is provided to reset printer DC data.</span></span> <span data-ttu-id="e39af-109">Una aplicación llama a esta función para restablecer la orientación del papel, el tamaño del papel, el factor de escala de salida, el número de copias que se van a imprimir, el origen del papel (o la ubicación), el modo dúplex, etc.</span><span class="sxs-lookup"><span data-stu-id="e39af-109">An application calls this function to reset the paper orientation, paper size, output scaling factor, number of copies to be printed, paper source (or bin), duplex mode, and so on.</span></span> <span data-ttu-id="e39af-110">Normalmente, una aplicación llama a esta función después de que un usuario ha cambiado una de las opciones de la impresora y el sistema ha emitido un mensaje de [**\_ DEVMODECHANGE de WM**](wm-devmodechange.md) .</span><span class="sxs-lookup"><span data-stu-id="e39af-110">Typically, an application calls this function after a user has changed one of the printer options and the system has issued a [**WM\_DEVMODECHANGE**](wm-devmodechange.md) message.</span></span>

 

 



