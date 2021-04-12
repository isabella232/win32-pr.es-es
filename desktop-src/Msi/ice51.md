---
description: ICE51 comprueba que se ha proporcionado un título para los archivos de recursos de fuentes.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278159"
---
# <a name="ice51"></a><span data-ttu-id="a607a-103">ICE51</span><span class="sxs-lookup"><span data-stu-id="a607a-103">ICE51</span></span>

<span data-ttu-id="a607a-104">ICE51 comprueba que se ha proporcionado un título para los archivos de recursos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="a607a-104">ICE51 checks that a title has been provided for font resource files.</span></span>

<span data-ttu-id="a607a-105">Debe proporcionar un título para un recurso de fuente que no tenga un nombre incrustado.</span><span class="sxs-lookup"><span data-stu-id="a607a-105">You must provide a title for a font resource that does not have an embedded name.</span></span> <span data-ttu-id="a607a-106">Solo los archivos de recursos de fuente. TTC,. ttf y. OTF no requieren un título, ya que estos archivos contienen un nombre incrustado.</span><span class="sxs-lookup"><span data-stu-id="a607a-106">Only .ttc, .ttf, and .otf font resource files do not require a title, because these files contain an embedded name.</span></span> <span data-ttu-id="a607a-107">No proporcione un título para un recurso de fuente que contenga un nombre incrustado, ya que el sistema registra la fuente dos veces.</span><span class="sxs-lookup"><span data-stu-id="a607a-107">Do not provide a title for a font resource that contains an embedded name because the system then registers the font twice.</span></span>

<span data-ttu-id="a607a-108">**[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** ICE51 no comprueba los archivos de recursos de fuente. OTF.</span><span class="sxs-lookup"><span data-stu-id="a607a-108">**[Windows Installer 4.5 and earlier](not-supported-in-windows-installer-4-5.md):** ICE51 does not check .otf font resource files.</span></span>

## <a name="result"></a><span data-ttu-id="a607a-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="a607a-109">Result</span></span>

<span data-ttu-id="a607a-110">ICE51 publica un error si hay archivos de recursos de fuentes. TTC,. ttf y. OTF con títulos.</span><span class="sxs-lookup"><span data-stu-id="a607a-110">ICE51 posts an error if there are any .ttc, .ttf, and .otf font resource files with titles.</span></span> <span data-ttu-id="a607a-111">ICE51 publica una advertencia si hay otros archivos de recursos de fuente sin un título.</span><span class="sxs-lookup"><span data-stu-id="a607a-111">ICE51 posts a warning if there are any other font resource files without a title.</span></span>

## <a name="example"></a><span data-ttu-id="a607a-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a607a-112">Example</span></span>

<span data-ttu-id="a607a-113">ICE51 notificaría la siguiente advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="a607a-113">ICE51 would report the following warning for the example shown.</span></span>

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

<span data-ttu-id="a607a-114">ICE51 notificaría el siguiente mensaje de error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="a607a-114">ICE51 would report the following error message for the example shown.</span></span>

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

<span data-ttu-id="a607a-115">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="a607a-115">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="a607a-116">Archivo</span><span class="sxs-lookup"><span data-stu-id="a607a-116">File</span></span>  | <span data-ttu-id="a607a-117">FileName</span><span class="sxs-lookup"><span data-stu-id="a607a-117">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="a607a-118">Font1</span><span class="sxs-lookup"><span data-stu-id="a607a-118">Font1</span></span> | <span data-ttu-id="a607a-119">font1. ttf</span><span class="sxs-lookup"><span data-stu-id="a607a-119">font1.ttf</span></span> |
| <span data-ttu-id="a607a-120">Font2</span><span class="sxs-lookup"><span data-stu-id="a607a-120">Font2</span></span> | <span data-ttu-id="a607a-121">font2. fon</span><span class="sxs-lookup"><span data-stu-id="a607a-121">font2.fon</span></span> |



 

[<span data-ttu-id="a607a-122">Tabla de fuentes</span><span class="sxs-lookup"><span data-stu-id="a607a-122">Font Table</span></span>](font-table.md)



| <span data-ttu-id="a607a-123">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="a607a-123">File\_</span></span> | <span data-ttu-id="a607a-124">FontTitle</span><span class="sxs-lookup"><span data-stu-id="a607a-124">FontTitle</span></span>          |
|--------|--------------------|
| <span data-ttu-id="a607a-125">Font1</span><span class="sxs-lookup"><span data-stu-id="a607a-125">Font1</span></span>  | <span data-ttu-id="a607a-126">Una fuente realmente atractiva</span><span class="sxs-lookup"><span data-stu-id="a607a-126">A Really Cool Font</span></span> |
| <span data-ttu-id="a607a-127">Font2</span><span class="sxs-lookup"><span data-stu-id="a607a-127">Font2</span></span>  |                    |



 

## <a name="related-topics"></a><span data-ttu-id="a607a-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a607a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a607a-129">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="a607a-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



