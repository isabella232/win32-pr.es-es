---
description: Guardar o descartar cambios
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Guardar o descartar cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907090"
---
# <a name="saving-or-discarding-changes"></a><span data-ttu-id="d7482-103">Guardar o descartar cambios</span><span class="sxs-lookup"><span data-stu-id="d7482-103">Saving or Discarding Changes</span></span>

<span data-ttu-id="d7482-104">Cuando se establecen propiedades en un elemento, en realidad no se registra ningún cambio en el catálogo de COM+ hasta que se guardan los cambios explícitamente.</span><span class="sxs-lookup"><span data-stu-id="d7482-104">When you set properties on an item, no changes are actually recorded to the COM+ catalog until you explicitly save changes.</span></span> <span data-ttu-id="d7482-105">Para ello, use el método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para la colección que contiene el elemento.</span><span class="sxs-lookup"><span data-stu-id="d7482-105">You do this using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object for the collection containing the item.</span></span>

<span data-ttu-id="d7482-106">Si desea descartar los cambios que aún no se han confirmado, puede llamar al método de [**rellenado**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d7482-106">If you want to discard changes that have not yet been committed, you can call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="d7482-107">Esto Lee todos los datos persistentes del catálogo de COM+ para todos los elementos de la colección, con lo que se eliminan eficazmente los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="d7482-107">This reads in all persistent data from the COM+ catalog for all items in the collection, effectively deleting any pending changes.</span></span>

<span data-ttu-id="d7482-108">Cuando se utiliza [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), las incoherencias en la configuración de propiedades que ha elegido producen un error y **SaveChanges** no puede escribir el objeto que devolvió el error.</span><span class="sxs-lookup"><span data-stu-id="d7482-108">When you use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), any inconsistencies in property settings that you have chosen result in an error, and **SaveChanges** fails to write the object that returned the error.</span></span> <span data-ttu-id="d7482-109">Todas las propiedades de un elemento determinado se escriben o no se escriben en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="d7482-109">All properties on a given item either are written or fail to be written as a whole.</span></span>

<span data-ttu-id="d7482-110">Sin embargo, cuando se producen errores de escritura, es posible que no se deba a una configuración incompatible. es posible que se haya producido algún otro error.</span><span class="sxs-lookup"><span data-stu-id="d7482-110">However, when write errors occur, they might not be due to incompatible settings; some other failure might have occurred.</span></span> <span data-ttu-id="d7482-111">Debe inspeccionar los detalles del error para estar seguro.</span><span class="sxs-lookup"><span data-stu-id="d7482-111">You need to inspect the details of the failure to be certain.</span></span> <span data-ttu-id="d7482-112">Para obtener más información, consulte [controlar errores de administración de com+](handling-com--administration-errors.md) e [interdependencias entre propiedades](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d7482-112">For more information, see [Handling COM+ Administration Errors](handling-com--administration-errors.md) and [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="d7482-113">Como norma general, cuanto más cambios intente guardar a la vez, especialmente en el hecho de que se produzcan cambios en varios objetos, más probabilidades de que obtenga un error y más difícil sea hacer un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="d7482-113">As a general rule, the more changes you attempt to save at once, particularly changes to multiple objects, the more likely you are to get an error and the more difficult it is to track down.</span></span>

<span data-ttu-id="d7482-114">Además, entre las llamadas a [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), no hay ningún bloqueo en los elementos de la colección; es posible la contención.</span><span class="sxs-lookup"><span data-stu-id="d7482-114">Additionally, between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), you do not have a lock on the items in the collection; contention is possible.</span></span> <span data-ttu-id="d7482-115">Para obtener más información, vea [obtener y establecer propiedades](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d7482-115">For more details, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7482-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7482-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7482-117">Obtener y establecer propiedades</span><span class="sxs-lookup"><span data-stu-id="d7482-117">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="d7482-118">Interdependencias entre propiedades</span><span class="sxs-lookup"><span data-stu-id="d7482-118">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="d7482-119">Consultar las propiedades disponibles</span><span class="sxs-lookup"><span data-stu-id="d7482-119">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> </dl>

 

 



