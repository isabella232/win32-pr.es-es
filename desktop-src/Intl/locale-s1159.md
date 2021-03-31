---
description: Configuración regional \_ S1159 y Sam de configuración regional \_
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 y LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911670"
---
# <a name="locale_s1159-and-locale_sam"></a>Configuración regional \_ S1159 y Sam de configuración regional \_

Cadena para el designador AM (primeras 12 horas del día). El número máximo de caracteres permitido para esta cadena, incluido un carácter nulo de terminación, es diferente para las distintas versiones de Windows.

**Windows XP:** Trece incluir un carácter nulo de terminación para [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Quince incluye un carácter nulo de terminación para [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0 y windows 2000:** Nueve incluido un carácter nulo de terminación.

**Windows Server 2003 y versiones posteriores:** Quince incluye un carácter nulo de terminación.

Windows 10 agregó el valor **\_ SAM de configuración regional** como sinónimo más legible para la **configuración regional \_ S1159**.

 

 



