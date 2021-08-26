---
description: La clave del Registro EUDC contiene una o varias subclaves que contienen valores que definen las fuentes asociadas a caracteres definidos por el usuario final (EUDC) para una página de códigos determinada.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a7509364545d9de01d4480a58d4e6af8043c30fa8f74db0fdbaf24e252e298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082995"
---
# <a name="eudc"></a>EUDC

La clave del Registro EUDC contiene una o varias subclaves que contienen valores que definen las fuentes asociadas a caracteres definidos por el usuario final [(EUDC)](end-user-defined-characters.md) para una página de códigos determinada. Tiene la siguiente ubicación del Registro:

HKEY \_ CURRENT \_ USER \\ EUDC

El formato es:

EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName

donde:



| Value                         | Descripción                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Nombre predefinido usado para establecer la fuente predeterminada del sistema. No hay ninguna fuente EUDC predeterminada del sistema a menos que esta entrada se especifique explícitamente.     |
| TrueTypeFontTypeface     | Nombre definido por el usuario asociado a una fuente TrueType que no sea EUDC.                                                                              |
| TrueTypeEUDCFontFileName | Cadena que consta del nombre de archivo de un archivo de fuente EUDC independiente. Este archivo identifica una fuente que se va a asociar a TrueTypeFontTypeface. |



 

En el ejemplo siguiente se muestra la clave EUDC para la página de códigos 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



En el ejemplo siguiente se establece la fuente EUDC predeterminada del sistema como Eudc.ttf y se asocian las fuentes EUDC independientes Mineudc.ttf y Goteudc.ttf con los nombres de fuente MS Mincho y MS Italic, respectivamente.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Cuando la página de códigos Windows (ACP del sistema) asociada al idioma de los programas no Unicode coincide con la subclave, el subsistema GDI busca los pares de valores de subclave para obtener información de visualización sobre el carácter. Primero busca un nombre que coincida con la fuente actual. Si no hay ninguno, examina el valor SystemDefaultEUDCFont. Si no se define ningún valor, GDI trata el carácter como indefinido.

Tenga en cuenta que el propio texto no tiene que estar en la Windows de códigos. Por ejemplo, suponga que la página de códigos tiene el identificador 1252, el valor predeterminado Windows página de códigos para inglés. Una aplicación pasa el único punto de código Unicode U+E000, en el área de uso privado (PUA) unicode, [**a DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). En este caso, GDI examina los valores del Registro en 1252 para obtener la información de fuente de las propiedades de visualización de caracteres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entradas del Registro eudc](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
