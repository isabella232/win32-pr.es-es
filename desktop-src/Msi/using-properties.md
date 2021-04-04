---
description: En las secciones siguientes se describe el uso de las propiedades de instalador integradas y las propiedades adicionales definidas por el autor del paquete.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Utilizar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154367"
---
# <a name="using-properties"></a><span data-ttu-id="16876-103">Utilizar propiedades</span><span class="sxs-lookup"><span data-stu-id="16876-103">Using Properties</span></span>

<span data-ttu-id="16876-104">En las secciones siguientes se describe el uso de las propiedades de instalador integradas y las propiedades adicionales definidas por el autor del paquete.</span><span class="sxs-lookup"><span data-stu-id="16876-104">The following sections describe using the built-in installer properties and additional properties defined by the package author.</span></span> <span data-ttu-id="16876-105">Las propiedades pueden ser [propiedades públicas](public-properties.md) o [propiedades privadas](private-properties.md).</span><span class="sxs-lookup"><span data-stu-id="16876-105">Properties can be either [public properties](public-properties.md) or [private properties](private-properties.md).</span></span> <span data-ttu-id="16876-106">Todas las propiedades que deben definirse al inicializarse el instalador deben tener su nombre y valor inicial enumerados en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="16876-106">Every property that needs to be defined upon initialization of the installer must have its name and initial value listed in the [Property table](property-table.md).</span></span> <span data-ttu-id="16876-107">Las propiedades que tienen un valor NULL no se muestran en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="16876-107">Properties having a Null value are not listed in the Property table.</span></span> <span data-ttu-id="16876-108">Puede obtener o establecer propiedades de programas y acciones personalizadas y establecer propiedades públicas desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="16876-108">You can get or set properties from programs and custom actions and set public properties from the command line.</span></span> <span data-ttu-id="16876-109">El proceso de instalación se puede modificar mediante el uso de propiedades en instrucciones condicionales.</span><span class="sxs-lookup"><span data-stu-id="16876-109">The installation process can be modified by using properties in conditional statements.</span></span>

[<span data-ttu-id="16876-110">Restricciones en los nombres de propiedad</span><span class="sxs-lookup"><span data-stu-id="16876-110">Restrictions on Property Names</span></span>](restrictions-on-property-names.md)

[<span data-ttu-id="16876-111">Inicialización de valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="16876-111">Initialization of Property Values</span></span>](initialization-of-property-values.md)

[<span data-ttu-id="16876-112">Obtener y establecer propiedades</span><span class="sxs-lookup"><span data-stu-id="16876-112">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)

[<span data-ttu-id="16876-113">Usar propiedades en instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="16876-113">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)

[<span data-ttu-id="16876-114">Usar una propiedad de directorio en una ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="16876-114">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)

> [!Note]  
> <span data-ttu-id="16876-115">No use propiedades para contraseñas u otra información que deba permanecer segura.</span><span class="sxs-lookup"><span data-stu-id="16876-115">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="16876-116">El instalador puede escribir el valor de una propiedad creada en la tabla de propiedades o crearla en tiempo de ejecución en un registro o en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="16876-116">The installer may write the value of a property authored into the Property table or created at runtime into a log or the system registry.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="16876-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16876-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16876-118">Acerca de las propiedades</span><span class="sxs-lookup"><span data-stu-id="16876-118">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="16876-119">Referencia de propiedades</span><span class="sxs-lookup"><span data-stu-id="16876-119">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



