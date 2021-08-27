---
description: '\_ILANGUAGE DE CONFIGURACIÓN REGIONAL'
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3159fe26ce1af7291c5990a07297e7513144b5187b55c00086bf46e452ef188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106655"
---
# <a name="locale_ilanguage"></a>\_ILANGUAGE DE CONFIGURACIÓN REGIONAL

[Identificador de idioma](language-identifiers.md) con un valor hexadecimal. Por ejemplo, el inglés (Estados Unidos) tiene el valor 0409, que indica 0x0409 hexadecimal, y es equivalente a 1033 decimal. El número máximo de caracteres permitido para esta cadena es cinco, incluido un carácter nulo de terminación.

**Windows Vista y versiones posteriores:** El uso de esta constante puede hacer [**que GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) devuelva un identificador de configuración regional no válido. La aplicación debe usar la [constante \_ LOCALE SNAME](locale-sname.md) al llamar a esta función.

 

 



