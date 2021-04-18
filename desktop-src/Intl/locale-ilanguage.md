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
# <a name="locale_ilanguage"></a><span data-ttu-id="35980-103">configuración regional \_ ILANGUAGE</span><span class="sxs-lookup"><span data-stu-id="35980-103">LOCALE\_ILANGUAGE</span></span>

<span data-ttu-id="35980-104">[Identificador de idioma](language-identifiers.md) con un valor hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="35980-104">[Language identifier](language-identifiers.md) with a hexadecimal value.</span></span> <span data-ttu-id="35980-105">Por ejemplo, Inglés (Estados Unidos) tiene el valor 0409, que indica 0x0409 hexadecimal, y es equivalente a 1033 decimal.</span><span class="sxs-lookup"><span data-stu-id="35980-105">For example, English (United States) has the value 0409, which indicates 0x0409 hexadecimal, and is equivalent to 1033 decimal.</span></span> <span data-ttu-id="35980-106">El número máximo de caracteres permitido para esta cadena es cinco, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="35980-106">The maximum number of characters allowed for this string is five, including a terminating null character.</span></span>

<span data-ttu-id="35980-107">**Windows Vista y versiones posteriores:** El uso de esta constante puede hacer que [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) devuelva un identificador de configuración regional no válido.</span><span class="sxs-lookup"><span data-stu-id="35980-107">**Windows Vista and later:** Use of this constant can cause [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) to return an invalid locale identifier.</span></span> <span data-ttu-id="35980-108">La aplicación debe usar la constante [ \_ SNAME de configuración regional](locale-sname.md) al llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="35980-108">Your application should use the [LOCALE\_SNAME](locale-sname.md) constant when calling this function.</span></span>

 

 



