---
description: Convencionalmente, el usuario puede seleccionar la posición del carácter de asociación (cp) haciendo clic en la mitad final del carácter &\# 0034;cp-1&0034; o la mitad inicial del \# carácter &\# 0034;cp&\# 0034;.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Traducción del desplazamiento X de posicionamiento del mouse a la posición del cursor de cursor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e135efaccb6454e55999d21f00e762d749eb380751848aef88cf4b4e5b8e913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693185"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Traducción del desplazamiento X de posicionamiento del mouse a la posición del cursor de cursor

Convencionalmente, el usuario puede seleccionar la posición del carácter de vínculo (cp) haciendo clic en la mitad final del carácter "cp-1" o en la mitad inicial del carácter "cp". Una aplicación puede implementar la traducción del desplazamiento x de la pulsación del mouse para la posición del cursor de cursor como se muestra a continuación:


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



En el caso de los scripts que acoplan el cursor de cursor a los límites del clúster, se devuelve una llamada a [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) con *fTrailing* establecido en 0 o el ancho del clúster en puntos de código.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



