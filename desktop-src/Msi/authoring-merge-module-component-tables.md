---
description: En cada módulo de combinación se requiere una tabla de componentes.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Crear tablas de componentes de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082545"
---
# <a name="authoring-merge-module-component-tables"></a><span data-ttu-id="745dc-103">Crear tablas de componentes de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="745dc-103">Authoring Merge Module Component Tables</span></span>

<span data-ttu-id="745dc-104">En cada módulo de combinación se requiere una [tabla de componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="745dc-104">A [Component table](component-table.md) is required in every merge module.</span></span> <span data-ttu-id="745dc-105">Esta tabla contiene un registro para cada componente entregado por el módulo de combinación en el archivo. msi de destino.</span><span class="sxs-lookup"><span data-stu-id="745dc-105">This table contains a record for each component delivered by the merge module to the target .msi file.</span></span> <span data-ttu-id="745dc-106">Tenga en cuenta que cada uno de estos componentes también debe especificarse en la [tabla ModuleComponents](modulecomponents-table.md) que se describe en [creación de tablas ModuleComponents](authoring-modulecomponents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="745dc-106">Note that each of these components must also be specified in the [ModuleComponents table](modulecomponents-table.md) described in [Authoring ModuleComponents Tables](authoring-modulecomponents-tables.md).</span></span>

<span data-ttu-id="745dc-107">Use la Convención de nomenclatura estándar al escribir nombres en la columna componente para asegurarse de que el identificador de cada componente es único para todos los módulos de combinación y bases de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="745dc-107">Use the standard naming convention when entering names into the Component column to ensure that the identifier for each component is unique for all merge modules and installation databases.</span></span> <span data-ttu-id="745dc-108">Para obtener más información, vea [asignar nombres a las claves principales en las bases de datos de módulos de combinación](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="745dc-108">For more information, see [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="745dc-109">Complete los campos restantes en cada registro, tal como se describe en una base de datos de instalación en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="745dc-109">Complete the remaining fields in each record as described for an installation database in [Component table](component-table.md).</span></span> <span data-ttu-id="745dc-110">Los componentes que se agregan a un paquete mediante un módulo de combinación deben cumplir las directrices de los componentes de Windows Installer válidos que se describen en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="745dc-110">The components added to a package by a merge module must adhere to the guidelines for valid Windows Installer Components described in the following sections:</span></span>

-   [<span data-ttu-id="745dc-111">Componentes de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="745dc-111">Windows Installer Components</span></span>](windows-installer-components.md)
-   [<span data-ttu-id="745dc-112">Organizar aplicaciones en componentes</span><span class="sxs-lookup"><span data-stu-id="745dc-112">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)

 

 



