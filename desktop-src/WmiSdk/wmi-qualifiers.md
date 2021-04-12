---
description: WMI tiene varios tipos de calificadores de clase y propiedad. Los calificadores también pueden tener modificaciones de tipos.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Calificadores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276111"
---
# <a name="wmi-qualifiers"></a><span data-ttu-id="1120d-104">Calificadores WMI</span><span class="sxs-lookup"><span data-stu-id="1120d-104">WMI Qualifiers</span></span>

<span data-ttu-id="1120d-105">WMI tiene varios tipos de [*calificadores*](gloss-q.md)de clase y propiedad.</span><span class="sxs-lookup"><span data-stu-id="1120d-105">WMI has several types of class and property [*qualifiers*](gloss-q.md).</span></span> <span data-ttu-id="1120d-106">Los calificadores también pueden tener modificaciones de [*tipos*](gloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="1120d-106">Qualifiers can also have modifying [*flavors*](gloss-f.md).</span></span> <span data-ttu-id="1120d-107">En WMI se usan los siguientes tipos de calificadores y sabores.</span><span class="sxs-lookup"><span data-stu-id="1120d-107">The following types of qualifiers and flavors are used in WMI.</span></span>

<span data-ttu-id="1120d-108">El nombre de cada calificador aparece con su tipo de datos y un indicador de si el calificador se puede aplicar a una clase, instancia, propiedad o método.</span><span class="sxs-lookup"><span data-stu-id="1120d-108">The name of each qualifier appears with its data type and an indicator of whether the qualifier can be applied to a class, instance, property, or method.</span></span> <span data-ttu-id="1120d-109">En el caso de los calificadores como la **Asociación** (descritos en [metacalificadores](meta-qualifiers.md)), hay una regla de uso implícita que también debe tener el calificador meta.</span><span class="sxs-lookup"><span data-stu-id="1120d-109">For qualifiers such as **Association** (discussed under [Meta Qualifiers](meta-qualifiers.md)), there is an implied usage rule that the meta qualifier must also be present.</span></span> <span data-ttu-id="1120d-110">Por ejemplo, la regla de uso implícita para los calificadores de **agregación** es que el calificador de **Asociación** también debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="1120d-110">For example, the implicit usage rule for the **Aggregation** qualifiers is that the **Association** qualifier must also be present.</span></span>



| <span data-ttu-id="1120d-111">Tipo de calificador</span><span class="sxs-lookup"><span data-stu-id="1120d-111">Qualifier type</span></span>                              | <span data-ttu-id="1120d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1120d-112">Description</span></span>                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1120d-113">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="1120d-113">Meta</span></span>](meta-qualifiers.md)                 | <span data-ttu-id="1120d-114">Refina la definición de las meta-construcciones aclarando el uso real de una declaración de clase o propiedad.</span><span class="sxs-lookup"><span data-stu-id="1120d-114">Refines the definition of meta-constructs by clarifying the actual usage of a class or property declaration.</span></span>                          |
| [<span data-ttu-id="1120d-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="1120d-115">Optional</span></span>](optional-qualifiers.md)         | <span data-ttu-id="1120d-116">Aborda situaciones que no son comunes a todas las implementaciones compatibles con CIM.</span><span class="sxs-lookup"><span data-stu-id="1120d-116">Addresses situations not common to all CIM-compliant implementations.</span></span>                                                                 |
| [<span data-ttu-id="1120d-117">Tipos de calificador</span><span class="sxs-lookup"><span data-stu-id="1120d-117">Qualifier Flavors</span></span>](qualifier-flavors.md)  | <span data-ttu-id="1120d-118">Proporciona más información sobre un calificador, como si una clase derivada o una instancia pueden reemplazar el valor original del calificador.</span><span class="sxs-lookup"><span data-stu-id="1120d-118">Provides more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span> |
| [<span data-ttu-id="1120d-119">Estándar</span><span class="sxs-lookup"><span data-stu-id="1120d-119">Standard</span></span>](standard-qualifiers.md)         | <span data-ttu-id="1120d-120">Admite las descripciones que todas las implementaciones compatibles con CIM deben controlar.</span><span class="sxs-lookup"><span data-stu-id="1120d-120">Supports the descriptions that all CIM-compliant implementations must handle.</span></span>                                                         |
| [<span data-ttu-id="1120d-121">Específico de WMI</span><span class="sxs-lookup"><span data-stu-id="1120d-121">WMI-specific</span></span>](wmi-specific-qualifiers.md) | <span data-ttu-id="1120d-122">Describe los calificadores específicos de WMI, como los calificadores de clase de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1120d-122">Describes qualifiers specific to WMI, such as performance counter class qualifiers.</span></span>                                                   |



 

<span data-ttu-id="1120d-123">Para obtener más información sobre cómo aplicar calificadores a las clases de WMI, vea [Agregar un calificador](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="1120d-123">For more information on applying qualifiers to your WMI classes, see [Adding a Qualifier](adding-a-qualifier.md).</span></span> <span data-ttu-id="1120d-124">Para ver cómo examinar los calificadores de clases WMI existentes, consulte el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="1120d-124">To see how to examine qualifiers on existing WMI classes, see the example code below.</span></span>

## <a name="example"></a><span data-ttu-id="1120d-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1120d-125">Example</span></span>

<span data-ttu-id="1120d-126">El siguiente código de PowerShell, tomado de la [Galería de TechNet](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), describe cómo recuperar calificadores de una clase WMI.</span><span class="sxs-lookup"><span data-stu-id="1120d-126">The following PowerShell code, taken from the [TechNet gallery](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), describes how to retrieve qualifiers from a WMI class.</span></span>


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 



