---
description: El tipo de archivo de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave externa en la tabla de archivos proporcionada por el usuario.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668073"
---
# <a name="file-type"></a><span data-ttu-id="46d20-104">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="46d20-104">File Type</span></span>

<span data-ttu-id="46d20-105">El tipo de archivo de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="46d20-105">The File Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="46d20-106">Este tipo consta de una clave externa en la [tabla de archivos](file-table.md) proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="46d20-106">This type consists of a foreign key into the [File table](file-table.md) provided by the user.</span></span>

<span data-ttu-id="46d20-107">El tipo de archivo se puede usar con los siguientes tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="46d20-107">The File type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="46d20-108">**AssemblyContext ContextData**</span><span class="sxs-lookup"><span data-stu-id="46d20-108">**AssemblyContext ContextData**</span></span>

<span data-ttu-id="46d20-109">Este tipo se puede usar para permitir que los usuarios configuren claves externas para los ensamblados de Common Language Runtime o Win32.</span><span class="sxs-lookup"><span data-stu-id="46d20-109">This type may be used to enable users to configure foreign keys to Win32 or common language runtime assemblies.</span></span> <span data-ttu-id="46d20-110">La herramienta de fusión mediante combinación debe sustituir un [identificador](identifier.md) de Windows Installer para los elementos de este tipo en la plantilla de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="46d20-110">The merge tool must substitute a Windows Installer [Identifier](identifier.md) for items of this type into the template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="46d20-111">Mergemod.dll no lo exige y depende de la herramienta de fusión mediante combinación para asegurarse de que el usuario proporciona una clave válida en la tabla de archivos.</span><span class="sxs-lookup"><span data-stu-id="46d20-111">Mergemod.dll does not enforce this and it is up to the merge tool to ensure that the user provides a valid key into the File table.</span></span>

<span data-ttu-id="46d20-112">NULL es un valor válido para este tipo a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="46d20-112">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



