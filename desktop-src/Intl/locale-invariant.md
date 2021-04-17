---
description: configuración regional \_ INvariable
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652415"
---
# <a name="locale_invariant"></a><span data-ttu-id="85207-103">configuración regional \_ INvariable</span><span class="sxs-lookup"><span data-stu-id="85207-103">LOCALE\_INVARIANT</span></span>

<span data-ttu-id="85207-104">**Windows XP:** Configuración regional que se usa para las funciones de nivel de sistema operativo que requieren resultados coherentes y independientes de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="85207-104">**Windows XP:** The locale used for operating system-level functions that require consistent and locale-independent results.</span></span> <span data-ttu-id="85207-105">Por ejemplo, la configuración regional invariable se usa cuando una aplicación compara cadenas de caracteres mediante la función [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y espera un resultado coherente independientemente de la configuración regional del usuario.</span><span class="sxs-lookup"><span data-stu-id="85207-105">For example, the invariant locale is used when an application compares character strings using the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) function and expects a consistent result regardless of the user locale.</span></span> <span data-ttu-id="85207-106">La configuración regional de todos los idiomas es similar a la de inglés (Estados Unidos), pero no debe usarse para Mostrar datos con formato.</span><span class="sxs-lookup"><span data-stu-id="85207-106">The settings of the invariant locale are similar to those for English (United States) but should not be used to display formatted data.</span></span> <span data-ttu-id="85207-107">Normalmente, una aplicación no usa la configuración regional \_ invariable, ya que espera que los resultados de una acción dependan de las reglas que rigen cada configuración regional individual.</span><span class="sxs-lookup"><span data-stu-id="85207-107">Typically, an application does not use LOCALE\_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.</span></span> <span data-ttu-id="85207-108">El valor de configuración regional \_ INVARIABLE es 0x007f.</span><span class="sxs-lookup"><span data-stu-id="85207-108">The value of LOCALE\_INVARIANT IS 0x007f.</span></span>

 

 
