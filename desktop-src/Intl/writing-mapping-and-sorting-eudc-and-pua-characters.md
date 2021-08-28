---
description: Las aplicaciones escriben caracteres definidos por el usuario final (EUDC) y caracteres de área de uso privado (PUA) en la pantalla o impresora igual que escriben otros caracteres, mediante funciones de salida como TextOut y ExtTextOut.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Escribir, asignar y ordenar caracteres EUDC y PUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ab43eb54055b97fe1823ad99467a4cd0b12a0a5fb971d52d225631cfd37ffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102085"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Escribir, asignar y ordenar caracteres EUDC y PUA

Las aplicaciones escriben caracteres definidos por el usuario final (EUDC) y caracteres de área de uso privado (PUA) en la pantalla o impresora igual que escriben otros caracteres, mediante funciones de salida como [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) y [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta). Estas funciones recuperan automáticamente información de caracteres de fuentes de caracteres EUDC o PUA si EUDC está habilitado. Para obtener más información, [vea End-User \_ Defined and Private Use Area Characters](end-user-defined-characters.md).

Al escribir caracteres EUDC o PUA, el funcionamiento de la función de salida de texto depende de la fuente seleccionada actualmente. Si la fuente seleccionada es una fuente de caracteres EUDC o PUA integrada, la función recupera información de caracteres de esa fuente. Si la fuente seleccionada es una fuente TrueType de juego de caracteres de doble [byte](double-byte-character-sets.md) (DBCS) que tiene una fuente EUDC independiente asociada, la función recupera información de la fuente EUDC especificada. De forma similar, si la fuente seleccionada es una fuente [TrueType Unicode](unicode.md) que tiene una fuente de caracteres PUA independiente asociada, la función recupera información de la fuente de caracteres PUA. Si la fuente seleccionada no tiene una fuente de caracteres EUDC o PUA asociada, la función recupera información de la fuente EUDC predeterminada del sistema. Si el carácter no está en la fuente EUDC predeterminada del sistema o no hay ninguna fuente EUDC predeterminada del sistema, la función escribe el carácter predeterminado definido por la fuente seleccionada.

Las aplicaciones pueden asignar EUDC a y desde Unicode mediante las funciones [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte.**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) La **función MultiByteToWideChar** asigna la mayoría de los EUDC a caracteres de la PUA Unicode. Sin embargo, para admitir determinados estándares nacionales o regionales, algunos EUDC se pueden asignar a puntos de código Unicode que no sean PUA. La **función WideCharToMultiByte** asigna un carácter de la PUA a su homólogo de EUDC, si existe dicha asignación y si el punto de código no tiene una asignación no PUA válida en Unicode. No todas las páginas de códigos tienen un intervalo EUDC. La página de códigos especificada en una llamada a **WideCharToMultiByte** debe contener un intervalo de código EUDC para que se produzca la asignación al intervalo EUDC. Si la página de códigos no contiene un intervalo de códigos EUDC, la función recupera el carácter predeterminado para los caracteres de la PUA Unicode.

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) no garantizan la asignación de ida y vuelta. En otras palabras, es posible empezar con una cadena multibyte determinada que contenga EUDC, asignar la cadena a Unicode con **MultiByteToWideChar** y asignarla de nuevo al DBCS original con **WideCharToMultiByte** y terminar con un resultado que no es idéntico a la cadena original. Las aplicaciones que dependen de la asignación de EUDC a Unicode deben asegurarse de que todos los caracteres necesarios pueden realizar un recorrido de ida y vuelta entre el área EUDC de la página de códigos adecuada y la PUA Unicode.

Las aplicaciones no deben intentar asignar EUDC de una página de códigos a otra. Si una aplicación comienza con un EUDC desde una página de códigos, lo asigna a Unicode con [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)y se asigna a un DBCS diferente con [**WideCharToMultiByte,**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)no hay ninguna garantía sobre los resultados. El carácter original podría asignarse a un EUDC diferente en la página de códigos de destino o podría asignarse como un carácter no definido. De forma similar, la asignación de una cadena Unicode a una página de códigos que tiene un intervalo EUDC puede tener resultados no deseados. Si la cadena Unicode contiene un punto de código PUA, es posible que el punto de código se asigne a un EUDC que no represente el mismo carácter.

Las aplicaciones pueden comparar cadenas DBCS que contienen EUDC mediante la versión ANSI de la [función CompareString.](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) La función asigna eficazmente los caracteres a Unicode antes de comparar los valores de caracteres. Las aplicaciones pueden crear una clave de ordenación para la cadena mediante la versión ANSI de la función [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) y el valor \_ SORTKEY de LCMAP. Esta función asigna primero caracteres a Unicode de forma eficaz. Todos los caracteres de pua se ordenan después de todos los demás caracteres Unicode. Dentro del área, los caracteres se ordenan en orden numérico. Si una aplicación intenta recuperar información de CTYPE para un EUDC mediante la función [GetStringTypeA,](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) la función recupera **NULL** para cada carácter.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
