---
description: El controlador de dominio de impresora se puede usar al imprimir en una impresora de matriz de puntos, una impresora de inyección de tinta, una impresora láser o un trazador.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Contextos de dispositivo de impresora (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984854"
---
# <a name="printer-device-contexts-windows-gdi"></a><span data-ttu-id="89f00-103">Contextos de dispositivo de impresora (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="89f00-103">Printer Device Contexts (Windows GDI)</span></span>

<span data-ttu-id="89f00-104">El controlador de dominio de impresora se puede usar al imprimir en una impresora de matriz de puntos, una impresora de inyección de tinta, una impresora láser o un trazador.</span><span class="sxs-lookup"><span data-stu-id="89f00-104">The printer DC can be used when printing on a dot-matrix printer, ink-jet printer, laser printer, or plotter.</span></span> <span data-ttu-id="89f00-105">Una aplicación crea un controlador de dominio de impresora mediante una llamada a la función [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) y proporcionando los argumentos adecuados (el nombre del controlador de impresora, el nombre de la impresora, el nombre de archivo o dispositivo para el medio de salida físico y otros datos de inicialización).</span><span class="sxs-lookup"><span data-stu-id="89f00-105">An application creates a printer DC by calling the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function and supplying the appropriate arguments (the name of the printer driver, the name of the printer, the file or device name for the physical output medium, and other initialization data).</span></span> <span data-ttu-id="89f00-106">Cuando una aplicación ha terminado de imprimirse, elimina el controlador de dominio de la impresora mediante una llamada a la función [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="89f00-106">When an application has finished printing, it deletes the printer DC by calling the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span> <span data-ttu-id="89f00-107">Una aplicación debe eliminar (en lugar de liberar) un controlador de dominio de impresora; se produce un error en la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) cuando una aplicación intenta utilizarla para liberar un controlador de dominio de impresora.</span><span class="sxs-lookup"><span data-stu-id="89f00-107">An application must delete (rather than release) a printer DC; the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function fails when an application attempts to use it to release a printer DC.</span></span>

<span data-ttu-id="89f00-108">Para obtener más información, consulte la salida de la [impresora](../printdocs/printer-output.md).</span><span class="sxs-lookup"><span data-stu-id="89f00-108">For more information, see [Printer Output](../printdocs/printer-output.md).</span></span>

 

 
