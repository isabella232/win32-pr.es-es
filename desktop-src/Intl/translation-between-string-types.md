---
description: Las funciones enumeradas en la tabla siguiente traducen cadenas de caracteres de un tipo de cadena a otro.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Traducción entre tipos de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171861"
---
# <a name="translation-between-string-types"></a>Traducción entre tipos de cadena

Las funciones enumeradas en la tabla siguiente traducen cadenas de caracteres de un tipo de cadena a otro.



| Función                                           | Descripción                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Convierte una cadena de caracteres en otra.             |
| [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Mapas una cadena de caracteres por configuración regional.                      |
| [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Convierte un código de clave virtual en un carácter Unicode. |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Mapas una cadena multibyte en una cadena Unicode.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Mapas una cadena Unicode a una cadena multibyte.            |



 

Las [**funciones WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) y [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) son especialmente útiles para las aplicaciones que admiten varios tipos de cadena. ANSI C también define las funciones de conversión **wcstombs** y **mbstowcs,** pero solo pueden convertir a y desde el juego de caracteres admitido por la biblioteca estándar de C.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
