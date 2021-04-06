---
description: El tipo de enumeración de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Enum (tipo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001607"
---
# <a name="enum-type"></a><span data-ttu-id="c316e-103">Enum (tipo)</span><span class="sxs-lookup"><span data-stu-id="c316e-103">Enum Type</span></span>

<span data-ttu-id="c316e-104">El tipo de enumeración de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="c316e-104">The Enum Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="c316e-105">Este tipo consta de una cadena de texto elegida por el usuario a partir de un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="c316e-105">This type consists of a text string chosen by the user from a set of choices.</span></span> <span data-ttu-id="c316e-106">La herramienta de combinación sustituye la cadena seleccionada seleccionada en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="c316e-106">The merge tool substitutes the selected string selected into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="c316e-107">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escriba "0" en la columna formato, escriba "enum" en la columna tipo y escriba la lista de posibles cadenas en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="c316e-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Enum" into the Type column, and enter the list of possible strings in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="c316e-108">La lista de cadenas posibles se debe proporcionar como una lista de cadenas deliminated por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="c316e-108">The list of possible strings must be provided as a list of strings deliminated by semicolons.</span></span> <span data-ttu-id="c316e-109">Cada opción debe tener el formato "nombre = valor".</span><span class="sxs-lookup"><span data-stu-id="c316e-109">Each choice must be in the form "Name=Value".</span></span> <span data-ttu-id="c316e-110">Se puede Agregar un punto y coma literal al valor prefijando el punto y coma con un carácter de barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="c316e-110">A literal semicolon can be added to the value by prefixing the semicolon with a backslash character.</span></span> <span data-ttu-id="c316e-111">NULL es un valor válido a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c316e-111">Null is a valid value unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



