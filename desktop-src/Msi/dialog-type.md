---
description: El tipo de cuadro de diálogo de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave externa en la tabla de diálogo proporcionada por el usuario.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667800"
---
# <a name="dialog-type"></a><span data-ttu-id="8af3a-104">Tipo de diálogo</span><span class="sxs-lookup"><span data-stu-id="8af3a-104">Dialog Type</span></span>

<span data-ttu-id="8af3a-105">El tipo de cuadro de diálogo de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="8af3a-105">The Dialog Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="8af3a-106">Este tipo consta de una clave externa en la [tabla de diálogo](dialog-table.md) proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8af3a-106">This type consists of a foreign key into the [Dialog table](dialog-table.md) provided by the user.</span></span>

<span data-ttu-id="8af3a-107">La herramienta de combinación debe sustituir un [identificador](identifier.md) de Windows Installer válido para los elementos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="8af3a-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="8af3a-108">Mergemod.dll no aplica esta restricción y depende de la herramienta de combinación para asegurarse de que el usuario proporciona una clave válida en la tabla del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8af3a-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Dialog table.</span></span>

<span data-ttu-id="8af3a-109">NULL es un valor válido para este tipo a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="8af3a-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="8af3a-110">El tipo de cuadro de diálogo se puede usar con los siguientes tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="8af3a-110">The Dialog type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="8af3a-111">**DialogNext ContextData**</span><span class="sxs-lookup"><span data-stu-id="8af3a-111">**DialogNext ContextData**</span></span>

<span data-ttu-id="8af3a-112">Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa en la tabla del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8af3a-112">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="8af3a-113">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escriba "1" en la columna formato, escriba "cuadro de diálogo" en la columna tipo y escriba "DialogNext" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="8af3a-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogNext" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="8af3a-114">**DialogPrev ContextData**</span><span class="sxs-lookup"><span data-stu-id="8af3a-114">**DialogPrev ContextData**</span></span>

<span data-ttu-id="8af3a-115">Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa en la tabla del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8af3a-115">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="8af3a-116">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escriba "1" en la columna formato, escriba "cuadro de diálogo" en la columna tipo y escriba "DialogPrev" en la columna ContextData de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8af3a-116">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogPrev" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



