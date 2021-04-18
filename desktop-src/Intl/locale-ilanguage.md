---
description: configuración regional \_ ILANGUAGE
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686494"
---
# <a name="locale_ilanguage"></a>configuración regional \_ ILANGUAGE

[Identificador de idioma](language-identifiers.md) con un valor hexadecimal. Por ejemplo, Inglés (Estados Unidos) tiene el valor 0409, que indica 0x0409 hexadecimal, y es equivalente a 1033 decimal. El número máximo de caracteres permitido para esta cadena es cinco, incluido un carácter nulo de terminación.

**Windows Vista y versiones posteriores:** El uso de esta constante puede hacer que [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) devuelva un identificador de configuración regional no válido. La aplicación debe usar la constante [ \_ SNAME de configuración regional](locale-sname.md) al llamar a esta función.

 

 



