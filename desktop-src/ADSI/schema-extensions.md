---
title: Extensiones de esquema
description: La arquitectura del esquema ADSI proporciona que las nuevas clases de esquema se pueden agregar al contenedor de clases de esquema y nuevas propiedades a un objeto de clase de esquema existente en tiempo de ejecución.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148731"
---
# <a name="schema-extensions"></a><span data-ttu-id="67b30-103">Extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="67b30-103">Schema Extensions</span></span>

<span data-ttu-id="67b30-104">La arquitectura del esquema ADSI proporciona que las nuevas clases de esquema se pueden agregar al contenedor de clases de esquema y nuevas propiedades a un objeto de clase de esquema existente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="67b30-104">The architecture of the ADSI schema provides that new schema classes can be added to the schema class container and new properties to an existing schema class object at run time.</span></span> <span data-ttu-id="67b30-105">Esta última capacidad no requiere ningún código nuevo.</span><span class="sxs-lookup"><span data-stu-id="67b30-105">The latter ability requires no new code.</span></span> <span data-ttu-id="67b30-106">Se trata de una característica importante para los espacios de nombres que permiten servicios de directorio extensibles.</span><span class="sxs-lookup"><span data-stu-id="67b30-106">This is an important feature for namespaces that allow extensible directory services.</span></span> <span data-ttu-id="67b30-107">El componente de proveedor debe permitir esta extensibilidad y saber dónde tener acceso y almacenar la instancia de clase y los valores de sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="67b30-107">The provider component must allow for this extensibility and know where to access and store the class instance and the values of its properties.</span></span> <span data-ttu-id="67b30-108">En un servicio de directorio extensible típico, esta información se almacena en la base de datos del servicio de directorio de la misma manera que cualquier otra clase de esquema y definiciones de propiedad.</span><span class="sxs-lookup"><span data-stu-id="67b30-108">In a typical extensible directory service, this information is stored in the directory service database in the same manner as any other schema class and property definitions.</span></span>

> [!Note]  
> <span data-ttu-id="67b30-109">En la terminología de la interfaz COM, solo se pueden agregar propiedades a una clase de esquema existente, no a métodos.</span><span class="sxs-lookup"><span data-stu-id="67b30-109">In COM interface terminology, only properties can be added to an existing schema class, not methods.</span></span> <span data-ttu-id="67b30-110">Para agregar un nuevo método, es necesario agregar una nueva implementación de ese método y, por tanto, requerir código adicional.</span><span class="sxs-lookup"><span data-stu-id="67b30-110">Adding a new method would require adding a new implementation of that method and thus require additional code.</span></span>

 

<span data-ttu-id="67b30-111">Para obtener un ejemplo de un esquema de proveedor específico, consulte [Administración de esquemas](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="67b30-111">For an example of a specific provider schema, see [Schema Management](schema-management.md).</span></span>

 

 




