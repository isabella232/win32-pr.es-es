---
description: El método GetDVDTextLanguageLCID recupera el identificador de configuración regional (LCID) para el bloque de cadena de texto especificado.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Método GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536627"
---
# <a name="getdvdtextlanguagelcid-method"></a><span data-ttu-id="4549b-103">Método GetDVDTextLanguageLCID</span><span class="sxs-lookup"><span data-stu-id="4549b-103">GetDVDTextLanguageLCID Method</span></span>

> [!Note]  
> <span data-ttu-id="4549b-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4549b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4549b-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="4549b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4549b-106">El `GetDVDTextLanguageLCID` método recupera el identificador de configuración regional (LCID) para el bloque de cadena de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="4549b-106">The `GetDVDTextLanguageLCID` method retrieves the locale identifier (LCID) for the specified text string block.</span></span>

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="4549b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4549b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4549b-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="4549b-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="4549b-109">Especifica el bloque de idioma de texto del disco como un entero.</span><span class="sxs-lookup"><span data-stu-id="4549b-109">Specifies the text language block on the disc as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4549b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4549b-110">Return Value</span></span>

<span data-ttu-id="4549b-111">Devuelve un valor de LCID que contiene información que especifica el idioma en el que se escriben las cadenas.</span><span class="sxs-lookup"><span data-stu-id="4549b-111">Returns an LCID value that contains information specifying the language the strings are written in.</span></span>

## <a name="remarks"></a><span data-ttu-id="4549b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4549b-112">Remarks</span></span>

<span data-ttu-id="4549b-113">Las cadenas de texto complementario se almacenan en bloques contiguos en el disco. Cada lenguaje tiene un bloque de cadenas.</span><span class="sxs-lookup"><span data-stu-id="4549b-113">Supplemental text strings are stored in contiguous blocks on the disc. Each language has one block of strings.</span></span> <span data-ttu-id="4549b-114">Una aplicación especifica estos bloques por un índice, que debe ser menor que el valor devuelto por [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="4549b-114">An application specifies these blocks by an index, which must be less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4549b-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="4549b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4549b-116">Objeto MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="4549b-116">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> <dt>

[<span data-ttu-id="4549b-117">**GetLangFromLangID**</span><span class="sxs-lookup"><span data-stu-id="4549b-117">**GetLangFromLangID**</span></span>](getlangfromlangid-method.md)
</dt> </dl>

 

 



