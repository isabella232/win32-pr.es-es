---
description: Una de las principales características de las funciones de la API de impresión de GDI es su compatibilidad con la independencia del dispositivo.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Acerca de la API de impresión GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697517"
---
# <a name="about-the-gdi-print-api"></a><span data-ttu-id="a03e4-103">Acerca de la API de impresión GDI</span><span class="sxs-lookup"><span data-stu-id="a03e4-103">About the GDI Print API</span></span>

<span data-ttu-id="a03e4-104">Una de las principales características de las funciones de la API de impresión de GDI es su compatibilidad con la independencia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a03e4-104">One of the chief features of the functions in the GDI print API is their support of device independence.</span></span> <span data-ttu-id="a03e4-105">En lugar de emitir comandos específicos del dispositivo para dibujar la salida en una impresora o un trazador determinado, una aplicación llama a funciones de alto nivel desde la interfaz de dispositivo gráfico (GDI).</span><span class="sxs-lookup"><span data-stu-id="a03e4-105">Instead of issuing device-specific commands to draw output on a particular printer or plotter, an application calls high-level functions from the graphics device interface (GDI).</span></span> <span data-ttu-id="a03e4-106">Por ejemplo, para imprimir una imagen de mapa de bits, una aplicación puede llamar a la función [**bitblt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) y proporcionar las coordenadas para el mapa de bits, así como los identificadores de los contextos de dispositivos de origen y de destino (DC).</span><span class="sxs-lookup"><span data-stu-id="a03e4-106">For example, to print a bitmapped image, an application can call the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function, supplying the coordinates for the bitmap as well as handles identifying the source and destination device contexts (DCs).</span></span> <span data-ttu-id="a03e4-107">A continuación, el controlador de impresora convierte la llamada a **bitblt** en los comandos de dispositivo sin formato.</span><span class="sxs-lookup"><span data-stu-id="a03e4-107">The call to **BitBlt** is then converted to raw device commands by a printer driver.</span></span> <span data-ttu-id="a03e4-108">Un controlador de dispositivo es una biblioteca de vínculos dinámicos (DLL) que admite la interfaz de controlador de dispositivo (DDI).</span><span class="sxs-lookup"><span data-stu-id="a03e4-108">A device driver is a dynamic-link library (DLL) that supports the device driver interface (DDI).</span></span> <span data-ttu-id="a03e4-109">Un controlador de dispositivo genera comandos de dispositivo sin formato cuando procesa llamadas a funciones DDI realizadas por el motor de gráficos.</span><span class="sxs-lookup"><span data-stu-id="a03e4-109">A device driver generates raw device commands when it processes calls to DDI functions made by the graphics engine.</span></span> <span data-ttu-id="a03e4-110">La impresora procesa los comandos cuando imprime la imagen.</span><span class="sxs-lookup"><span data-stu-id="a03e4-110">The commands are processed by the printer when it prints the image.</span></span> <span data-ttu-id="a03e4-111">La sintaxis, el número y el tipo de estos comandos varían de un dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a03e4-111">The syntax, number, and type of these commands vary from device to device.</span></span>

<span data-ttu-id="a03e4-112">En esta información general se proporciona información sobre los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="a03e4-112">This overview provides information on the following topics.</span></span>

<dl>

[<span data-ttu-id="a03e4-113">Interfaz de impresión predeterminada</span><span class="sxs-lookup"><span data-stu-id="a03e4-113">Default Printing Interface</span></span>](default-printing-interface.md)  
[<span data-ttu-id="a03e4-114">Contextos de dispositivo de impresora</span><span class="sxs-lookup"><span data-stu-id="a03e4-114">Printer Device Contexts</span></span>](printer-output.md)  
[<span data-ttu-id="a03e4-115">Escapes de impresora</span><span class="sxs-lookup"><span data-stu-id="a03e4-115">Printer Escapes</span></span>](printer-escapes.md)  
[<span data-ttu-id="a03e4-116">Presentación y salida de WYSIWYG</span><span class="sxs-lookup"><span data-stu-id="a03e4-116">WYSIWYG Display and Output</span></span>](wysiwyg-display-and-output.md)  
[<span data-ttu-id="a03e4-117">DEVMODE por usuario</span><span class="sxs-lookup"><span data-stu-id="a03e4-117">Per-User DEVMODE</span></span>](per-user-devmode.md)  
</dl>

 

 
