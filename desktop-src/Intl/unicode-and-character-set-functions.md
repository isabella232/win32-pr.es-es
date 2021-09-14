---
description: Las funciones siguientes se usan con juegos de caracteres.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Funciones unicode y juego de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255003"
---
# <a name="unicode-and-character-set-functions"></a>Funciones unicode y juego de caracteres

Las funciones siguientes se usan con juegos de caracteres.



| Función                                                       | Descripción                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**GetTextCharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Recupera un identificador de juego de caracteres para la fuente seleccionada actualmente en un contexto de dispositivo especificado.         |
| [**GetTextCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Recupera información sobre el juego de caracteres de la fuente seleccionada actualmente en un contexto de dispositivo especificado. |
| [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | Determina si un carácter especificado es un byte inicial para el valor predeterminado del sistema Windows página de códigos ANSI (CP \_ ACP).           |
| [**IsDBCSLeadByteEx**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Determina si un carácter especificado es potencialmente un byte inicial.                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Determina si es probable que un búfer contenga una forma de texto Unicode.                                                   |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Mapas una cadena de caracteres a una cadena UTF-16 (carácter ancho).                                                          |
| [**TranslateCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Traduce la información del juego de caracteres y establece todos los miembros de una estructura de destino en los valores adecuados.           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Mapas una cadena UTF-16 (carácter ancho) en una nueva cadena de caracteres.                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | No debe usarse.                                                                                                           |
| [**NlsDllCodePageTranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | No debe usarse.                                                                                                           |
| [**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | No utilizar.                                                                                                           |



 

 

 
