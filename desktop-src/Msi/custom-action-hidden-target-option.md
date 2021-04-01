---
description: Utilice las siguientes marcas de opciones para especificar que el instalador no escriba el valor especificado en el campo de destino de la tabla CustomAction en el registro. Para establecer la opción, agregue el valor de esta tabla al valor del campo Type de la tabla CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Opción de destino oculto de acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082789"
---
# <a name="custom-action-hidden-target-option"></a><span data-ttu-id="1f820-104">Opción de destino oculto de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="1f820-104">Custom Action Hidden Target Option</span></span>

<span data-ttu-id="1f820-105">Utilice las siguientes marcas de opciones para especificar que el instalador no escriba el valor especificado en el campo de destino de la [tabla CustomAction](customaction-table.md) en el registro.</span><span class="sxs-lookup"><span data-stu-id="1f820-105">Use the following option flags to specify that the installer not write the value entered into the Target field of the [CustomAction table](customaction-table.md) into the log.</span></span> <span data-ttu-id="1f820-106">Para establecer la opción, agregue el valor de esta tabla al valor del campo Type de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="1f820-106">To set the option add the value in this table to the value in the Type field of the CustomAction table.</span></span>



| <span data-ttu-id="1f820-107">Constante</span><span class="sxs-lookup"><span data-stu-id="1f820-107">Constant</span></span>                            | <span data-ttu-id="1f820-108">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1f820-108">Hexadecimal</span></span> | <span data-ttu-id="1f820-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="1f820-109">Decimal</span></span> | <span data-ttu-id="1f820-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f820-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f820-111">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="1f820-111">(none)</span></span>                              | <span data-ttu-id="1f820-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="1f820-112">0x0000</span></span>      | <span data-ttu-id="1f820-113">0</span><span class="sxs-lookup"><span data-stu-id="1f820-113">0</span></span>       | <span data-ttu-id="1f820-114">El instalador puede escribir el valor en la columna de destino de la tabla CustomAction en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="1f820-114">The installer may write the value in the Target column of the CustomAction table into the log file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1f820-115">**msidbCustomActionTypeHideTarget**</span><span class="sxs-lookup"><span data-stu-id="1f820-115">**msidbCustomActionTypeHideTarget**</span></span> | <span data-ttu-id="1f820-116">0x2000</span><span class="sxs-lookup"><span data-stu-id="1f820-116">0x2000</span></span>      | <span data-ttu-id="1f820-117">8192</span><span class="sxs-lookup"><span data-stu-id="1f820-117">8192</span></span>    | <span data-ttu-id="1f820-118">No se impide que el instalador escriba el valor en la columna de destino de la [tabla CustomAction](customaction-table.md) en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="1f820-118">The installer is prevented from writing the value in the Target column of the [CustomAction table](customaction-table.md) into the log file.</span></span> <span data-ttu-id="1f820-119">La propiedad CustomActionData tampoco se registra cuando el instalador ejecuta la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="1f820-119">The CustomActionData property is also not logged when the installer executes the custom action.</span></span><br/> <span data-ttu-id="1f820-120">Dado que el instalador establece el valor de CustomActionData desde una propiedad con el mismo nombre que la acción personalizada, dicha propiedad debe aparecer en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) para evitar que su valor aparezca en el registro.</span><span class="sxs-lookup"><span data-stu-id="1f820-120">Because the installer sets the value of CustomActionData from a property with the same name as the custom action, that property must be listed in the [**MsiHiddenProperties**](msihiddenproperties.md) Property to prevent its value from appearing in the log.</span></span><br/> |



 

<span data-ttu-id="1f820-121">Para obtener más información, consulte [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md) .</span><span class="sxs-lookup"><span data-stu-id="1f820-121">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f820-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f820-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f820-123">Referencia de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="1f820-123">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="1f820-124">Acerca de las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="1f820-124">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="1f820-125">Uso de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="1f820-125">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 




