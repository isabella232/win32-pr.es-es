---
description: El tipo de identificador de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156328"
---
# <a name="identifier-type"></a><span data-ttu-id="ba0ac-103">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="ba0ac-103">Identifier Type</span></span>

<span data-ttu-id="ba0ac-104">El tipo de identificador de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="ba0ac-104">The Identifier Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="ba0ac-105">Este tipo consta de una cadena de texto proporcionada por el usuario en el formato de un [identificador](identifier.md)de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-105">This type consists of an text string provided by the user in the format of a Windows Installer [Identifier](identifier.md).</span></span> <span data-ttu-id="ba0ac-106">La herramienta de combinación sustituye esta cadena en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="ba0ac-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="ba0ac-107">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "0" en la columna formato, escribir "identificador" en la columna tipo y dejar en blanco la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Identifier" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="ba0ac-108">Vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="ba0ac-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="ba0ac-109">NULL es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Attributes de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



