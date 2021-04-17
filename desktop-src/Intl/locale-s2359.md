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
# <a name="locale_s2359-and-locale_spm"></a><span data-ttu-id="0525d-103">Configuración regional \_ S2359 y configuración regional \_ SPM</span><span class="sxs-lookup"><span data-stu-id="0525d-103">LOCALE\_S2359 and LOCALE\_SPM</span></span>

<span data-ttu-id="0525d-104">Cadena para el designador PM (segundo 12 horas del día).</span><span class="sxs-lookup"><span data-stu-id="0525d-104">String for the PM designator (second 12 hours of the day).</span></span> <span data-ttu-id="0525d-105">El número máximo de caracteres permitido para esta cadena es diferente para las distintas versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="0525d-105">The maximum number of characters allowed for this string is different for different releases of Windows.</span></span>

<span data-ttu-id="0525d-106">**Windows XP:** Trece incluir un carácter nulo de terminación para [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="0525d-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="0525d-107">Quince incluye un carácter nulo de terminación para [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="0525d-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="0525d-108">**Windows Me/98/95, Windows NT 4,0 y windows 2000:** Nueve incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="0525d-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="0525d-109">**Windows Server 2003 y versiones posteriores:** Quince incluye un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="0525d-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="0525d-110">Windows 10 agregó el valor **configuración regional \_ SPM** como sinónimo más legible para la **configuración regional \_ S2359**.</span><span class="sxs-lookup"><span data-stu-id="0525d-110">Windows 10 added the value **LOCALE\_SPM** as a more readable synonym for **LOCALE\_S2359**.</span></span>

 

 



