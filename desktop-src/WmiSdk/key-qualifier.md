---
description: El calificador de clave indica si la propiedad forma parte del identificador de espacio de nombres.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Calificador de clave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816123"
---
# <a name="key-qualifier"></a><span data-ttu-id="92784-103">Calificador de clave</span><span class="sxs-lookup"><span data-stu-id="92784-103">Key Qualifier</span></span>

<span data-ttu-id="92784-104">El calificador de **clave** indica si la propiedad forma parte del identificador de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="92784-104">The **Key** qualifier indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="92784-105">Si hay más de una propiedad que tiene el calificador de **clave** , todas estas propiedades forman colectivamente la clave (una clave compuesta).</span><span class="sxs-lookup"><span data-stu-id="92784-105">If more than one property has the **Key** qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="92784-106">Cuando se toman juntas, las propiedades clave deben proporcionar una referencia única para cada instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="92784-106">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="92784-107">Si este calificador se coloca en una propiedad, solo se permite el valor **true** .</span><span class="sxs-lookup"><span data-stu-id="92784-107">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

<span data-ttu-id="92784-108">Puede usar cualquier tipo de propiedad, excepto los siguientes:</span><span class="sxs-lookup"><span data-stu-id="92784-108">You can use any property type except for the following:</span></span>

-   <span data-ttu-id="92784-109">Matrices</span><span class="sxs-lookup"><span data-stu-id="92784-109">Arrays</span></span>
-   <span data-ttu-id="92784-110">Números reales y de punto flotante</span><span class="sxs-lookup"><span data-stu-id="92784-110">Real and floating-point numbers</span></span>
-   <span data-ttu-id="92784-111">Objetos insertados</span><span class="sxs-lookup"><span data-stu-id="92784-111">Embedded objects</span></span>
-   <span data-ttu-id="92784-112">Caracteres inferiores a ASCII 32 (es decir, caracteres de espacio en blanco)</span><span class="sxs-lookup"><span data-stu-id="92784-112">Characters lower than ASCII 32 (that is, white space characters)</span></span>
-   <span data-ttu-id="92784-113">Las cadenas de caracteres de tipo **char16** o cadenas de caracteres que se definen como claves deben contener valores mayores que U + 0020.</span><span class="sxs-lookup"><span data-stu-id="92784-113">Character strings of type **char16** or character strings that are defined as keys must contain values greater than U+0020.</span></span> <span data-ttu-id="92784-114">Esto se debe a que WMI usa valores de clave en las rutas de acceso de objeto y no se pueden usar caracteres no imprimibles en una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="92784-114">This is because WMI uses key values in object paths, and you cannot use nonprinting characters in an object path.</span></span>

<span data-ttu-id="92784-115">Cuando una clase primaria especifica una clave, todas las clases derivadas de la clase primaria heredan esa clave.</span><span class="sxs-lookup"><span data-stu-id="92784-115">When a parent class specifies a key, all classes derived from the parent class inherit that key.</span></span> <span data-ttu-id="92784-116">Las clases derivadas no pueden modificar la clave heredada ni definir ninguna propiedad de clave nueva.</span><span class="sxs-lookup"><span data-stu-id="92784-116">The derived classes cannot alter the inherited key or define any new key property.</span></span> <span data-ttu-id="92784-117">Sin embargo, al derivar una subclase de una clase abstracta sin una clave, puede introducir una clave en la subclase.</span><span class="sxs-lookup"><span data-stu-id="92784-117">However, when you derive a subclass from an abstract class without a key, you can introduce a key in the subclass.</span></span>

<span data-ttu-id="92784-118">Todas las clases que definen más de una instancia de deben especificar una clave.</span><span class="sxs-lookup"><span data-stu-id="92784-118">All classes that define more than one instance must specify a key.</span></span> <span data-ttu-id="92784-119">Dado que las clases abstractas no definen ninguna instancia, no necesitan especificar claves.</span><span class="sxs-lookup"><span data-stu-id="92784-119">Because abstract classes do not define any instances, they do not need to specify keys.</span></span> <span data-ttu-id="92784-120">Dado que las clases singleton definen solo una instancia, no pueden especificar claves.</span><span class="sxs-lookup"><span data-stu-id="92784-120">Because singleton classes define only one instance, they cannot specify keys.</span></span>

<span data-ttu-id="92784-121">Las claves se escriben una vez en la creación de instancias de objeto y no se deben modificar posteriormente.</span><span class="sxs-lookup"><span data-stu-id="92784-121">Keys are written one time at object instantiation and must not be modified later.</span></span> <span data-ttu-id="92784-122">No tiene sentido aplicar un valor predeterminado a una propiedad con clave calificada.</span><span class="sxs-lookup"><span data-stu-id="92784-122">It does not make sense to apply a default value to a key-qualified property.</span></span>

## <a name="requirements"></a><span data-ttu-id="92784-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92784-123">Requirements</span></span>



| <span data-ttu-id="92784-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="92784-124">Requirement</span></span> | <span data-ttu-id="92784-125">Value</span><span class="sxs-lookup"><span data-stu-id="92784-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="92784-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92784-126">Minimum supported client</span></span><br/> | <span data-ttu-id="92784-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92784-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="92784-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92784-128">Minimum supported server</span></span><br/> | <span data-ttu-id="92784-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92784-129">Windows Server 2008</span></span><br/> |



 

 




