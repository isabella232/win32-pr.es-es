---
description: Las funciones ImageHlp las usan principalmente las herramientas de programación, las utilidades de instalación de aplicaciones y otros programas que necesitan acceso a los datos contenidos en una imagen PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Acerca de ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659429"
---
# <a name="about-imagehlp"></a><span data-ttu-id="92739-103">Acerca de ImageHlp</span><span class="sxs-lookup"><span data-stu-id="92739-103">About ImageHlp</span></span>

<span data-ttu-id="92739-104">Las funciones ImageHlp las usan principalmente las herramientas de programación, las utilidades de instalación de aplicaciones y otros programas que necesitan acceso a los datos contenidos en una imagen PE.</span><span class="sxs-lookup"><span data-stu-id="92739-104">The ImageHlp functions are used mostly by programming tools, application setup utilities, and other programs that need access to the data contained in a PE image.</span></span> <span data-ttu-id="92739-105">Todas las funciones ImageHlp tienen un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="92739-105">All ImageHlp functions are single threaded.</span></span> <span data-ttu-id="92739-106">Por lo tanto, las llamadas desde más de un subproceso a esta función probablemente producirán un comportamiento inesperado o daños en la memoria.</span><span class="sxs-lookup"><span data-stu-id="92739-106">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="92739-107">Para evitar esto, debe sincronizar todas las llamadas simultáneas de más de un subproceso a esta función.</span><span class="sxs-lookup"><span data-stu-id="92739-107">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

<span data-ttu-id="92739-108">En los temas siguientes se describen las imágenes PE y la funcionalidad proporcionada por las funciones ImageHlp.</span><span class="sxs-lookup"><span data-stu-id="92739-108">The following topics describe PE images and the functionality provided by the ImageHlp functions.</span></span>

-   [<span data-ttu-id="92739-109">Formato PE</span><span class="sxs-lookup"><span data-stu-id="92739-109">PE Format</span></span>](pe-format.md)
-   [<span data-ttu-id="92739-110">Funciones de acceso a imágenes</span><span class="sxs-lookup"><span data-stu-id="92739-110">Image Access Functions</span></span>](image-access-functions.md)
-   [<span data-ttu-id="92739-111">Funciones de integridad de la imagen</span><span class="sxs-lookup"><span data-stu-id="92739-111">Image Integrity Functions</span></span>](image-integrity-functions.md)
-   [<span data-ttu-id="92739-112">Funciones de modificación de imágenes</span><span class="sxs-lookup"><span data-stu-id="92739-112">Image Modification Functions</span></span>](image-modification-functions.md)

 

 



