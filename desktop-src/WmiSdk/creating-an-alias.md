---
description: Un alias en WMI es una referencia simbólica en una clase o una instancia de clase ubicada en otro lugar de un archivo Managed Object Format (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Creación de un alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706172"
---
# <a name="creating-a-wmi-alias"></a><span data-ttu-id="33462-103">Creación de un alias WMI</span><span class="sxs-lookup"><span data-stu-id="33462-103">Creating a WMI Alias</span></span>

<span data-ttu-id="33462-104">Un [*alias*](gloss-a.md) en WMI es una referencia simbólica en una clase o una instancia de clase ubicada en otro lugar de un archivo Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="33462-104">An [*alias*](gloss-a.md) in WMI is a symbolic reference in either a class or a class instance located elsewhere in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="33462-105">El compilador MOF utiliza alias para establecer referencias entre clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="33462-105">The MOF compiler uses aliases to establish references between classes and instances.</span></span> <span data-ttu-id="33462-106">El compilador resuelve los alias de las clases a las que hacen referencia, por lo que los nombres de alias no están disponibles en el código compilado.</span><span class="sxs-lookup"><span data-stu-id="33462-106">The compiler resolves aliases to the classes to which they refer, so alias names are not available in compiled code.</span></span> <span data-ttu-id="33462-107">Como resultado, las aplicaciones cliente no pueden hacer referencia a clases mediante alias.</span><span class="sxs-lookup"><span data-stu-id="33462-107">As a result, client applications cannot refer to classes using aliases.</span></span>

> [!Note]  
> <span data-ttu-id="33462-108">WMI admite referencias hacia delante, pero no alias circulares.</span><span class="sxs-lookup"><span data-stu-id="33462-108">WMI supports forward referencing but not circular aliases.</span></span>

 

<span data-ttu-id="33462-109">Un alias solo tiene ámbito dentro del archivo MOF en el que se declara el alias.</span><span class="sxs-lookup"><span data-stu-id="33462-109">An alias has scope only within the MOF file in which you declare the alias.</span></span> <span data-ttu-id="33462-110">Por lo tanto, normalmente se usa un alias como método abreviado para una ruta de acceso de objeto larga.</span><span class="sxs-lookup"><span data-stu-id="33462-110">Therefore, you typically use an alias as a shortcut to a lengthy object path.</span></span>

<span data-ttu-id="33462-111">**Para definir un alias**</span><span class="sxs-lookup"><span data-stu-id="33462-111">**To define an alias**</span></span>

1.  <span data-ttu-id="33462-112">Agregue la frase "as $*aliasname*" a la declaración de instancia o clase.</span><span class="sxs-lookup"><span data-stu-id="33462-112">Add the phrase "as $*aliasname*" to the instance or class declaration.</span></span>
2.  <span data-ttu-id="33462-113">Los nombres de alias siguen las mismas reglas que los nombres de instancia y clase, excepto en que los nombres de alias deben comenzar con un signo de dólar ($).</span><span class="sxs-lookup"><span data-stu-id="33462-113">Alias names follow the same rules as instance and class names, except that alias names must begin with a dollar sign ($).</span></span> <span data-ttu-id="33462-114">Los caracteres de subrayado pueden aparecer en un nombre de alias después del carácter inicial.</span><span class="sxs-lookup"><span data-stu-id="33462-114">Underscores can appear in an alias name following the initial character.</span></span>

<span data-ttu-id="33462-115">En el ejemplo de código siguiente se describe cómo usar un alias en una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="33462-115">The following code example describes how to use an alias in a class definition.</span></span>

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

<span data-ttu-id="33462-116">Los siguientes ejemplos de código describen cómo usar un alias como referencia simbólica a una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="33462-116">The following code examples describe how to use an alias as a symbolic reference to an object path.</span></span> <span data-ttu-id="33462-117">En estos ejemplos se declaran dos clases para describir un disco: la clase Disk para indicar la letra de unidad y la clase DiskRef para indicar la ruta de acceso del disco.</span><span class="sxs-lookup"><span data-stu-id="33462-117">These examples declare two classes to describe a disk: the Disk class to indicate the drive letter and the DiskRef class to indicate the disk path.</span></span> <span data-ttu-id="33462-118">Se define un alias para la instancia de clase de disco.</span><span class="sxs-lookup"><span data-stu-id="33462-118">An alias is defined for the Disk class instance.</span></span> <span data-ttu-id="33462-119">Este alias se usa como el valor de la propiedad PathToDisk en la instancia de DiskRef.</span><span class="sxs-lookup"><span data-stu-id="33462-119">This alias is used as the value for the PathToDisk property in the DiskRef instance.</span></span>

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a><span data-ttu-id="33462-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33462-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33462-121">Crear una clase</span><span class="sxs-lookup"><span data-stu-id="33462-121">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



