---
description: Fuentes de varios archivos de recursos
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Fuentes de varios archivos de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/17/2021
ms.locfileid: "104998875"
---
# <a name="fonts-from-multiple-resource-files"></a><span data-ttu-id="d6e33-103">Fuentes de varios archivos de recursos</span><span class="sxs-lookup"><span data-stu-id="d6e33-103">Fonts from Multiple Resource Files</span></span>

<span data-ttu-id="d6e33-104">Normalmente, una fuente se encuentra en un archivo de recursos de fuente único.</span><span class="sxs-lookup"><span data-stu-id="d6e33-104">Typically, a font is contained in a single font resource file.</span></span> <span data-ttu-id="d6e33-105">Sin embargo, la información de algunas fuentes se distribuye entre varios archivos.</span><span class="sxs-lookup"><span data-stu-id="d6e33-105">However, the information for some fonts is spread among several files.</span></span> <span data-ttu-id="d6e33-106">Por ejemplo, escriba 1 varias fuentes maestras requieren dos archivos:</span><span class="sxs-lookup"><span data-stu-id="d6e33-106">For example, Type 1 multiple master fonts require two files:</span></span>

-   <span data-ttu-id="d6e33-107">. PFM para las métricas de fuente</span><span class="sxs-lookup"><span data-stu-id="d6e33-107">.pfm for the font metrics</span></span>
-   <span data-ttu-id="d6e33-108">. PFB para los bits de fuente</span><span class="sxs-lookup"><span data-stu-id="d6e33-108">.pfb for the font bits</span></span>

<span data-ttu-id="d6e33-109">Para agregar una fuente de varios archivos al sistema, use las funciones [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) .</span><span class="sxs-lookup"><span data-stu-id="d6e33-109">To add a font from multiple files to the system, use the [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) or [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) functions.</span></span> <span data-ttu-id="d6e33-110">El parámetro *lpszFilename* de estas funciones debe apuntar a una cadena que contenga los nombres de archivo separados por la barra vertical o la canalización ( \| ).</span><span class="sxs-lookup"><span data-stu-id="d6e33-110">The *lpszFilename* parameter in these functions must point to a string that contains the file names separated by the vertical bar or pipe ( \| ).</span></span> <span data-ttu-id="d6e33-111">Por ejemplo, para especificar abcxxxxx. PFM y abcxxxxx. PFB para una fuente de tipo 1, use la cadena "abcxxxxx. PFM \| abcxxxxx. PFB".</span><span class="sxs-lookup"><span data-stu-id="d6e33-111">For example, to specify abcxxxxx.pfm and abcxxxxx.pfb for a Type 1 font, use the string "abcxxxxx.pfm \| abcxxxxx.pfb."</span></span>

<span data-ttu-id="d6e33-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) difiere de [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) en que la aplicación que llama a **AddFontResourceEx** puede especificar la fuente como privada para sí misma o no Enumerable.</span><span class="sxs-lookup"><span data-stu-id="d6e33-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differs from [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in that the application calling **AddFontResourceEx** can specify the font as private to itself or non-enumerable.</span></span>

<span data-ttu-id="d6e33-113">Para agregar una fuente de una imagen de memoria, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="d6e33-113">To add a font from a memory image, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span></span> <span data-ttu-id="d6e33-114">Esto permite que una aplicación use una fuente que está incrustada en un documento o una página web.</span><span class="sxs-lookup"><span data-stu-id="d6e33-114">This allows an application to use a font that is embedded in a document or a webpage.</span></span>

<span data-ttu-id="d6e33-115">Para quitar una fuente que proviene de varios archivos de recursos, llame a [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) o [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), en función de la función utilizada para agregar la fuente.</span><span class="sxs-lookup"><span data-stu-id="d6e33-115">To remove a font that came from multiple resource files, call [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) or [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), depending on the function used to add the font.</span></span> <span data-ttu-id="d6e33-116">Debe especificar las mismas marcas que se usaron para agregar la fuente.</span><span class="sxs-lookup"><span data-stu-id="d6e33-116">You must specify the same flags that were used to add the font.</span></span> <span data-ttu-id="d6e33-117">Para quitar una fuente que se ha agregado a partir de una imagen de memoria, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="d6e33-117">To remove a font that was added from a memory image, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span></span>

<span data-ttu-id="d6e33-118">El uso de una fuente que proviene de varios archivos de recursos de fuente es idéntico al uso de una fuente de un archivo de recursos único.</span><span class="sxs-lookup"><span data-stu-id="d6e33-118">Using a font that comes from multiple font-resource files is identical to using a font from a single resource file.</span></span>

 

 
