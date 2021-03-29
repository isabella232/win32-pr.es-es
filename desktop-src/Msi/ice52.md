---
description: ICE52 comprueba las propiedades privadas en la tabla AppSearch. Vea acerca de las propiedades.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911909"
---
# <a name="ice52"></a><span data-ttu-id="ef47e-104">ICE52</span><span class="sxs-lookup"><span data-stu-id="ef47e-104">ICE52</span></span>

<span data-ttu-id="ef47e-105">ICE52 comprueba las propiedades privadas en la [tabla AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef47e-105">ICE52 checks for private properties in the [AppSearch table](appsearch-table.md).</span></span> <span data-ttu-id="ef47e-106">Vea [acerca de las propiedades](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ef47e-106">See [About Properties](about-properties.md).</span></span>

<span data-ttu-id="ef47e-107">Al usar Windows 2000, todas las propiedades establecidas en la columna propiedad de la tabla AppSearch deben ser propiedades públicas.</span><span class="sxs-lookup"><span data-stu-id="ef47e-107">When using Windows 2000 all properties set in the Property column of the AppSearch table must be public properties.</span></span>

## <a name="result"></a><span data-ttu-id="ef47e-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="ef47e-108">Result</span></span>

<span data-ttu-id="ef47e-109">ICE52 expone una advertencia si hay una propiedad privada en la tabla AppSearch.</span><span class="sxs-lookup"><span data-stu-id="ef47e-109">ICE52 posts a warning if there is a private property in the AppSearch table.</span></span>

## <a name="example"></a><span data-ttu-id="ef47e-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef47e-110">Example</span></span>

<span data-ttu-id="ef47e-111">ICE52 envía la siguiente advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="ef47e-111">ICE52 posts the following warning for the example shown.</span></span>

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[<span data-ttu-id="ef47e-112">Tabla AppSearch</span><span class="sxs-lookup"><span data-stu-id="ef47e-112">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="ef47e-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ef47e-113">Property</span></span>  | <span data-ttu-id="ef47e-114">Firma</span><span class="sxs-lookup"><span data-stu-id="ef47e-114">Signature</span></span>  |
|-----------|------------|
| <span data-ttu-id="ef47e-115">PROPERTY1</span><span class="sxs-lookup"><span data-stu-id="ef47e-115">PROPERTY1</span></span> | <span data-ttu-id="ef47e-116">Signature1</span><span class="sxs-lookup"><span data-stu-id="ef47e-116">Signature1</span></span> |
| <span data-ttu-id="ef47e-117">Property2</span><span class="sxs-lookup"><span data-stu-id="ef47e-117">Property2</span></span> | <span data-ttu-id="ef47e-118">Signature2</span><span class="sxs-lookup"><span data-stu-id="ef47e-118">Signature2</span></span> |



 

<span data-ttu-id="ef47e-119">Para corregir este cambio de advertencia en la propiedad pública personalizada: PROPERTY2.</span><span class="sxs-lookup"><span data-stu-id="ef47e-119">To fix this warning change to the custom public property: PROPERTY2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef47e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef47e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef47e-121">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="ef47e-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



