---
description: ICE58 comprueba que la tabla de medios no tiene más de 80 filas.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002561"
---
# <a name="ice58"></a><span data-ttu-id="dfc4e-103">ICE58</span><span class="sxs-lookup"><span data-stu-id="dfc4e-103">ICE58</span></span>

<span data-ttu-id="dfc4e-104">ICE58 comprueba que la [tabla de medios](media-table.md) no tiene más de 80 filas.</span><span class="sxs-lookup"><span data-stu-id="dfc4e-104">ICE58 checks that your [Media table](media-table.md) does not have more than 80 rows.</span></span>

## <a name="result"></a><span data-ttu-id="dfc4e-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="dfc4e-105">Result</span></span>

<span data-ttu-id="dfc4e-106">Las advertencias que emite ICE58 provocan un error en la instalación a menos que el paquete se instale con Windows Installer 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="dfc4e-106">Warnings reported by ICE58 cause the installation to fail unless the package is installed with Windows Installer 2.0 or later.</span></span> <span data-ttu-id="dfc4e-107">A partir de Windows Installer 2,0, se quita la restricción a más de 80 entradas de la tabla de medios.</span><span class="sxs-lookup"><span data-stu-id="dfc4e-107">Beginning with Windows Installer 2.0, the restriction to more than 80 media table entries is removed.</span></span> <span data-ttu-id="dfc4e-108">No se emite ninguna advertencia si la propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) del paquete es mayor o igual que 150.</span><span class="sxs-lookup"><span data-stu-id="dfc4e-108">No warning is issued if the package's [**Page Count Summary**](page-count-summary.md) Property is greater than or equal to 150.</span></span> <span data-ttu-id="dfc4e-109">Los paquetes del esquema 200 o superior solo se pueden instalar mediante Windows Installer 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="dfc4e-109">Packages of schema 200 or higher can only be installed by Windows Installer 2.0 or later.</span></span>

## <a name="example"></a><span data-ttu-id="dfc4e-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dfc4e-110">Example</span></span>

<span data-ttu-id="dfc4e-111">ICE58 notifica los siguientes errores y advertencias para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="dfc4e-111">ICE58 reports the following errors and warnings for the example shown.</span></span>

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

<span data-ttu-id="dfc4e-112">Para corregir este error, elimine las entradas de la tabla de medios no utilizadas, consolide las entradas de la tabla de medios que hacen referencia a los mismos medios y reempaquete la aplicación para reducir el contenido multimedia necesario.</span><span class="sxs-lookup"><span data-stu-id="dfc4e-112">To fix this error, eliminate any unused media table entries, consolidate media table entries that refer to the same media, and repackage your application to reduce the media required.</span></span>

<span data-ttu-id="dfc4e-113">[Tabla de medios](media-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="dfc4e-113">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="dfc4e-114">Detectaron</span><span class="sxs-lookup"><span data-stu-id="dfc4e-114">DiskId</span></span> | <span data-ttu-id="dfc4e-115">LastSequence\_</span><span class="sxs-lookup"><span data-stu-id="dfc4e-115">LastSequence\_</span></span> |
|--------|----------------|
| <span data-ttu-id="dfc4e-116">1</span><span class="sxs-lookup"><span data-stu-id="dfc4e-116">1</span></span>      | <span data-ttu-id="dfc4e-117">10</span><span class="sxs-lookup"><span data-stu-id="dfc4e-117">10</span></span>             |
| <span data-ttu-id="dfc4e-118">2</span><span class="sxs-lookup"><span data-stu-id="dfc4e-118">2</span></span>      | <span data-ttu-id="dfc4e-119">20</span><span class="sxs-lookup"><span data-stu-id="dfc4e-119">20</span></span>             |
| <span data-ttu-id="dfc4e-120">...</span><span class="sxs-lookup"><span data-stu-id="dfc4e-120">...</span></span>    | <span data-ttu-id="dfc4e-121">...</span><span class="sxs-lookup"><span data-stu-id="dfc4e-121">...</span></span>            |
| <span data-ttu-id="dfc4e-122">81</span><span class="sxs-lookup"><span data-stu-id="dfc4e-122">81</span></span>     | <span data-ttu-id="dfc4e-123">810</span><span class="sxs-lookup"><span data-stu-id="dfc4e-123">810</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="dfc4e-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dfc4e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfc4e-125">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="dfc4e-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



