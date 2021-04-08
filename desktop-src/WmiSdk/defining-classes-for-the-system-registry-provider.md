---
description: Una aplicación de administración que utiliza el proveedor del registro del sistema puede definir clases con propiedades que representan los datos del registro para claves concretas y, a continuación, almacena las clases en el repositorio WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definir clases para el proveedor del registro del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002516"
---
# <a name="defining-classes-for-the-system-registry-provider"></a><span data-ttu-id="adca8-103">Definir clases para el proveedor del registro del sistema</span><span class="sxs-lookup"><span data-stu-id="adca8-103">Defining Classes for the System Registry Provider</span></span>

<span data-ttu-id="adca8-104">Una aplicación de administración que utiliza el proveedor del registro del sistema puede definir clases con propiedades que representan los datos del registro para claves concretas y, a continuación, almacena las clases en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="adca8-104">A management application using the System Registry provider can define classes with properties that represent registry data for particular keys and then stores the classes in the WMI repository.</span></span> <span data-ttu-id="adca8-105">La mayoría de los procesos para definir una clase para el registro del sistema son idénticos a la definición de cualquier otra clase.</span><span class="sxs-lookup"><span data-stu-id="adca8-105">Most of the processes for defining a class for the system registry is identical to defining any other class.</span></span> <span data-ttu-id="adca8-106">Sin embargo, el proveedor del registro del sistema requiere que se utilicen tipos de datos y calificadores específicos.</span><span class="sxs-lookup"><span data-stu-id="adca8-106">However, the System Registry provider requires that you use specific data types and qualifiers.</span></span>

<span data-ttu-id="adca8-107">En el procedimiento siguiente se describe cómo definir una clase para el proveedor del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="adca8-107">The following procedure describes how to define a class for the System Registry provider.</span></span>

<span data-ttu-id="adca8-108">**Para definir una clase para el proveedor del registro del sistema**</span><span class="sxs-lookup"><span data-stu-id="adca8-108">**To define a class for the System Registry provider**</span></span>

1.  <span data-ttu-id="adca8-109">Cree la clase como lo haría con cualquier otra clase.</span><span class="sxs-lookup"><span data-stu-id="adca8-109">Create the class as you would any other class.</span></span>

    <span data-ttu-id="adca8-110">Para obtener más información, vea [crear una clase](creating-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="adca8-110">For more information, see [Creating a Class](creating-a-class.md).</span></span>

2.  <span data-ttu-id="adca8-111">Asigne los tipos de datos del registro adecuados a los tipos de WMI adecuados.</span><span class="sxs-lookup"><span data-stu-id="adca8-111">Map the appropriate registry data types to the appropriate WMI types.</span></span>

    <span data-ttu-id="adca8-112">El proveedor del registro del sistema asigna los tipos de datos del registro a tipos de datos WMI específicos.</span><span class="sxs-lookup"><span data-stu-id="adca8-112">The System Registry provider maps the registry data types to specific WMI data types.</span></span> <span data-ttu-id="adca8-113">Para obtener más información, vea [asignar un tipo de datos del registro a un tipo de datos de WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="adca8-113">For more information, see [Mapping a Registry Data Type to a WMI Data Type](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span></span>

3.  <span data-ttu-id="adca8-114">Use los calificadores necesarios para definir la ubicación del proveedor del registro y la ubicación de la clave del registro adecuada.</span><span class="sxs-lookup"><span data-stu-id="adca8-114">Use the required qualifiers to define the location of the Registry provider and the location of the appropriate registry key.</span></span>

    <span data-ttu-id="adca8-115">El proveedor del registro del sistema usa tres calificadores para definir la ubicación de varias clases, proveedores y entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="adca8-115">The System Registry provider uses three qualifiers to define the location of various classes, providers, and registry entries.</span></span> <span data-ttu-id="adca8-116">Para obtener más información, vea [definir una clase de registro con calificadores](defining-a-registry-class-with-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="adca8-116">For more information, see [Defining a Registry Class With Qualifiers](defining-a-registry-class-with-qualifiers.md).</span></span>

 

 



