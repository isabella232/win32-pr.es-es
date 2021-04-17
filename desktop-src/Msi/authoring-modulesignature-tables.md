---
description: La tabla ModuleSignature contiene toda la información necesaria para identificar el módulo de combinación.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Creación de tablas ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652610"
---
# <a name="authoring-modulesignature-tables"></a><span data-ttu-id="47dea-103">Creación de tablas ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="47dea-103">Authoring ModuleSignature Tables</span></span>

<span data-ttu-id="47dea-104">La [tabla ModuleSignature](modulesignature-table.md) contiene toda la información necesaria para identificar el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="47dea-104">The [ModuleSignature table](modulesignature-table.md) contains all the information needed to identify the merge module.</span></span>

<span data-ttu-id="47dea-105">El campo ModuleID es la clave principal de esta tabla y debe seguir la Convención descrita en [asignar nombres a las claves principales de las bases de datos del módulo de combinación](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="47dea-105">The ModuleID field is the primary key for this table and must follow the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="47dea-106">Por ejemplo, si el nombre legible del módulo de combinación es myLibrary y el GUID del módulo de combinación es {880DE2F0-CDD8-11D1-A849-006097ABDE17}, la entrada de la columna ModuleID de la tabla ModuleSignature se convierte en myLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.</span><span class="sxs-lookup"><span data-stu-id="47dea-106">For example, if the readable name of the merge module is MyLibrary and the GUID for the merge module is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column of the ModuleSignature table becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

<span data-ttu-id="47dea-107">Escriba el identificador decimal para el idioma predeterminado del módulo de combinación en el campo idioma de la tabla ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="47dea-107">Enter the decimal identifier for the default language of the merge module into the Language field of the ModuleSignature table.</span></span>

<span data-ttu-id="47dea-108">Escriba la versión del módulo de combinación en el campo versión.</span><span class="sxs-lookup"><span data-stu-id="47dea-108">Enter the version of the merge module into the Version field.</span></span>

 

 



