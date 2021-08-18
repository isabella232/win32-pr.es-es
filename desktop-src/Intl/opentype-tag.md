---
description: Define una matriz de 4 bytes que contiene cuatro valores ASCII de 8 bits de espacio, A-Z o a-z para identificar etiquetas de características de fuente, lenguaje y script OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c784fa7f6243e7e5444dcbc64c690ce7184d6ace469759c19be9de87854732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040785"
---
# <a name="opentype_tag"></a>ETIQUETA \_ OPENTYPE

Define una matriz de 4 bytes que contiene cuatro valores ASCII de 8 bits de espacio, A-Z o a-z para identificar etiquetas de características de fuente, lenguaje y script OpenType.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Comentarios

En los ejemplos siguientes se definen representaciones de etiquetas de características OpenType.

-   La etiqueta de característica de la característica de ligadura es "liga".
-   Las etiquetas de idioma para el idioma Desánido, Urdu y Persa son "ROM", "URD" y "FAR", respectivamente. Tenga en cuenta que cada una de estas etiquetas termina con un espacio.
-   Las etiquetas de script para los scripts latinos y árabes son "latn" y "arabic", respectivamente.

Para obtener más información sobre las etiquetas de características de OpenType y la especificación openType, vea <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Redistribuible<br/>          | Usp10.dll versión 1.600 o posterior en Windows XPand más adelante<br/>                |
| Header<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Estructuras de unidireccional](uniscribe-structures.md)
</dt> <dt>

[**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




