---
description: Configuración regional \_ S2359 y configuración regional \_ SPM
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 y LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688058"
---
# <a name="locale_s2359-and-locale_spm"></a>Configuración regional \_ S2359 y configuración regional \_ SPM

Cadena para el designador PM (segundo 12 horas del día). El número máximo de caracteres permitido para esta cadena es diferente para las distintas versiones de Windows.

**Windows XP:** Trece incluir un carácter nulo de terminación para [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Quince incluye un carácter nulo de terminación para [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0 y windows 2000:** Nueve incluido un carácter nulo de terminación.

**Windows Server 2003 y versiones posteriores:** Quince incluye un carácter nulo de terminación.

Windows 10 agregó el valor **configuración regional \_ SPM** como sinónimo más legible para la **configuración regional \_ S2359**.

 

 



