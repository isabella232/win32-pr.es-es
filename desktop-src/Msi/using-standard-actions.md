---
description: Una acción se ejecuta en el Windows Installer llamando a la función MsiDoAction o incluyendo la acción en una tabla de secuencia.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Uso de acciones estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652547"
---
# <a name="using-standard-actions"></a><span data-ttu-id="933d8-103">Uso de acciones estándar</span><span class="sxs-lookup"><span data-stu-id="933d8-103">Using Standard Actions</span></span>

<span data-ttu-id="933d8-104">Una acción se ejecuta en el Windows Installer llamando a la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o incluyendo la acción en una tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="933d8-104">An action is executed in the Windows Installer either by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function or including the action in a sequence table.</span></span> <span data-ttu-id="933d8-105">Dado que la mayoría de las acciones encapsulan un solo propósito, la manera más común de usar acciones es ordenar una serie de acciones en una secuencia para realizar una tarea más grande.</span><span class="sxs-lookup"><span data-stu-id="933d8-105">Because most actions encapsulate a single purpose, the most common way to use actions is to order a series of actions into a sequence to accomplish a larger task.</span></span> <span data-ttu-id="933d8-106">El instalador tiene tres acciones de nivel superior estándar que llaman a un conjunto asociado de tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="933d8-106">The installer has three standard top-level actions that call an associated set of sequence tables.</span></span> <span data-ttu-id="933d8-107">Estas tablas de secuencia asociadas pueden contener acciones estándar, acciones personalizadas y elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="933d8-107">These associated sequence tables may contain standard actions, custom actions, and user-interface elements.</span></span> <span data-ttu-id="933d8-108">Cada acción de una tabla de secuencia tiene un número de secuencia asociado y también puede tener una expresión condicional asociada.</span><span class="sxs-lookup"><span data-stu-id="933d8-108">Each action in a sequence table has an associated sequence number and may also have an associated conditional expression.</span></span> <span data-ttu-id="933d8-109">Todas las acciones de una tabla de secuencia se visitan en orden y solo se ejecutan si la expresión condicional se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="933d8-109">All actions in a sequence table are visited in order and are only executed if the conditional expression evaluates to True.</span></span>

<span data-ttu-id="933d8-110">Aunque una acción estándar puede tener cualquier número de secuencia asociado, muchas tienen restricciones de secuencia que deben seguirse para que la acción funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="933d8-110">While a standard action can have any sequence number associated with it, many have sequence restrictions which must be followed for the action to function properly.</span></span> <span data-ttu-id="933d8-111">Por ejemplo, la [acción FileCost](filecost-action.md)debe llamarse después de la [acción CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="933d8-111">For example the [FileCost action](filecost-action.md), must be called after the [CostInitialize action](costinitialize-action.md).</span></span> <span data-ttu-id="933d8-112">Para obtener más información sobre las restricciones de la secuencia de acciones estándar, vea [acciones con restricciones de secuenciación](actions-with-sequencing-restrictions.md), [acciones sin restricciones de secuenciación](actions-without-sequencing-restrictions.md)o [referencia de acciones estándar](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="933d8-112">For more information on standard action sequencing restrictions, see [Actions with Sequencing Restrictions](actions-with-sequencing-restrictions.md), [Actions without Sequencing Restrictions](actions-without-sequencing-restrictions.md), or [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="933d8-113">En los temas siguientes se proporciona más información acerca del uso de las acciones estándar.</span><span class="sxs-lookup"><span data-stu-id="933d8-113">The following topics provide more information about using standard actions.</span></span>

-   [<span data-ttu-id="933d8-114">Publicar productos, características y componentes</span><span class="sxs-lookup"><span data-stu-id="933d8-114">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)
-   [<span data-ttu-id="933d8-115">Búsqueda de archivos</span><span class="sxs-lookup"><span data-stu-id="933d8-115">File Searching</span></span>](file-searching.md)
-   [<span data-ttu-id="933d8-116">Costo de archivos</span><span class="sxs-lookup"><span data-stu-id="933d8-116">File Costing</span></span>](file-costing.md)
-   [<span data-ttu-id="933d8-117">Instalación de archivos</span><span class="sxs-lookup"><span data-stu-id="933d8-117">File Installation</span></span>](file-installation.md)
-   [<span data-ttu-id="933d8-118">Modificar el registro</span><span class="sxs-lookup"><span data-stu-id="933d8-118">Modifying the Registry</span></span>](modifying-the-registry.md)
-   [<span data-ttu-id="933d8-119">Ejecutar acciones</span><span class="sxs-lookup"><span data-stu-id="933d8-119">Running Actions</span></span>](running-actions.md)

<span data-ttu-id="933d8-120">Vea también [sobre acciones estándar](about-standard-actions.md) o [referencia de acciones estándar](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="933d8-120">See also [About Standard Actions](about-standard-actions.md) or [Standard Actions Reference](standard-actions-reference.md).</span></span>

 

 



