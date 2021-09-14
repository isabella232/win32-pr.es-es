---
description: SSCRIPT \_ DE CONFIGURACIÓN REGIONAL
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274268"
---
# <a name="locale_sscripts"></a>SSCRIPT \_ DE CONFIGURACIÓN REGIONAL

**Windows Vista y versiones posteriores:** Cadena que representa una lista de scripts, utilizando la notación de 4 caracteres usada en [ISO 15924.](https://www.unicode.org/iso15924/iso15924-codes.html) Cada nombre de script consta de cuatro caracteres latinos y la lista se organiza en orden alfabético con cada nombre, incluido el último, seguido de un punto y coma.

Se puede llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* establecido en LOCALE SSCRIPTS como parte de una estrategia para mitigar los problemas de seguridad relacionados con los nombres de dominio \_ internacionalizados (IDN). Estos son algunos valores de ejemplo:



| Configuración regional                  | Nombre de configuración regional o idioma | Value                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Spanish (Traditional Sort) - Spain | es-ES                | Latn;                                                                                                  |
| Hindi (India)           | hi-IN                | Deva;                                                                                                  |
| Japonés (Japón)        | ja-JP                | **Windows 7 y versiones posteriores:** Hani; Hira; Jpan; Kana;<br/> **Windows Vista:** Hani; Hira; Kana;<br/> |



 

Un valor de script compuesto no incluye el script latino a menos que sea una parte esencial del sistema de escritura utilizado para la configuración regional concreta. Los caracteres latinos se suelen usar en el contexto de configuraciones regionales para las que no son nativos, por ejemplo, para un nombre de negocio externo. En el ejemplo anterior de Hindi en la India, el único valor de script es "Deva" (para "Devachari"), aunque los caracteres latinos también pueden aparecer en texto hindi. La [función VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) tiene una marca especial para abordar este caso.

 

 




