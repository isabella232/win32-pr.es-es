---
description: El instalador establece las propiedades mediante el orden de prioridad siguiente. Un valor de propiedad de esta lista puede invalidar un valor que se encuentra después de él y que se ha reemplazado por un valor que está delante de él en la lista.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Orden de prioridad de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678469"
---
# <a name="order-of-property-precedence"></a><span data-ttu-id="29f35-104">Orden de prioridad de propiedad</span><span class="sxs-lookup"><span data-stu-id="29f35-104">Order of Property Precedence</span></span>

<span data-ttu-id="29f35-105">El instalador establece las propiedades mediante el orden de prioridad siguiente.</span><span class="sxs-lookup"><span data-stu-id="29f35-105">The installer sets properties using the following order of precedence.</span></span> <span data-ttu-id="29f35-106">Un valor de propiedad de esta lista puede invalidar un valor que se encuentra después de él y que se ha reemplazado por un valor que está delante de él en la lista.</span><span class="sxs-lookup"><span data-stu-id="29f35-106">A property value in this list can override a value that comes after it and be overridden by a value coming before it in the list.</span></span>

1.  <span data-ttu-id="29f35-107">Propiedades especificadas por el entorno operativo.</span><span class="sxs-lookup"><span data-stu-id="29f35-107">Properties specified by the operating environment.</span></span>
2.  <span data-ttu-id="29f35-108">[Propiedades públicas](public-properties.md) establecidas en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="29f35-108">[Public properties](public-properties.md) set on the command line.</span></span>
3.  <span data-ttu-id="29f35-109">Propiedades públicas enumeradas por [**AdminProperties**](adminproperties.md) propertyset durante una [instalación administrativa](administrative-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="29f35-109">Public properties listed by the [**AdminProperties**](adminproperties.md) propertyset during an [administrative installation](administrative-installation.md) .</span></span>
4.  <span data-ttu-id="29f35-110">Propiedades públicas o privadas establecidas durante la aplicación de una [*transformación*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="29f35-110">Public or private properties set during the application of a [*transform*](t-gly.md).</span></span>
5.  <span data-ttu-id="29f35-111">Propiedad pública o privada que se establece mediante la creación de la [tabla de propiedades](property-table.md) del archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="29f35-111">Public or private property that set by authoring the [Property table](property-table.md) of the .msi file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29f35-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29f35-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f35-113">Acerca de las propiedades</span><span class="sxs-lookup"><span data-stu-id="29f35-113">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



