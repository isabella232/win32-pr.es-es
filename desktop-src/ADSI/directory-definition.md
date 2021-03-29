---
title: Definición de directorio
description: El componente de proveedor de ejemplo usa un diseño de directorio relativamente sencillo para clarificar la relación entre los componentes y mostrar los requisitos mínimos necesarios para ser un proveedor ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903064"
---
# <a name="directory-definition"></a><span data-ttu-id="5e5e7-103">Definición de directorio</span><span class="sxs-lookup"><span data-stu-id="5e5e7-103">Directory Definition</span></span>

<span data-ttu-id="5e5e7-104">El componente de proveedor de ejemplo usa un diseño de directorio relativamente sencillo para clarificar la relación entre los componentes y mostrar los requisitos mínimos necesarios para ser un proveedor ADSI.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-104">The example provider component uses a relatively simple directory design to clarify the relationship between components and to show the minimum requirements necessary to be an ADSI provider.</span></span>

<span data-ttu-id="5e5e7-105">El "directorio" del componente de proveedor de ejemplo consta de dos nodos raíz: "Seattle" y "Toronto".</span><span class="sxs-lookup"><span data-stu-id="5e5e7-105">The "directory" for the example provider component consists of two root nodes: "Seattle" and "Toronto".</span></span> <span data-ttu-id="5e5e7-106">Seattle contiene dos subnivels más, "Bellevue" y "Redmond".</span><span class="sxs-lookup"><span data-stu-id="5e5e7-106">Seattle contains two more sublevels, "Bellevue" and "Redmond".</span></span> <span data-ttu-id="5e5e7-107">Cada una de estas entradas contiene varias cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-107">Each of these entries contains several user accounts.</span></span> <span data-ttu-id="5e5e7-108">La entrada "Toronto" no tiene más subniveles, pero contiene directamente varias cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-108">The "Toronto" entry has no further sublevels, but directly contains several user accounts.</span></span> <span data-ttu-id="5e5e7-109">En la siguiente ilustración se muestran estos dos nodos raíz conectados a una red.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-109">The following figure shows these two root nodes connected to a network.</span></span>

![definición de directorio](images/dssmdo.png)

<span data-ttu-id="5e5e7-111">En términos jerárquicos, el nodo de espacio de nombres contiene "Seattle" y "Toronto".</span><span class="sxs-lookup"><span data-stu-id="5e5e7-111">In hierarchical terms, the Namespace node contains "Seattle" and "Toronto".</span></span> <span data-ttu-id="5e5e7-112">"Seattle" contiene "Bellevue" y "Redmond".</span><span class="sxs-lookup"><span data-stu-id="5e5e7-112">"Seattle" contains "Bellevue" and "Redmond".</span></span> <span data-ttu-id="5e5e7-113">"Bellevue" y "Redmond" contienen un conjunto de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-113">"Bellevue" and "Redmond" each contain a set of user accounts.</span></span> <span data-ttu-id="5e5e7-114">"Toronto" contiene directamente las cuentas de usuario sin nodos intermedios de la organización.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-114">"Toronto" directly contains the user accounts with no intermediate organizational nodes.</span></span>

<span data-ttu-id="5e5e7-115">El componente de proveedor de ejemplo representa esta estructura con solo dos tipos de objeto Active Directory: un objeto contenedor y un objeto hoja.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-115">The example provider component represents this structure with only two Active Directory object types: a container object and a leaf object.</span></span> <span data-ttu-id="5e5e7-116">"Seattle", "Toronto", "Bellevue" y "Redmond" son objetos contenedores y cada cuenta de usuario es un objeto hoja.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-116">"Seattle", "Toronto", "Bellevue", and "Redmond" are container objects and each user account is a leaf object.</span></span>

<span data-ttu-id="5e5e7-117">El componente proveedor de ejemplo crea una clase de esquema denominada "unidad organizativa" para un tipo de objeto contenedor y una clase de esquema denominada "usuario" para una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-117">The example provider component creates a schema class called "Organizational Unit" for a container object type and a schema class called "User" for a user account.</span></span>

<span data-ttu-id="5e5e7-118">Las propiedades de cada clase de esquema, sus métodos y las reglas que rigen las relaciones de contención de estos objetos se definen en la [Administración de esquemas](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="5e5e7-118">The properties for each schema class, their methods, and the rules that govern the containment relationships for these objects are all defined in [Schema Management](schema-management.md).</span></span>

 

 




