---
title: Clases auxiliares vinculadas dinámicamente
description: Una clase auxiliar vinculada dinámicamente es una clase que se adjunta a un objeto individual, en lugar de a una clase de objeto.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Clases auxiliares vinculadas dinámicamente AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268291"
---
# <a name="dynamically-linked-auxiliary-classes"></a><span data-ttu-id="86822-104">Clases auxiliares vinculadas dinámicamente</span><span class="sxs-lookup"><span data-stu-id="86822-104">Dynamically Linked Auxiliary Classes</span></span>

<span data-ttu-id="86822-105">Una clase auxiliar vinculada dinámicamente es una clase que se adjunta a un objeto individual, en lugar de a una clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="86822-105">A dynamically linked auxiliary class is a class that is attached to an individual object, rather than to an object class.</span></span> <span data-ttu-id="86822-106">La vinculación dinámica permite almacenar atributos adicionales con un objeto individual sin el impacto en todo el bosque de la extensión de la definición de esquema de una clase completa.</span><span class="sxs-lookup"><span data-stu-id="86822-106">Dynamic linking enables you to store additional attributes with an individual object without the forest-wide impact of extending the schema definition for an entire class.</span></span> <span data-ttu-id="86822-107">Por ejemplo, una empresa puede usar la vinculación dinámica para asociar una clase auxiliar específica de ventas a los objetos de usuario de sus vendedores y otras clases auxiliares específicas del Departamento a los objetos de usuario de los empleados de otros departamentos.</span><span class="sxs-lookup"><span data-stu-id="86822-107">For example, an enterprise could use dynamic linking to attach a sales-specific auxiliary class to the user objects of its sales people, and other department-specific auxiliary classes to the user objects of employees in other departments.</span></span>

<span data-ttu-id="86822-108">La vinculación dinámica no es compleja: agregue el nombre de la clase auxiliar a los valores del atributo **objectClass** de un objeto.</span><span class="sxs-lookup"><span data-stu-id="86822-108">Dynamic linking is not complex: add the name of the auxiliary class to the values of an object's **objectClass** attribute.</span></span> <span data-ttu-id="86822-109">Si la clase auxiliar tiene atributos obligatorios (**mustHave** o **systemMustHave**), debe establecerlos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="86822-109">If the auxiliary class has any mandatory attributes (**mustHave** or **systemMustHave**), you must set them at the same time.</span></span> <span data-ttu-id="86822-110">Para obtener más información y un ejemplo de código, vea [Agregar una clase auxiliar a una instancia de objeto](adding-an-auxiliary-class-to-an-object-instance.md).</span><span class="sxs-lookup"><span data-stu-id="86822-110">For more information and a code example, see [Adding an Auxiliary Class to an Object Instance](adding-an-auxiliary-class-to-an-object-instance.md).</span></span>

<span data-ttu-id="86822-111">Para quitar una clase auxiliar vinculada dinámicamente, borre los valores de todos los atributos de la clase auxiliar y, a continuación, quite el nombre de la clase auxiliar del atributo **objectClass** del objeto.</span><span class="sxs-lookup"><span data-stu-id="86822-111">To remove a dynamically linked auxiliary class, clear the values of all attributes from the auxiliary class, and then remove the name of the auxiliary class from the **objectClass** attribute of the object.</span></span>

<span data-ttu-id="86822-112">Si agrega dinámicamente una clase auxiliar que es una subclase de otra clase auxiliar, ambas clases auxiliares se agregan al objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="86822-112">If you dynamically add an auxiliary class that is a subclass of another auxiliary class, both auxiliary classes are added to the target object.</span></span> <span data-ttu-id="86822-113">Sin embargo, al quitar la clase auxiliar secundaria no se quita su elemento primario; cada clase se debe quitar explícitamente.</span><span class="sxs-lookup"><span data-stu-id="86822-113">However, removing the child auxiliary class does not remove its parent; each class must be explicitly removed.</span></span>

 

 




