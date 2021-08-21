---
description: Constantes RETURN de LOCALE \_ \*
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: LOCALE_RETURN* Constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58714897333f69b058588f9050b9bb52ed29c37d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466032"
---
# <a name="locale_return-constants"></a>Constantes RETURN de LOCALE \_ \*

En este tema se definen las constantes RETURN de LOCALE \_ \* usadas por NLS.




| Valor | Significado | 
|-------|---------|
| LOCALE_RETURN_GENITIVE_NAMES | <strong>Windows 7 y versiones posteriores:</strong> Recupere los nombres tivetive de months, que son los nombres que se usan cuando los nombres de mes se combinan con otros elementos. Por ejemplo, en Insulsa, el equivalente de enero se escribe "" cuando el mes se denomina solo. Sin embargo, cuando el nombre del mes se usa en combinación, por ejemplo, en una fecha como el 5 de enero de 2003, se usa la forma tive del nombre. En el ejemplo Desastroso, el nombre del mes tive se muestra como "5 2003". La lista de nombres de mes tive comienza con enero y está delimitada por punto y coma. Si no hay ningún mes 13, use un punto y coma en su lugar al final de la lista.<blockquote>[!Note]<br />Los nombres de mes Tivetive no existen en todos los idiomas.</blockquote><br /><br /> | 
| LOCALE_RETURN_NUMBER | <strong>Windows Me/98, Windows NT 4.0 y versiones posteriores:</strong> Recuperar un número. Esta constante hace <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>que GetLocaleInfo</strong></a> o <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recuperen un valor como un número en lugar de como una cadena. El búfer que recibe el valor debe ser al menos la longitud de un valor DWORD. Esta constante se puede combinar con cualquier otra constante que tenga un nombre que comience por "LOCALE_I". | 




 

 

 




