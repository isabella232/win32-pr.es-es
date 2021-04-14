---
description: La clave del registro EUDC contiene una o más subclaves que contienen valores que definen las fuentes asociadas a los caracteres definidos por el usuario final (EUDCs) de una página de códigos determinada.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668411"
---
# <a name="eudc"></a>EUDC

La clave del registro EUDC contiene una o más subclaves que contienen valores que definen las fuentes asociadas a los [caracteres definidos por el usuario final (EUDCs)](end-user-defined-characters.md) de una página de códigos determinada. Tiene la siguiente ubicación del registro:

HKEY \_ Current \_ User \\ EUDC

El formato es:

EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName

donde:



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Nombre predefinido que se usa para establecer la fuente predeterminada del sistema. No hay ninguna fuente EUDC predeterminada del sistema, a menos que se especifique explícitamente esta entrada.     |
| TrueTypeFontTypeface     | Nombre definido por el usuario asociado a una fuente TrueType que no es EUDC.                                                                              |
| TrueTypeEUDCFontFileName | Cadena formada por el nombre de archivo de un archivo de fuente EUDC independiente. Este archivo identifica una fuente que se va a asociar a TrueTypeFontTypeface. |



 

En el ejemplo siguiente se muestra la clave EUDC para la página de códigos 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



En el ejemplo siguiente se establece la fuente EUDC predeterminada del sistema como EUDC. ttf y se asocian las fuentes EUDC independientes Mineudc. ttf y Goteudc. ttf con los nombres de fuente MS Mincho y MS Gothic, respectivamente.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Cuando la página de códigos de Windows (sistema ACP) asociada con el idioma para programas no Unicode coincide con la subclave, el subsistema GDI busca los pares de valores de subclave para obtener información sobre el carácter. Primero busca un nombre que coincida con la fuente actual. Si no hay ninguno, examina el valor de SystemDefaultEUDCFont. Si no se define ningún valor, GDI trata el carácter como sin definir.

Tenga en cuenta que el texto no tiene que estar en la página de códigos de Windows. Por ejemplo, supongamos que la página de códigos tiene el identificador 1252, la página de códigos predeterminada de Windows para inglés. Una aplicación pasa a [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)el punto de código Unicode U + E000 y, en el área de uso privado de Unicode (PUA). En este caso, GDI examina los valores del registro en 1252 para obtener la información de fuente de las propiedades de presentación de caracteres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entradas del registro de EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
