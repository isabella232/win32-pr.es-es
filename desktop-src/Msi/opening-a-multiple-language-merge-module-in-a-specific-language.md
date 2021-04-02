---
description: Al combinar un módulo en una base de datos de instalación, hay dos lenguajes importantes.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Abrir un módulo de combinación de Multiple-Language en un idioma específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082258"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a><span data-ttu-id="47bfd-103">Abrir un módulo de combinación de Multiple-Language en un idioma específico</span><span class="sxs-lookup"><span data-stu-id="47bfd-103">Opening a Multiple-Language Merge Module in a Specific Language</span></span>

<span data-ttu-id="47bfd-104">Al combinar un módulo en una base de datos de instalación, hay dos lenguajes importantes.</span><span class="sxs-lookup"><span data-stu-id="47bfd-104">When merging a module into an installation database, there are two important languages.</span></span> <span data-ttu-id="47bfd-105">El primero es el idioma del paquete de instalación de destino especificado por [**ProductLanguage**](productlanguage.md) en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="47bfd-105">The first is the language of the target installation package specified by [**ProductLanguage**](productlanguage.md) in the [Property Table](property-table.md).</span></span> <span data-ttu-id="47bfd-106">El segundo es el idioma del módulo de combinación que aparece en la columna Language de la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="47bfd-106">The second is the language of the merge module that appears in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="47bfd-107">El idioma del paquete de instalación se puede pasar al módulo mediante la herramienta de combinación cuando se abre el paquete para una combinación.</span><span class="sxs-lookup"><span data-stu-id="47bfd-107">The language of the installation package can be passed to the module by the merge tool when the package is opened for a merge.</span></span> <span data-ttu-id="47bfd-108">Sin embargo, a veces puede ser necesario omitir el idioma del destino y solicitar que el módulo se abra en otro idioma, por ejemplo, un paquete en inglés que instale los recursos en inglés y en alemán desde el módulo.</span><span class="sxs-lookup"><span data-stu-id="47bfd-108">However, sometimes it may be necessary to disregard the language of the target, and request that the module be opened in another language, for example, an English package installing both the English and German resources from the module.</span></span>

<span data-ttu-id="47bfd-109">Al abrir un módulo con una solicitud de lenguaje, la herramienta de combinación comprueba el idioma solicitado con los idiomas especificados en la columna idioma de la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="47bfd-109">When opening a module with a language request, the merge tool checks the requested language against the languages that are specified in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="47bfd-110">El siguiente proceso se utiliza para determinar el idioma que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="47bfd-110">The following process is used to determine which language to use.</span></span>

<span data-ttu-id="47bfd-111">**Para determinar el idioma que se va a usar**</span><span class="sxs-lookup"><span data-stu-id="47bfd-111">**To determine which language to use**</span></span>

1.  <span data-ttu-id="47bfd-112">Si el idioma de la [tabla ModuleSignature](modulesignature-table.md) es igual o más general que el idioma solicitado, se abre el módulo.</span><span class="sxs-lookup"><span data-stu-id="47bfd-112">If the language in the [ModuleSignature Table](modulesignature-table.md) is equal or more general than the requested language, the module opens.</span></span>
2.  <span data-ttu-id="47bfd-113">Si el módulo admite el lenguaje exacto solicitado, se usa ese idioma.</span><span class="sxs-lookup"><span data-stu-id="47bfd-113">If the module supports the exact language requested, that language is used.</span></span>
3.  <span data-ttu-id="47bfd-114">Si el módulo admite el grupo de idiomas del idioma solicitado, se usa el grupo de idioma; por ejemplo, Active 9 Si se solicitó 1033 pero no se encontró en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="47bfd-114">If the module supports the language group of the language requested that language group is used, for example, check 9 if 1033 was requested but not found in step 2.</span></span>
4.  <span data-ttu-id="47bfd-115">Compruebe si hay una transformación de idioma que cambie el módulo a neutro.</span><span class="sxs-lookup"><span data-stu-id="47bfd-115">Check if there is a language transform that changes the module to neutral.</span></span>
5.  <span data-ttu-id="47bfd-116">Si ninguno de los pasos anteriores se realiza correctamente, el módulo no admite el idioma solicitado y se produce un error en la combinación.</span><span class="sxs-lookup"><span data-stu-id="47bfd-116">If none of the previous steps succeed, the module does not support the requested language and the merge fails.</span></span>

 

 



