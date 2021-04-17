---
description: El tipo de texto arbitrario de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo de texto arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667043"
---
# <a name="arbitrary-text-type"></a><span data-ttu-id="d77fe-103">Tipo de texto arbitrario</span><span class="sxs-lookup"><span data-stu-id="d77fe-103">Arbitrary Text Type</span></span>

<span data-ttu-id="d77fe-104">El tipo de texto arbitrario de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="d77fe-104">The Arbitrary Text Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="d77fe-105">Este tipo consta de una cadena de texto arbitraria de cualquier longitud proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d77fe-105">This type consists of an arbitrary text string of any length provided by the user.</span></span> <span data-ttu-id="d77fe-106">La herramienta de combinación sustituye esta cadena arbitraria a las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="d77fe-106">The merge tool substitutes this arbitrary string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="d77fe-107">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "0" en la columna formato y dejar en blanco las columnas Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena de texto arbitraria puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d77fe-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).The arbitrary text string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="d77fe-108">Para obtener más información, vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="d77fe-108">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="d77fe-109">NULL es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Attributes de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d77fe-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



