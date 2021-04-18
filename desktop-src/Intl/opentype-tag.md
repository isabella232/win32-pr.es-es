---
description: Define una matriz de 4 bytes que contiene los valores ASCII de 4 8 bits de espacio, A-Z o a-z para identificar las etiquetas de características de fuente, idioma y script OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687192"
---
# <a name="opentype_tag"></a>\_etiqueta OPENTYPE

Define una matriz de 4 bytes que contiene los valores ASCII de 4 8 bits de espacio, A-Z o a-z para identificar las etiquetas de características de fuente, idioma y script OpenType.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Observaciones

En los siguientes ejemplos se definen representaciones de etiquetas de características OpenType.

-   La etiqueta de característica de la característica de ligadura es "Liga".
-   Las etiquetas de idioma para rumano, urdu y persa son "ROM", "URD" y "FAR", respectivamente. Tenga en cuenta que cada una de estas etiquetas finaliza con un espacio.
-   Las etiquetas de script para los scripts latinos y árabes son "latn" y "árabe", respectivamente.

Para obtener más información sobre las etiquetas de las características OpenType y la especificación OpenType, vea <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Redistribuible<br/>          | Usp10.dll la versión 1,600 o superior de la ventana de Windows más adelante<br/>                |
| Encabezado<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Estructuras de Uniscribe](uniscribe-structures.md)
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

 

 




