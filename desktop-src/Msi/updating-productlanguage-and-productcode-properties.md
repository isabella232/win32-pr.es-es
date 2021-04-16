---
description: La propiedad ProductLanguage se debe actualizar al identificador de idioma numérico (LANGID) del nuevo lenguaje.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Actualización de las propiedades ProductLanguage y ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678397"
---
# <a name="updating-productlanguage-and-productcode-properties"></a><span data-ttu-id="93f36-103">Actualización de las propiedades ProductLanguage y ProductCode</span><span class="sxs-lookup"><span data-stu-id="93f36-103">Updating ProductLanguage and ProductCode Properties</span></span>

<span data-ttu-id="93f36-104">La propiedad [**ProductLanguage**](productlanguage.md) se debe actualizar al identificador de idioma numérico (LANGID) del nuevo lenguaje.</span><span class="sxs-lookup"><span data-stu-id="93f36-104">The [**ProductLanguage**](productlanguage.md) property must be updated to the numeric language identifier (LANGID) for the new language.</span></span> <span data-ttu-id="93f36-105">En el caso del ejemplo de localización, el valor de la propiedad **ProductLanguage** debe cambiarse del langid para inglés (1033) al langid para francés (1036) en la tabla de [propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="93f36-105">In the case of the localization example, the value of the **ProductLanguage** property must be changed from the LANGID for English (1033) to the LANGID for French (1036) in the [Property table](property-table.md).</span></span>

<span data-ttu-id="93f36-106">El valor de la propiedad [**ProductCode**](productcode.md) en la [tabla de propiedades](property-table.md) debe cambiarse a un nuevo valor único al localizar una base de datos porque un producto localizado se considera un producto diferente.</span><span class="sxs-lookup"><span data-stu-id="93f36-106">The value of the [**ProductCode**](productcode.md) property in the [Property table](property-table.md) must be changed to a new, unique value when localizing a database because a localized product is considered a different product.</span></span> <span data-ttu-id="93f36-107">Por ejemplo, las versiones en alemán y en Inglés de una aplicación se consideran dos productos diferentes y deben tener distintos códigos de producto.</span><span class="sxs-lookup"><span data-stu-id="93f36-107">For example, the German and English versions of an application are considered two different products and must have different product codes.</span></span> <span data-ttu-id="93f36-108">Consulte [códigos de producto](product-codes.md).</span><span class="sxs-lookup"><span data-stu-id="93f36-108">See [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="93f36-109">Utilice el editor de tablas de base de datos para actualizar los valores de las propiedades ProductCode y ProductLanguage en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="93f36-109">Use your database table editor to update the values of the ProductCode and ProductLanguage properties in the Property table.</span></span> <span data-ttu-id="93f36-110">No reutilice el GUID que se muestra si copia este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="93f36-110">Do not reuse the GUID shown if you copy this example.</span></span>

[<span data-ttu-id="93f36-111">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="93f36-111">Property Table</span></span>](property-table.md)



| <span data-ttu-id="93f36-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="93f36-112">Property</span></span>                                   | <span data-ttu-id="93f36-113">Value</span><span class="sxs-lookup"><span data-stu-id="93f36-113">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="93f36-114">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="93f36-114">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="93f36-115">{EE389960-E426-4EEA-B669-AD8129249881}</span><span class="sxs-lookup"><span data-stu-id="93f36-115">{EE389960-E426-4EEA-B669-AD8129249881}</span></span> |
| [<span data-ttu-id="93f36-116">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="93f36-116">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="93f36-117">1036</span><span class="sxs-lookup"><span data-stu-id="93f36-117">1036</span></span>                                   |



 

[<span data-ttu-id="93f36-118">Continuar</span><span class="sxs-lookup"><span data-stu-id="93f36-118">Continue</span></span>](updating-a-summary-information-stream.md)

 

 



