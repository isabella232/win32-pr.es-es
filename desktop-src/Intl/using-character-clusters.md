---
description: Los clústeres de caracteres son secuencias de glifo que no se pueden dividir entre líneas.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Uso de clústeres de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819006"
---
# <a name="using-character-clusters"></a><span data-ttu-id="67906-103">Uso de clústeres de caracteres</span><span class="sxs-lookup"><span data-stu-id="67906-103">Using Character Clusters</span></span>

<span data-ttu-id="67906-104">Los clústeres de caracteres son secuencias de glifo que no se pueden dividir entre líneas.</span><span class="sxs-lookup"><span data-stu-id="67906-104">Character clusters are glyph sequences that cannot be split between lines.</span></span> <span data-ttu-id="67906-105">Algunos lenguajes, por ejemplo tailandés e hindú, restringen la colocación del símbolo de intercalación a puntos entre los clústeres.</span><span class="sxs-lookup"><span data-stu-id="67906-105">Some languages, for example Thai and Indic, restrict caret placement to points between clusters.</span></span> <span data-ttu-id="67906-106">Esta restricción se aplica al movimiento de intercalación iniciado con las acciones del teclado o del mouse (prueba de posicionamiento).</span><span class="sxs-lookup"><span data-stu-id="67906-106">This restriction applies to caret movement initiated with keyboard or mouse actions (hit testing).</span></span>

<span data-ttu-id="67906-107">Uniscribe proporciona información del clúster en los atributos visuales contenidos en una estructura [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr) y los atributos lógicos contenidos en una estructura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="67906-107">Uniscribe provides cluster information in both the visual attributes contained in a [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure, and the logical attributes contained in a [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="67906-108">Una vez que la aplicación llama a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), la información del clúster se representa mediante secuencias del mismo valor en la matriz de **\_ LOGATTR de script** y el miembro **fClusterStart** de la matriz de **script \_ VISATTR** .</span><span class="sxs-lookup"><span data-stu-id="67906-108">After the application calls [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), the cluster information is represented both by sequences of the same value in the **SCRIPT\_LOGATTR** array, and by the **fClusterStart** member in the **SCRIPT\_VISATTR** array.</span></span>

<span data-ttu-id="67906-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) también recupera el miembro **fCharStop** de la estructura [**\_ LOGATTR del script**](/windows/win32/api/usp10/ns-usp10-script_logattr) para identificar las posiciones del clúster.</span><span class="sxs-lookup"><span data-stu-id="67906-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) also retrieves the **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure to identify cluster positions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67906-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67906-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67906-111">Usar Uniscribe</span><span class="sxs-lookup"><span data-stu-id="67906-111">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



