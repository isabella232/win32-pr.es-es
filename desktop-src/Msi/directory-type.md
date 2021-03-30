---
description: El tipo de directorio de tipo semántico es uno de los tipos de formato de clave, que consta de una clave externa en la tabla de directorios proporcionada por el usuario.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910954"
---
# <a name="directory-type"></a><span data-ttu-id="8e086-103">Tipo de directorio</span><span class="sxs-lookup"><span data-stu-id="8e086-103">Directory Type</span></span>

<span data-ttu-id="8e086-104">El tipo de directorio de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md), que consta de una clave externa en la tabla de [directorios](directory-table.md) proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8e086-104">The Directory Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md), which consists of a foreign key into the [Directory table](directory-table.md) provided by the user.</span></span>

<span data-ttu-id="8e086-105">La herramienta de combinación debe sustituir un [identificador](identifier.md) de Windows Installer válido para los elementos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="8e086-105">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="8e086-106">Mergemod.dll no aplica esta restricción y depende de la herramienta de combinación para asegurarse de que el usuario proporciona una clave válida en la tabla del directorio.</span><span class="sxs-lookup"><span data-stu-id="8e086-106">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Directory table.</span></span>

<span data-ttu-id="8e086-107">Un elemento configurable del tipo de directorio solo debe modificar el directorio de destino de la instalación y no modificar la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="8e086-107">A configurable item of the Directory type should only modify the destination directory of the installation and not modify the source image.</span></span> <span data-ttu-id="8e086-108">Por lo tanto, un elemento configurable de este tipo solo debe modificar las claves externas en la tabla del directorio y no modificar directamente la tabla de directorios.</span><span class="sxs-lookup"><span data-stu-id="8e086-108">A configurable item of this type should therefore only modify foreign keys to the Directory table and not modify the Directory table directly.</span></span>

<span data-ttu-id="8e086-109">Dado que la \_ columna de directorio de la [tabla de componentes](component-table.md) no acepta valores NULL, NULL es un valor no válido para un elemento configurable de este tipo aunque no se haya establecido msmConfigItemNonNullable en la columna Attributes.</span><span class="sxs-lookup"><span data-stu-id="8e086-109">Because the Directory\_ column of the [Component table](component-table.md) is non-nullable, null is an invalid value for a configurable item of this type even if the msmConfigItemNonNullable is not set in the Attributes column.</span></span>

<span data-ttu-id="8e086-110">El tipo de directorio se puede usar con dos tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="8e086-110">The Directory type may be used with two kinds of ContextData.</span></span>

<span data-ttu-id="8e086-111">**IsolationDirectory ContextData**</span><span class="sxs-lookup"><span data-stu-id="8e086-111">**IsolationDirectory ContextData**</span></span>

<span data-ttu-id="8e086-112">Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione un directorio de destino para los archivos del módulo.</span><span class="sxs-lookup"><span data-stu-id="8e086-112">A configurable merge module may use this type to enable the user to provide a destination directory for files in the module.</span></span> <span data-ttu-id="8e086-113">La herramienta de combinación sustituye el identificador del directorio en las plantillas de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="8e086-113">The merge tool substitutes the directory's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="8e086-114">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del directorio en la columna nombre, escribir "1" en la columna formato, escribir "directorio" en la columna tipo y escribir "IsolationDirectory" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="8e086-114">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "IsolationDirectory" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="8e086-115">**ShortcutLocation ContextData**</span><span class="sxs-lookup"><span data-stu-id="8e086-115">**ShortcutLocation ContextData**</span></span>

<span data-ttu-id="8e086-116">Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione un directorio de destino para los accesos directos en el módulo.</span><span class="sxs-lookup"><span data-stu-id="8e086-116">A configurable merge module may use this type to enable the user to provide a destination directory for shortcuts in the module.</span></span> <span data-ttu-id="8e086-117">La herramienta de combinación sustituye el identificador del acceso directo en las plantillas de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="8e086-117">The merge tool substitutes the shortcut's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="8e086-118">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del directorio en la columna nombre, escribir "1" en la columna formato, escribir "directorio" en la columna tipo y escribir "ShortcutLocation" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="8e086-118">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "ShortcutLocation" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



