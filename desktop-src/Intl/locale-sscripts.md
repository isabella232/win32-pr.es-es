---
description: configuración regional \_ SSCRIPTS
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666592"
---
# <a name="locale_sscripts"></a>configuración regional \_ SSCRIPTS

**Windows Vista y versiones posteriores:** Una cadena que representa una lista de scripts, con la notación de 4 caracteres utilizada en [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Cada nombre de script consta de cuatro caracteres latinos y la lista se organiza en orden alfabético con cada nombre, incluido el último, seguido de un punto y coma.

Se puede llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCTYPE* establecido en la configuración regional \_ SSCRIPTS como parte de una estrategia para mitigar los problemas de seguridad relacionados con los nombres de dominio internacionalizados (IDN). Estos son algunos valores de ejemplo:



| Configuración regional                  | Nombre de idioma o configuración regional | Value                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Spanish (Traditional Sort) - Spain | es-ES                | LATN                                                                                                  |
| Hindi (India)           | hi-IN                | Deva                                                                                                  |
| Japonés (Japón)        | ja-JP                | **Windows 7 y versiones posteriores:** Hani; Hira; Jpan; Kana<br/> **Windows Vista:** Hani; Hira; Kana<br/> |



 

Un valor de script compuesto no incluye el script Latino a menos que sea una parte esencial del sistema de escritura que se usa para la configuración regional concreta. Los caracteres latinos se suelen usar en el contexto de las configuraciones regionales para las que no son nativas, por ejemplo, para un nombre empresarial extranjero. En el ejemplo anterior de Hindi en India, el único valor de script es "Deva" (para "Devanagari"), aunque los caracteres latinos también pueden aparecer en texto Hindi. La función [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) tiene una marca especial para abordar este caso.

 

 




