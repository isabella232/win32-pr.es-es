---
description: La palabra clave Ref de MOF describe una ruta de acceso de objeto y se asigna a un \_ tipo de automatización VT BSTR.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Referencias (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911205"
---
# <a name="references-wmi"></a><span data-ttu-id="ad4bd-103">Referencias (WMI)</span><span class="sxs-lookup"><span data-stu-id="ad4bd-103">References (WMI)</span></span>

<span data-ttu-id="ad4bd-104">La palabra clave **ref** de MOF describe una ruta de acceso de objeto y se asigna a un \_ tipo de automatización VT BSTR.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-104">The MOF **ref** key word describes an object path and maps to a VT\_BSTR Automation type.</span></span> <span data-ttu-id="ad4bd-105">La ruta de acceso del objeto puede ser una ruta de acceso completa a un servidor y un espacio de nombres, o una ruta de acceso relativa a otro objeto en el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-105">The object path can be either a full path to a server and namespace, or a relative path to another object in the same namespace.</span></span> <span data-ttu-id="ad4bd-106">Puede usar una palabra clave **ref** para vincular dos o más clases.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-106">You can use a **ref** key word to link two or more classes together.</span></span> <span data-ttu-id="ad4bd-107">WMI admite dos tipos de rutas de acceso de objeto, que se utilizan para definir rutas de acceso generales o específicas en WMI.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-107">WMI supports two types of object paths, which use to define general or specific paths within WMI.</span></span>

<span data-ttu-id="ad4bd-108">El propósito principal de la palabra clave **ref** es reducir el tiempo de transporte y la codificación entre los objetos que existen completamente dentro del repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-108">The main purpose of the **ref** key word is to reduce transport time and encoding between objects that exist entirely within the WMI repository.</span></span> <span data-ttu-id="ad4bd-109">También puede usar la palabra clave **ref** para crear una asociación entre dos clases.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-109">You can also use the **ref** key word to create an association between two classes.</span></span> <span data-ttu-id="ad4bd-110">Para obtener más información, vea [declarar una clase de asociación](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="ad4bd-110">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span> <span data-ttu-id="ad4bd-111">Si el elemento al que se hace referencia se encuentra en el mismo archivo MOF, utilice un alias para inicializar el valor de **referencia** .</span><span class="sxs-lookup"><span data-stu-id="ad4bd-111">If the referenced item is located within the same MOF file, use an alias to initialize the **ref** value.</span></span> <span data-ttu-id="ad4bd-112">Para obtener más información, vea [crear un alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="ad4bd-112">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

> [!Note]  
> <span data-ttu-id="ad4bd-113">Cuando se aplica una palabra de clave de **referencia** a una propiedad de clave, puede distinguir las referencias de objeto por el valor de cadena de objeto en lugar de por el valor desreferenciado.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-113">When a **ref** key word is applied to a key property, you can distinguish object references by the object string value instead of by the dereferenced value.</span></span>

 

<span data-ttu-id="ad4bd-114">MOF admite el concepto de una ruta de objeto fuertemente tipada y fuertemente tipada.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-114">MOF supports the concept of a weakly typed and strongly typed object path.</span></span> <span data-ttu-id="ad4bd-115">Una ruta de acceso de objeto débilmente tipada apunta a un objeto de una clase no especificada y utiliza la palabra clave **ref** con la palabra clave [Object](object.md) .</span><span class="sxs-lookup"><span data-stu-id="ad4bd-115">A weakly typed object path points to an object of an unspecified class and uses the **ref** key word with the [OBJECT](object.md) keyword.</span></span> <span data-ttu-id="ad4bd-116">Un objeto fuertemente tipado apunta a un objeto de una clase específica y usa **ref** con el nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="ad4bd-116">A strongly typed object points to an object of a specific class and uses **ref** with the class name.</span></span> <span data-ttu-id="ad4bd-117">En el ejemplo siguiente se describe una referencia de **RefToAnyClass** débilmente tipada que puede apuntar a cualquier clase o instancia de clase, y una referencia **RefToClassX** que solo puede apuntar a una instancia o clase **ClassX** :</span><span class="sxs-lookup"><span data-stu-id="ad4bd-117">The following example describes a weakly typed **RefToAnyClass** reference that can point to any class or class instance, and a **RefToClassX** reference that can point only to a **ClassX** class or instance:</span></span>

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

<span data-ttu-id="ad4bd-118">En el ejemplo siguiente se describen dos instancias y un objeto Association que hace referencia a las instancias anteriores:</span><span class="sxs-lookup"><span data-stu-id="ad4bd-118">The following example describes two instances and an association object that references the previous instances:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



