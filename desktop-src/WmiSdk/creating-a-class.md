---
description: En WMI, una clase es un objeto que describe algún aspecto de una empresa, como un tipo especial de unidad de disco.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Crear una clase WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678343"
---
# <a name="creating-a-wmi-class"></a><span data-ttu-id="cdb65-103">Crear una clase WMI</span><span class="sxs-lookup"><span data-stu-id="cdb65-103">Creating a WMI Class</span></span>

<span data-ttu-id="cdb65-104">En WMI, una clase es un objeto que describe algún aspecto de una empresa, como un tipo especial de unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="cdb65-104">In WMI, a class is an object that describes some aspect of an enterprise, such as a special type of disk drive.</span></span> <span data-ttu-id="cdb65-105">Después de crear una definición de clase, escriba la DLL del proveedor para proporcionar instancias de la clase, los datos de propiedad y los métodos de ejecución definidos para la clase.</span><span class="sxs-lookup"><span data-stu-id="cdb65-105">After you have created a class definition, write your provider DLL to supply instances of the class, property data, and execute methods defined for the class.</span></span> <span data-ttu-id="cdb65-106">Los scripts y las aplicaciones pueden obtener datos o controlar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdb65-106">Scripts and applications can then obtain data or control the device.</span></span> <span data-ttu-id="cdb65-107">Para obtener más información, vea [desarrollar un proveedor WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cdb65-107">For more information, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="cdb65-108">Para asegurarse de que todas las definiciones de clases de WMI para objetos administrados se restauran en el [*repositorio de WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador de la instrucción [**\# pragma AUTORECOVER**](pragma-autorecover.md) en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="cdb65-108">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) statement preprocessor instruction in your MOF file.</span></span>

 

## <a name="base-class"></a><span data-ttu-id="cdb65-109">Clase base</span><span class="sxs-lookup"><span data-stu-id="cdb65-109">Base Class</span></span>

<span data-ttu-id="cdb65-110">Una clase base representa un concepto general.</span><span class="sxs-lookup"><span data-stu-id="cdb65-110">A base class represents some general concept.</span></span> <span data-ttu-id="cdb65-111">Por ejemplo, la clase [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) representa todos los tipos de unidades de CD-ROM en WMI y contiene propiedades generales que describen todos los tipos de unidades de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="cdb65-111">For example, the [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) class represents all types of CD-ROM drives in WMI, and contains general properties that describe all kinds of CD-ROM drives.</span></span> <span data-ttu-id="cdb65-112">Para obtener más información, vea [crear una clase base](creating-a-base-class.md).</span><span class="sxs-lookup"><span data-stu-id="cdb65-112">For more information, see [Creating a Base Class](creating-a-base-class.md).</span></span>

<span data-ttu-id="cdb65-113">Una clase derivada hereda propiedades y métodos de otra clase.</span><span class="sxs-lookup"><span data-stu-id="cdb65-113">A derived class inherits properties and methods from another class.</span></span> <span data-ttu-id="cdb65-114">Normalmente, una clase derivada representa un caso específico de una clase base.</span><span class="sxs-lookup"><span data-stu-id="cdb65-114">A derived class usually represents a specific case of a base class.</span></span> <span data-ttu-id="cdb65-115">Por ejemplo, la [**clase \_ CDROMDrive de Win32**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) representa una unidad de CD-ROM en un sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="cdb65-115">For example, the [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) class represents a CD-ROM drive on a Windows system.</span></span> <span data-ttu-id="cdb65-116">La **clase \_ CDROMDrive de Win32** se basa en y hereda muchas de las propiedades de [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span><span class="sxs-lookup"><span data-stu-id="cdb65-116">The **Win32\_CDROMDrive** class is based on and inherits many of properties from [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span></span> <span data-ttu-id="cdb65-117">Sin embargo, **Win32 \_ CDROMDrive**, al igual que otras clases derivadas, pueden tener propiedades adicionales que hacen que la clase derivada sea única.</span><span class="sxs-lookup"><span data-stu-id="cdb65-117">However, **Win32\_CDROMDrive**, like other derived classes, can have additional properties that make the derived class unique.</span></span> <span data-ttu-id="cdb65-118">Para obtener más información, vea [crear una clase derivada](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="cdb65-118">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

## <a name="properties-and-methods"></a><span data-ttu-id="cdb65-119">Propiedades y métodos</span><span class="sxs-lookup"><span data-stu-id="cdb65-119">Properties and Methods</span></span>

<span data-ttu-id="cdb65-120">Crear una clase significa definir las propiedades que describen esa clase.</span><span class="sxs-lookup"><span data-stu-id="cdb65-120">Creating a class means defining the properties that describe that class.</span></span> <span data-ttu-id="cdb65-121">También puede definir métodos que manipulen el objeto representado por la clase.</span><span class="sxs-lookup"><span data-stu-id="cdb65-121">You can also define methods that manipulate the object represented by the class.</span></span>

<span data-ttu-id="cdb65-122">Por lo general, una propiedad representa un aspecto del objeto, como un número de serie para un dispositivo o un tamaño en bytes para un proceso, mientras que un método representa una acción que cambia el estado o el comportamiento del dispositivo o de la entidad lógica.</span><span class="sxs-lookup"><span data-stu-id="cdb65-122">Generally, a property represents an aspect of the object, such as a serial number for a device or a size in bytes for a process, while a method represents an action that changes the state or behavior of the device or logical entity.</span></span>

<span data-ttu-id="cdb65-123">Cada clase debe tener al menos una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="cdb65-123">Each class must have at least one key property.</span></span> <span data-ttu-id="cdb65-124">Aunque una clase puede tener varias claves, no se puede crear una instancia de una clase con más de 256 claves.</span><span class="sxs-lookup"><span data-stu-id="cdb65-124">While a class may have multiple keys, you cannot create an instance of a class with more than 256 keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdb65-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cdb65-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdb65-126">Diseñar clases de Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="cdb65-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
