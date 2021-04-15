---
description: Cuando una aplicación convierte cadenas de ASCII o de una página de códigos de Windows (ANSI) a Unicode, debe convertir las secuencias de escape carácter a carácter en Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Usar secuencias de escape y caracteres de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688701"
---
# <a name="using-escape-sequences-and-control-characters"></a><span data-ttu-id="e25ff-103">Usar secuencias de escape y caracteres de control</span><span class="sxs-lookup"><span data-stu-id="e25ff-103">Using Escape Sequences and Control Characters</span></span>

<span data-ttu-id="e25ff-104">Cuando una aplicación convierte cadenas de ASCII o de una [Página de códigos de Windows (ANSI)](code-pages.md) a Unicode, debe convertir las secuencias de escape carácter a carácter en Unicode.</span><span class="sxs-lookup"><span data-stu-id="e25ff-104">When an application converts strings from ASCII or from a [Windows (ANSI) code page](code-pages.md) to Unicode, it should translate escape sequences character-by-character into Unicode.</span></span> <span data-ttu-id="e25ff-105">Cuando se convierte un archivo de texto ASCII u otro archivo de 8 bits en Unicode, existe la posibilidad de que se convierta posteriormente.</span><span class="sxs-lookup"><span data-stu-id="e25ff-105">When an ASCII or other 8-bit text file is converted to Unicode, there is a chance that it will subsequently be converted back.</span></span> <span data-ttu-id="e25ff-106">Convertir secuencias de escape en Unicode carácter a carácter, en lugar de combinarlas como un solo carácter Unicode, permite realizar la conversión inversa sin necesidad de reconocer y analizar las secuencias de escape como tal.</span><span class="sxs-lookup"><span data-stu-id="e25ff-106">Converting escape sequences into Unicode on a character-by-character basis, instead of combining them as a single Unicode character, makes it possible to perform the reverse conversion without needing to recognize and parse the escape sequences as such.</span></span> <span data-ttu-id="e25ff-107">Por ejemplo, ESC + A debe ser 0x001B (ESC), 0x0041 (A), en lugar de 0x411B.</span><span class="sxs-lookup"><span data-stu-id="e25ff-107">For example, ESC+A should become 0x001B (ESC), 0x0041 (A), instead of 0x411B.</span></span>

<span data-ttu-id="e25ff-108">Los primeros valores de código de 32 16 bits en Unicode están diseñados para los caracteres de control 32.</span><span class="sxs-lookup"><span data-stu-id="e25ff-108">The first 32 16-bit code values in Unicode are intended for the 32 control characters.</span></span> <span data-ttu-id="e25ff-109">Esta especificación admite el uso existente de caracteres de control para la aplicación de formato.</span><span class="sxs-lookup"><span data-stu-id="e25ff-109">This specification supports the existing use of control characters for formatting purposes.</span></span> <span data-ttu-id="e25ff-110">Las aplicaciones Unicode pueden tratar estos caracteres de control exactamente de la misma manera que tratan sus equivalentes ASCII.</span><span class="sxs-lookup"><span data-stu-id="e25ff-110">Unicode applications can treat these control characters in exactly the same way as they treat their ASCII equivalents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e25ff-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e25ff-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e25ff-112">Usar caracteres especiales en Unicode</span><span class="sxs-lookup"><span data-stu-id="e25ff-112">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



