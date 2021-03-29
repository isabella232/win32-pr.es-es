---
title: Generar códigos de Four-Character
description: Generar códigos de Four-Character
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- e/s de archivos multimedia, códigos de cuatro caracteres
- e/s de archivos, códigos de cuatro caracteres
- entrada y salida (e/s), códigos de cuatro caracteres
- E/s (entrada y salida), códigos de cuatro caracteres
- códigos de cuatro caracteres
- mmioStringToFOURCC función)
- mmioFOURCC (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789993"
---
# <a name="generating-four-character-codes"></a><span data-ttu-id="37ccd-110">Generar códigos de Four-Character</span><span class="sxs-lookup"><span data-stu-id="37ccd-110">Generating Four-Character Codes</span></span>

<span data-ttu-id="37ccd-111">Puede usar la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) o la función [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) para generar códigos de cuatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="37ccd-111">You can use the [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) macro or the [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) function to generate four-character codes.</span></span> <span data-ttu-id="37ccd-112">En el ejemplo siguiente se usa **mmioFOURCC** para generar un código de cuatro caracteres para "Wave".</span><span class="sxs-lookup"><span data-stu-id="37ccd-112">The following example uses **mmioFOURCC** to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



<span data-ttu-id="37ccd-113">En el ejemplo siguiente se usa [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) para generar un código de cuatro caracteres para "Wave".</span><span class="sxs-lookup"><span data-stu-id="37ccd-113">The following example uses [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



<span data-ttu-id="37ccd-114">El segundo parámetro de [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) especifica las marcas para convertir la cadena en un código de cuatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="37ccd-114">The second parameter in [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) specifies flags for converting the string to a four-character code.</span></span> <span data-ttu-id="37ccd-115">Si especifica la marca de el \_ valor de TOUPPER, **mmioStringToFOURCC** convierte todos los caracteres alfabéticos de la cadena a mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="37ccd-115">If you specify the MMIO\_TOUPPER flag, **mmioStringToFOURCC** converts all alphabetic characters in the string to uppercase.</span></span> <span data-ttu-id="37ccd-116">Esto resulta útil si necesita especificar un código de cuatro caracteres para identificar un procedimiento de e/s personalizado, ya que los códigos de cuatro caracteres que identifican los nombres de extensión de archivo deben estar en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="37ccd-116">This is useful when you need to specify a four-character code to identify a custom I/O procedure because four-character codes identifying file-extension names must be all uppercase.</span></span>

 

 