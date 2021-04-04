---
description: Convencionalmente, el usuario puede seleccionar posición del símbolo de intercalación (CP) haciendo clic en la mitad final del carácter &\# 0034; CP-1&\# 0034; o en la mitad inicial del carácter &\# 0034; CP&\# 0034;.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Trasladar el desplazamiento de la X hasta la posición del símbolo de intercalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f993de35ebffac4740b367927d1a8edf864a813e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910102"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a><span data-ttu-id="4d8fe-103">Trasladar el desplazamiento de la X hasta la posición del símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="4d8fe-103">Translating Mouse Hit X Offset to Caret Position</span></span>

<span data-ttu-id="4d8fe-104">Convencionalmente, el usuario puede seleccionar posición del símbolo de intercalación (CP) haciendo clic en la mitad final del carácter "CP-1" o en la mitad inicial del carácter "CP".</span><span class="sxs-lookup"><span data-stu-id="4d8fe-104">Conventionally, the user can select caret position (cp) by clicking either the trailing half of character "cp-1" or the leading half of character "cp".</span></span> <span data-ttu-id="4d8fe-105">Una aplicación puede implementar la traslación del desplazamiento de x del mouse en la posición del símbolo de intercalación como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="4d8fe-105">An application can implement the translation of mouse hit x offset to caret position as follows:</span></span>


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



<span data-ttu-id="4d8fe-106">En el caso de los scripts que ajustan el símbolo de intercalación a los límites del clúster, una llamada a [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) devuelve con *fTrailing* establecido en 0 o en el ancho del clúster en los puntos de código.</span><span class="sxs-lookup"><span data-stu-id="4d8fe-106">For scripts that snap the caret to cluster boundaries, a call to [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) returns with *fTrailing* set to either 0 or the width of the cluster in code points.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d8fe-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d8fe-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d8fe-108">Usar Uniscribe</span><span class="sxs-lookup"><span data-stu-id="4d8fe-108">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



