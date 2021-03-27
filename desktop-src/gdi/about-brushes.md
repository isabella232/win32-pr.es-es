---
description: 'Hay dos tipos de pinceles: lógico y físico.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Acerca de los pinceles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155212"
---
# <a name="about-brushes"></a><span data-ttu-id="0c1a3-103">Acerca de los pinceles</span><span class="sxs-lookup"><span data-stu-id="0c1a3-103">About Brushes</span></span>

<span data-ttu-id="0c1a3-104">Hay dos tipos de pinceles: lógico y físico.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-104">There are two types of brushes: logical and physical.</span></span> <span data-ttu-id="0c1a3-105">Un *pincel lógico* es una descripción del mapa de bits ideal que una aplicación usa para pintar formas.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-105">A *logical brush* is a description of the ideal bitmap that an application uses to paint shapes.</span></span> <span data-ttu-id="0c1a3-106">Un *pincel físico* es el mapa de bits real que un controlador de dispositivo crea en función de la definición de pincel lógico de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-106">A *physical brush* is the actual bitmap that a device driver creates based on an application's logical-brush definition.</span></span> <span data-ttu-id="0c1a3-107">Para obtener más información sobre los mapas de bits, vea [mapas de bits](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="0c1a3-107">For more information about bitmaps, see [Bitmaps](bitmaps.md).</span></span>

<span data-ttu-id="0c1a3-108">Cuando una aplicación llama a una de las funciones que crea un pincel, recupera un identificador que identifica un pincel lógico.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-108">When an application calls one of the functions that creates a brush, it retrieves a handle that identifies a logical brush.</span></span> <span data-ttu-id="0c1a3-109">Cuando la aplicación pasa este identificador a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , el controlador de dispositivo de la pantalla o impresora correspondiente crea el pincel físico.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-109">When the application passes this handle to the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function, the device driver for the corresponding display or printer creates the physical brush.</span></span>

<span data-ttu-id="0c1a3-110">En los temas siguientes se describen los pinceles:</span><span class="sxs-lookup"><span data-stu-id="0c1a3-110">The following topics describe brushes:</span></span>

-   [<span data-ttu-id="0c1a3-111">Origen del pincel</span><span class="sxs-lookup"><span data-stu-id="0c1a3-111">Brush Origin</span></span>](brush-origin.md)
-   [<span data-ttu-id="0c1a3-112">Tipos de pinceles lógicos</span><span class="sxs-lookup"><span data-stu-id="0c1a3-112">Logical Brush Types</span></span>](logical-brush-types.md)
-   [<span data-ttu-id="0c1a3-113">Transferencia de bloque de patrón</span><span class="sxs-lookup"><span data-stu-id="0c1a3-113">Pattern Block Transfer</span></span>](pattern-block-transfer.md)
-   [<span data-ttu-id="0c1a3-114">Funciones de pincel habilitadas para ICM</span><span class="sxs-lookup"><span data-stu-id="0c1a3-114">ICM-Enabled Brush Functions</span></span>](icm-enabled-brush-functions.md)

 

 



