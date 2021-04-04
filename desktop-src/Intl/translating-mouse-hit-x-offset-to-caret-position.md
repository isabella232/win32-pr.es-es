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
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Trasladar el desplazamiento de la X hasta la posición del símbolo de intercalación

Convencionalmente, el usuario puede seleccionar posición del símbolo de intercalación (CP) haciendo clic en la mitad final del carácter "CP-1" o en la mitad inicial del carácter "CP". Una aplicación puede implementar la traslación del desplazamiento de x del mouse en la posición del símbolo de intercalación como se indica a continuación:


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



En el caso de los scripts que ajustan el símbolo de intercalación a los límites del clúster, una llamada a [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) devuelve con *fTrailing* establecido en 0 o en el ancho del clúster en los puntos de código.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



