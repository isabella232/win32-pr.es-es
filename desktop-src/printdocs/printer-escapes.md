---
description: Los escapes de impresora proporcionados por Windows de 16 bits permitían el acceso a las características especiales del dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Escapes de impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277437"
---
# <a name="printer-escapes"></a><span data-ttu-id="225f2-103">Escapes de impresora</span><span class="sxs-lookup"><span data-stu-id="225f2-103">Printer Escapes</span></span>

<span data-ttu-id="225f2-104">Los escapes de impresora proporcionados por Windows de 16 bits permitían el acceso a las características especiales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="225f2-104">The printer escapes provided by 16-bit Windows allowed access special device features.</span></span> <span data-ttu-id="225f2-105">La mayoría de estos escapes están obsoletos, pero se proporcionan algunos para simplificar la migración de aplicaciones basadas en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="225f2-105">Most of these escapes are obsolete, but a few are provided to simplify the porting of 16-bit Windows-based applications.</span></span> <span data-ttu-id="225f2-106">GDI admite un conjunto completo de funciones de ruta de acceso que las aplicaciones pueden usar en lugar de los escapes para dibujar trazados en cualquier dispositivo.</span><span class="sxs-lookup"><span data-stu-id="225f2-106">GDI supports a complete set of path functions that applications can use instead of the escapes to draw paths on any device.</span></span> <span data-ttu-id="225f2-107">Para obtener una lista de las funciones que reemplazan algunos de los escapes, vea la función [**escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .</span><span class="sxs-lookup"><span data-stu-id="225f2-107">For a list of functions that replace some of the escapes, see the [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) function.</span></span>

<span data-ttu-id="225f2-108">De los escapes de impresora originales 64, solo se pueden usar **QUERYESCSUPPORT** y **PASSTHROUGH** .</span><span class="sxs-lookup"><span data-stu-id="225f2-108">Of the 64 original printer escapes, only **QUERYESCSUPPORT** and **PASSTHROUGH** can be used.</span></span>

<span data-ttu-id="225f2-109">También hay una función de escape extendida denominada [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="225f2-109">There is also an extended escape function called [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="225f2-110">Esta función permite a las aplicaciones tener acceso a las capacidades de un dispositivo determinado que no están directamente disponibles a través de GDI.</span><span class="sxs-lookup"><span data-stu-id="225f2-110">This function allows applications to access capabilities of a particular device not directly available through GDI.</span></span>

 

 



