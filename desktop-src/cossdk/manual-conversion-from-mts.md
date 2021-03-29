---
description: Conversión manual desde MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversión manual desde MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807375"
---
# <a name="manual-conversion-from-mts"></a><span data-ttu-id="92351-103">Conversión manual desde MTS</span><span class="sxs-lookup"><span data-stu-id="92351-103">Manual Conversion from MTS</span></span>

<span data-ttu-id="92351-104">Es posible que desee aislar la conversión de paquetes MTS en aplicaciones COM+ para que quede fuera del proceso de instalación de Windows.</span><span class="sxs-lookup"><span data-stu-id="92351-104">You might want to isolate conversion of MTS packages to COM+ applications so that it is outside the Windows setup process.</span></span> <span data-ttu-id="92351-105">El siguiente procedimiento ofrece un enfoque alternativo:</span><span class="sxs-lookup"><span data-stu-id="92351-105">The following procedure offers an alternate approach:</span></span>

1.  <span data-ttu-id="92351-106">Exporte los paquetes MTS mediante la característica de exportación de paquetes MTS 2,0 (lo que da como resultado un archivo de paquete MTS y una colección de otros archivos).</span><span class="sxs-lookup"><span data-stu-id="92351-106">Export the MTS packages using the MTS 2.0 Package Export feature (resulting in an MTS package file and a collection of other files).</span></span>
2.  <span data-ttu-id="92351-107">Elimine los paquetes MTS y actualice Windows, o realice una instalación limpia de Windows.</span><span class="sxs-lookup"><span data-stu-id="92351-107">Delete the MTS packages and upgrade Windows, or perform a clean installation of Windows.</span></span>
3.  <span data-ttu-id="92351-108">Instale los archivos de paquete MTS (. Pak) en un sistema Windows 2000 o posterior mediante el Asistente para instalación de aplicaciones de la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="92351-108">Install the MTS package (.pak) files on a Windows 2000 or later system by using the Component Services administrative tool's Application Install wizard.</span></span> <span data-ttu-id="92351-109">También tendrá que restablecer la identidad "ejecutar como" de la aplicación en el registro del sistema en **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID \\ runas**.</span><span class="sxs-lookup"><span data-stu-id="92351-109">You will also need to reset the application's "Run As" identity in the system registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\APPID\\RunAs**.</span></span>

> [!Note]  
> <span data-ttu-id="92351-110">Solo el procedimiento de conversión automática (a través del programa de instalación de Windows o mediante la utilidad MTSTOCOM) genera el archivo de registro MTSTOCOM.</span><span class="sxs-lookup"><span data-stu-id="92351-110">Only the automatic conversion procedure (through Windows setup or by running the MTSTOCOM utility) generates the MTSTOCOM log file.</span></span> <span data-ttu-id="92351-111">Este archivo no se genera al seguir el procedimiento de conversión manual.</span><span class="sxs-lookup"><span data-stu-id="92351-111">This file is not generated when following the manual conversion procedure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="92351-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92351-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92351-113">Conversión automática desde MTS</span><span class="sxs-lookup"><span data-stu-id="92351-113">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="92351-114">Resultados y problemas de la conversión de COM+</span><span class="sxs-lookup"><span data-stu-id="92351-114">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="92351-115">Biblioteca de administración de MTS</span><span class="sxs-lookup"><span data-stu-id="92351-115">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



