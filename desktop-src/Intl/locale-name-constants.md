---
description: Constantes de nombre de configuración regional \_ \*
ms.assetid: 63e2e368-af2f-4af0-bbea-2b27d1939394
title: Constantes de LOCALE_NAME *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aaaba8665c729a047be6a7e3a3d6b3239c81af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687938"
---
# <a name="locale_name-constants"></a><span data-ttu-id="68837-103">Constantes de nombre de configuración regional \_ \*</span><span class="sxs-lookup"><span data-stu-id="68837-103">LOCALE\_NAME\* Constants</span></span>

<span data-ttu-id="68837-104">En este tema se definen las constantes de nombre de configuración regional \_ \* utilizadas por NLS.</span><span class="sxs-lookup"><span data-stu-id="68837-104">This topic defines the LOCALE\_NAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68837-105">Value</span><span class="sxs-lookup"><span data-stu-id="68837-105">Value</span></span></th>
<th><span data-ttu-id="68837-106">Significado</span><span class="sxs-lookup"><span data-stu-id="68837-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68837-107">LOCALE_NAME_INVARIANT</span><span class="sxs-lookup"><span data-stu-id="68837-107">LOCALE_NAME_INVARIANT</span></span></td>
<td><span data-ttu-id="68837-108">Nombre de una configuración regional invariable que proporciona datos de calendario y configuración regional estables.</span><span class="sxs-lookup"><span data-stu-id="68837-108">Name of an invariant locale that provides stable locale and calendar data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68837-109">LOCALE_NAME_MAX_LENGTH</span><span class="sxs-lookup"><span data-stu-id="68837-109">LOCALE_NAME_MAX_LENGTH</span></span></td>
<td><span data-ttu-id="68837-110">Longitud máxima de un nombre de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="68837-110">Maximum length of a locale name.</span></span> <span data-ttu-id="68837-111">El número máximo de caracteres permitido para esta cadena es 85, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="68837-111">The maximum number of characters allowed for this string is 85, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="68837-112">La aplicación debe usar la constante para la longitud máxima de nombre de configuración regional, en lugar de codificar de forma rígida el valor &quot; 85 &quot; .</span><span class="sxs-lookup"><span data-stu-id="68837-112">Your application must use the constant for the maximum locale name length, instead of hard-coding the value &quot;85&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68837-113">LOCALE_NAME_SYSTEM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="68837-113">LOCALE_NAME_SYSTEM_DEFAULT</span></span></td>
<td><span data-ttu-id="68837-114">Nombre de la configuración regional actual del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68837-114">Name of the current operating system locale.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68837-115">LOCALE_NAME_USER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="68837-115">LOCALE_NAME_USER_DEFAULT</span></span></td>
<td><span data-ttu-id="68837-116">Nombre de la configuración regional del usuario actual, que coincide con el conjunto de preferencias de la parte configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="68837-116">Name of the current user locale, matching the preference set in the regional and language options portion of Control Panel.</span></span> <span data-ttu-id="68837-117">Esta configuración regional puede ser diferente de la configuración regional del idioma de la interfaz de usuario actual.</span><span class="sxs-lookup"><span data-stu-id="68837-117">This locale can be different from the locale for the current user interface language.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




