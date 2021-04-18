---
description: De forma predeterminada, el motor y el catálogo de Windows Search no distinguen los signos diacríticos, que son signos de acento agregados a las letras para modificar el significado o la Pronunciación de una palabra.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Sensibilidad diacrítica en las búsquedas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715009"
---
# <a name="diacritic-sensitivity-in-searches"></a><span data-ttu-id="902b0-103">Sensibilidad diacrítica en las búsquedas</span><span class="sxs-lookup"><span data-stu-id="902b0-103">Diacritic Sensitivity in Searches</span></span>

<span data-ttu-id="902b0-104">De forma predeterminada, el motor y el catálogo de Windows Search no distinguen los signos diacríticos, que son signos de acento agregados a las letras para modificar el significado o la Pronunciación de una palabra.</span><span class="sxs-lookup"><span data-stu-id="902b0-104">By default, the Windows Search engine and catalog are insensitive to diacritics, which are accent marks added to letters to alter a word's meaning or pronunciation.</span></span> <span data-ttu-id="902b0-105">Sin embargo, Windows Search permite cambiar esto para el catálogo mediante el [Administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) para establecer la sensibilidad diacrítica.</span><span class="sxs-lookup"><span data-stu-id="902b0-105">However, Windows Search enables you to change this for your catalog using the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to set diacritic sensitivity.</span></span> <span data-ttu-id="902b0-106">Por ejemplo, con la distinción de diacríticos establecida en **false**, el catálogo trataría "resume" y "resumé" como si fueran la misma palabra.</span><span class="sxs-lookup"><span data-stu-id="902b0-106">For example, with diacritic sensitivity set to **FALSE**, the catalog would treat "resume" and "resumé" as if they were the same word.</span></span>

<span data-ttu-id="902b0-107">En el nivel de consulta, los términos de consulta con signos diacríticos en las cláusulas FREETEXT y Contains se pasan al motor y, a continuación, se normalizan (como serían en el tiempo de índice) para buscar coincidencias.</span><span class="sxs-lookup"><span data-stu-id="902b0-107">At the query layer, query terms with diacritics in FREETEXT and CONTAINS clauses are passed through to the engine and are then normalized (as they would be at index time) for matching.</span></span> <span data-ttu-id="902b0-108">La coincidencia con el catálogo siempre distingue los signos diacríticos.</span><span class="sxs-lookup"><span data-stu-id="902b0-108">Matching against the catalog is always diacritic sensitive.</span></span>

> [!Note]  
> <span data-ttu-id="902b0-109">Este no es el caso de los intervalos de caracteres 0x2e81-F8FF y 0x1100-0x11ff.</span><span class="sxs-lookup"><span data-stu-id="902b0-109">This is not the case for the character ranges 0x2e81-f8ff and 0x1100-0x11ff.</span></span>

 

 

 



