---
description: SSCRIPT \_ DE CONFIGURACIÓN REGIONAL
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aede4d6d1843fd32bdd17ae3a275a364c3a2d4f0bd282302f49d7b4a3b0dd1ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105855"
---
# <a name="locale_sscripts"></a>SSCRIPT \_ DE CONFIGURACIÓN REGIONAL

**Windows Vista y versiones posteriores:** Cadena que representa una lista de scripts, utilizando la notación de 4 caracteres usada en [ISO 15924.](https://www.unicode.org/iso15924/iso15924-codes.html) Cada nombre de script consta de cuatro caracteres latinos y la lista se organiza en orden alfabético con cada nombre, incluido el último, seguido de un punto y coma.

Se puede llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* establecido en LOCALE SSCRIPTS como parte de una estrategia para mitigar los problemas de seguridad relacionados con los nombres de dominio \_ internacionalizados (IDN). Estos son algunos valores de ejemplo:



| Configuración regional                  | Configuración regional/nombre de idioma | Value                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Spanish (Traditional Sort) - Spain | es-ES                | Latn;                                                                                                  |
| Hindi (India)           | hi-IN                | Deva;                                                                                                  |
| Japonés (Japón)        | ja-JP                | **Windows 7 y versiones posteriores:** Hani; Hira; Jpan; Kana;<br/> **Windows Vista:** Hani; Hira; Kana;<br/> |



 

Un valor de script compuesto no incluye el script latino a menos que sea una parte esencial del sistema de escritura utilizado para la configuración regional determinada. Los caracteres latinos se usan a menudo en el contexto de configuraciones regionales para las que no son nativos, por ejemplo, para un nombre empresarial externo. En el ejemplo anterior de Hindi en la India, el único valor de script es "Deva" (para "Deva bytei"), aunque los caracteres latinos también pueden aparecer en el texto de Hindi. La [función VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) tiene una marca especial para resolver este caso.

 

 




