---
description: Las aplicaciones escriben caracteres finales definidos por el usuario (EUDCs) y caracteres de área de uso privado (PUA) en la pantalla o la impresora de la misma forma que escriben otros caracteres, mediante funciones de salida como TextOut y ExtTextOut.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Escribir, asignar y ordenar caracteres EUDC y PUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c34264d956bb6a87407e249f68b2bc03fb2c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275440"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Escribir, asignar y ordenar caracteres EUDC y PUA

Las aplicaciones escriben caracteres finales definidos por el usuario (EUDCs) y caracteres de área de uso privado (PUA) en la pantalla o la impresora de la misma forma que escriben otros caracteres, mediante funciones de salida como [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) y [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta). Estas funciones recuperan automáticamente información de caracteres de las fuentes de caracteres EUDC o PUA si se habilita EUDC. Para obtener más información, vea [caracteres de \_ área de uso privados y definidos por el usuario final](end-user-defined-characters.md).

Al escribir caracteres EUDCs o PUA, el funcionamiento de la función de salida de texto depende de la fuente seleccionada actualmente. Si la fuente seleccionada es una fuente de caracteres EUDC o PUA integrada, la función recupera información de caracteres de esa fuente. Si la fuente seleccionada es una fuente TrueType de [juego de caracteres de doble byte](double-byte-character-sets.md) (DBCS) que tiene asociada una fuente EUDC independiente, la función recupera información de la fuente EUDC especificada. Del mismo modo, si la fuente seleccionada es una fuente TrueType [Unicode](unicode.md) que tiene una fuente de caracteres PUA independiente asociada, la función recupera información de la fuente de caracteres PUA. Si la fuente seleccionada no tiene una fuente de caracteres EUDC o PUA asociada, la función recupera información de la fuente EUDC predeterminada del sistema. Si el carácter no está en la fuente EUDC predeterminada del sistema o no hay ninguna fuente EUDC predeterminada del sistema, la función escribe el carácter predeterminado definido por la fuente seleccionada.

Las aplicaciones pueden asignar EUDCs a y desde Unicode mediante las funciones [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) . La función **MultiByteToWideChar** asigna la mayoría de los EUDCs a los caracteres de PUA de Unicode. Sin embargo, para admitir determinados estándares nacionales o regionales, algunos EUDCs pueden asignarse a puntos de código Unicode no PUA. La función **WideCharToMultiByte** asigna un carácter de PUA a su homólogo de EUDC, si existe tal asignación, y si el punto de código no tiene una asignación no PUA válida en Unicode. No todas las páginas de códigos tienen un intervalo EUDC. La página de códigos especificada en una llamada a **WideCharToMultiByte** debe contener un intervalo de código EUDC para que se produzca la asignación al intervalo EUDC. Si la página de códigos no contiene un intervalo de código EUDC, la función recupera el carácter predeterminado para los caracteres de la PUA Unicode.

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) no garantizan la asignación de ida y vuelta. En otras palabras, es posible empezar con una cadena multibyte determinada que contenga EUDCs, asignar la cadena a Unicode con **MultiByteToWideChar** y asignarla de nuevo al DBCS original con **WideCharToMultiByte** y acabar con un resultado que no sea idéntico a la cadena original. Las aplicaciones que dependen de la asignación de EUDCs a Unicode deben asegurarse de que todos los caracteres necesarios puedan realizarse entre el área de EUDC de la página de códigos adecuada y el PUA de Unicode.

Las aplicaciones no deben intentar asignar EUDCs de una página de códigos a otra. Si una aplicación se inicia con un EUDC de una página de códigos, lo asigna a Unicode con [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)y se asigna a un DBCS diferente con [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte), no hay ninguna garantía sobre los resultados. El carácter original podría estar asignado a un EUDC diferente en la página de códigos de destino, o bien se podría asignar como un carácter no definido. Del mismo modo, la asignación de una cadena Unicode a una página de códigos que tiene un intervalo de EUDC puede tener resultados imprevistos. Si la cadena Unicode contiene un punto de código PUA, es posible que el punto de código se asigne a un EUDC que no represente el mismo carácter.

Las aplicaciones pueden comparar cadenas DBCS que contienen EUDCs con la versión ANSI de la función [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) . La función asigna de forma eficaz los caracteres a Unicode antes de comparar los valores de caracteres. Las aplicaciones pueden crear una clave de ordenación para la cadena mediante la versión ANSI de la función [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) y el valor LCMAP de \_ SORTKEY. Esta función asigna realmente caracteres a Unicode primero. Todos los caracteres de PUA se ordenan después de todos los demás caracteres Unicode. Dentro del área, los caracteres se ordenan en orden numérico. Si una aplicación intenta recuperar información de CTYPE para un EUDC mediante la función [GetStringTypeA](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) , la función recupera **null** para cada carácter.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
