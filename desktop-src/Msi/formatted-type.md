---
description: El tipo con formato de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo con formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082336"
---
# <a name="formatted-type"></a><span data-ttu-id="52d48-103">Tipo con formato</span><span class="sxs-lookup"><span data-stu-id="52d48-103">Formatted Type</span></span>

<span data-ttu-id="52d48-104">El tipo con formato de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="52d48-104">The Formatted Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="52d48-105">Este tipo consta de una cadena de texto arbitraria de cualquier longitud proporcionada por el usuario y en el formato de texto con formato de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="52d48-105">This type consists of an arbitrary text string of any length provided by the user and in the Windows Installer formatted text format.</span></span> <span data-ttu-id="52d48-106">Para obtener más información, vea [con formato](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="52d48-106">For details, see [Formatted](formatted.md).</span></span> <span data-ttu-id="52d48-107">La herramienta de combinación sustituye esta cadena en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="52d48-107">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="52d48-108">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "0" en la columna formato, escribir "con formato" en la columna tipo y dejar en blanco la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="52d48-108">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Formatted" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="52d48-109">Para obtener más información, vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="52d48-109">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="52d48-110">NULL es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Attributes de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="52d48-110">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



