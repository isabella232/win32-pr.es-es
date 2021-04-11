---
description: El espacio de nombres WMI es un objeto de programación que define el ámbito de un conjunto de clases e instancias. Las clases del proveedor de WMI se deben definir dentro de un espacio de nombres.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Crear jerarquías en WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276266"
---
# <a name="creating-hierarchies-within-wmi"></a><span data-ttu-id="16696-104">Crear jerarquías en WMI</span><span class="sxs-lookup"><span data-stu-id="16696-104">Creating Hierarchies Within WMI</span></span>

<span data-ttu-id="16696-105">El [*espacio de nombres WMI*](gloss-n.md) es un objeto de programación que define el ámbito de un conjunto de clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="16696-105">[*WMI namespace*](gloss-n.md) is a programming object that defines the scope for a set of classes and instances.</span></span> <span data-ttu-id="16696-106">Las clases del proveedor de WMI se deben definir dentro de un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="16696-106">WMI provider classes must be defined inside a namespace.</span></span>

<span data-ttu-id="16696-107">Los espacios de nombres describen diferentes entornos administrados, como el entorno de SMS.</span><span class="sxs-lookup"><span data-stu-id="16696-107">Namespaces describe different managed environments, such as the SMS environment.</span></span> <span data-ttu-id="16696-108">Dado que las clases y las instancias de un esquema definen los componentes de un entorno administrado, cada esquema nuevo requiere un espacio de nombres nuevo.</span><span class="sxs-lookup"><span data-stu-id="16696-108">Because the classes and instances of a schema define the components of a managed environment, each new schema requires a new namespace.</span></span> <span data-ttu-id="16696-109">Por ejemplo, el \\ espacio de nombres root cimv2 contiene las clases e instancias definidas en el esquema de Win32, así como las clases de modelo de información común primario (CIM) de las que hereda el esquema de Win32.</span><span class="sxs-lookup"><span data-stu-id="16696-109">For example, the root\\cimv2 namespace contains the classes and instances defined in the Win32 schema as well as the parent Common Information Model (CIM) classes from which the Win32 schema inherits.</span></span> <span data-ttu-id="16696-110">Las clases CIM están definidas por el equipo de tareas de administración distribuida ([DMTF](https://www.dmtf.org/home)).</span><span class="sxs-lookup"><span data-stu-id="16696-110">CIM classes are defined by the Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).</span></span>

> [!Note]  
> <span data-ttu-id="16696-111">Para asegurarse de que todas las definiciones de clases de WMI para objetos administrados se restauran en el [*repositorio de WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador [**\# pragma autocover**](pragma-autorecover.md) en el archivo [*Managed Object Format (MOF)*](gloss-m.md) .</span><span class="sxs-lookup"><span data-stu-id="16696-111">To ensure that all of your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

 

<span data-ttu-id="16696-112">WMI define un espacio de nombres como una instancia de la clase de sistema de [**\_ \_ espacio de nombres**](--namespace.md) o cualquier clase que derive de un espacio de **\_ \_ nombres**.</span><span class="sxs-lookup"><span data-stu-id="16696-112">WMI defines a namespace as an instance of the [**\_\_Namespace**](--namespace.md) system class or any class that derives from **\_\_Namespace**.</span></span> <span data-ttu-id="16696-113">La clase de sistema de **\_ \_ espacio de nombres** tiene una propiedad única denominada **Name**, que debe ser única dentro del ámbito del espacio de nombres primario.</span><span class="sxs-lookup"><span data-stu-id="16696-113">The **\_\_Namespace** system class has a single property called **Name**, which must be unique within the scope of the parent namespace.</span></span> <span data-ttu-id="16696-114">La propiedad **Name** también debe contener una cadena que empiece por una letra.</span><span class="sxs-lookup"><span data-stu-id="16696-114">The **Name** property must also contain a string that begins with a letter.</span></span> <span data-ttu-id="16696-115">Todos los demás caracteres de la cadena pueden ser letras, dígitos o caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="16696-115">All other characters in the string can be letters, digits, or underscores.</span></span> <span data-ttu-id="16696-116">Todos los caracteres no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="16696-116">All characters are case-insensitive.</span></span>

<span data-ttu-id="16696-117">Además de determinar el nombre único de un espacio de nombres secundario, el espacio de nombres WMI primario puede proteger las instancias estáticas de las clases frente a modificaciones accidentales de otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="16696-117">In addition to determining the unique name for a child namespace, the parent WMI namespace can protect the static instances of your classes from accidental modification by other providers.</span></span> <span data-ttu-id="16696-118">Por ejemplo, puede que le resulte conveniente anidar un nuevo espacio de nombres en un espacio de nombres existente para otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="16696-118">For example, you may find it convenient to nest a new namespace under an existing namespace for another provider.</span></span> <span data-ttu-id="16696-119">Sin embargo, el proveedor original puede intentar actualizar todas las instancias de clase para que coincida con un nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="16696-119">However, the original provider may try to update all class instances to match up with a new schema.</span></span> <span data-ttu-id="16696-120">Al hacerlo, el proveedor original puede eliminar todos los subelementos secundarios de un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="16696-120">In doing so, the original provider may delete all sub-children in a namespace.</span></span> <span data-ttu-id="16696-121">Aunque puede ser una acción adecuada para el espacio de nombres de destino, puede afectar a las instancias de clase no relacionadas en un espacio de nombres secundario (es decir, sus propias clases de proveedor).</span><span class="sxs-lookup"><span data-stu-id="16696-121">While this may be an appropriate action for the target namespace, it may affect unrelated class instances in a child namespace (i.e., your own provider classes).</span></span>

<span data-ttu-id="16696-122">Por lo tanto, se recomienda crear y registrar el espacio de nombres como independiente de los espacios de nombres que no controle directamente.</span><span class="sxs-lookup"><span data-stu-id="16696-122">Therefore, it is generally recommended that you create and register your namespace as separate from namespaces that you do not directly control.</span></span> <span data-ttu-id="16696-123">Esto es especialmente cierto si las clases solo se derivan de clases CIM generales u otras clases de la empresa.</span><span class="sxs-lookup"><span data-stu-id="16696-123">This is especially true if your classes derive only from general CIM classes or other classes from your company.</span></span> <span data-ttu-id="16696-124">El espacio de nombres puede estar en el espacio de nombres **raíz** , como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="16696-124">Your namespace can be under the **Root** namespace, such as the following:</span></span>

<span data-ttu-id="16696-125">**Root/mycompany/mi producto**</span><span class="sxs-lookup"><span data-stu-id="16696-125">**Root/myCompany/myProduct**</span></span>

<span data-ttu-id="16696-126">En cambio, si la nueva clase se deriva de la clase de otro proveedor, puede que necesite almacenar la clase en un subespacio de nombres de ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="16696-126">In contrast, if your new class derives from the class of another provider, you may need to store your class in a sub-namespace of that provider.</span></span> <span data-ttu-id="16696-127">Tenga en cuenta que esto expone la nueva clase a la eliminación accidental por parte del proveedor original.</span><span class="sxs-lookup"><span data-stu-id="16696-127">Note that this exposes your new class to accidental deletion by the original provider.</span></span>

<span data-ttu-id="16696-128">WMI proporciona varias maneras diferentes de crear un espacio de nombres:</span><span class="sxs-lookup"><span data-stu-id="16696-128">WMI provides several different ways to create a namespace:</span></span>

-   [<span data-ttu-id="16696-129">Crear un espacio de nombres secundario con código MOF</span><span class="sxs-lookup"><span data-stu-id="16696-129">Creating a Child Namespace with MOF Code</span></span>](creating-a-child-namespace-with-mof-code.md)
-   [<span data-ttu-id="16696-130">Crear un espacio de nombres relacionado con código MOF</span><span class="sxs-lookup"><span data-stu-id="16696-130">Creating a Sibling Namespace with MOF Code</span></span>](creating-a-sibling-namespace-with-mof-code.md)
-   [<span data-ttu-id="16696-131">Crear un espacio de nombres con la API de WMI</span><span class="sxs-lookup"><span data-stu-id="16696-131">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a><span data-ttu-id="16696-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16696-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16696-133">Diseñar clases de Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="16696-133">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



