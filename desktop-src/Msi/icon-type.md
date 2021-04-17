---
description: El tipo de icono de tipo semántico es uno de los tipos de formato de clave. Este tipo se compone de una clave en la tabla de iconos proporcionada por el usuario.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Tipo de icono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652463"
---
# <a name="icon-type"></a><span data-ttu-id="57e35-104">Tipo de icono</span><span class="sxs-lookup"><span data-stu-id="57e35-104">Icon Type</span></span>

<span data-ttu-id="57e35-105">El tipo de icono de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="57e35-105">The Icon Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="57e35-106">Este tipo se compone de una clave en la [tabla de iconos](icon-table.md) proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="57e35-106">This type consists of a key into the [Icon table](icon-table.md) provided by the user.</span></span>

<span data-ttu-id="57e35-107">La herramienta de combinación debe sustituir un [identificador](identifier.md) de Windows Installer válido para los elementos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="57e35-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="57e35-108">Mergemod.dll no aplica esta restricción y depende de la herramienta de combinación para asegurarse de que el usuario proporciona una clave válida en la tabla de iconos.</span><span class="sxs-lookup"><span data-stu-id="57e35-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Icon table.</span></span>

<span data-ttu-id="57e35-109">NULL es un valor válido para este tipo a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="57e35-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="57e35-110">El tipo binario se puede utilizar con los siguientes tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="57e35-110">The Binary type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="57e35-111">**ShortcutIcon ContextData**</span><span class="sxs-lookup"><span data-stu-id="57e35-111">**ShortcutIcon ContextData**</span></span>

<span data-ttu-id="57e35-112">Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa a una fila de la [tabla de iconos](icon-table.md) que contenga una imagen adecuada para su uso como icono de acceso directo.</span><span class="sxs-lookup"><span data-stu-id="57e35-112">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the [Icon Table](icon-table.md) that contains an image suitable for use as a shortcut icon.</span></span> <span data-ttu-id="57e35-113">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escriba "1" en la columna formato, escriba "Icon" en la columna Type y escriba "ShorcutIcon" en la columna ContextData de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="57e35-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Icon" into the Type column, and enter "ShorcutIcon" into the ContextData column of the ModuleConfiguration table.</span></span> <span data-ttu-id="57e35-114">Este tipo no es adecuado para su uso en una tabla de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="57e35-114">This type is not appropriate for use in a user interface table.</span></span> <span data-ttu-id="57e35-115">Para modificar una clave a la tabla de iconos en estas tablas, vea el icono ContextData en [tipo binario](binary-type.md).</span><span class="sxs-lookup"><span data-stu-id="57e35-115">To modify a key to the Icon table in these tables see Icon ContextData under [Binary Type](binary-type.md).</span></span>

 

 



