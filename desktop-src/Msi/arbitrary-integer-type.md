---
description: El tipo entero arbitrario de tipo semántico es uno de los tipos de formato entero.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Tipo de entero arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156340"
---
# <a name="arbitrary-integer-type"></a><span data-ttu-id="10c63-103">Tipo de entero arbitrario</span><span class="sxs-lookup"><span data-stu-id="10c63-103">Arbitrary Integer Type</span></span>

<span data-ttu-id="10c63-104">El tipo entero arbitrario de [tipo semántico](semantic-types.md) es uno de los [tipos de formato entero](integer-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="10c63-104">The Arbitrary Integer Type of [semantic type](semantic-types.md) is one of the [Integer Format Types](integer-format-types.md).</span></span> <span data-ttu-id="10c63-105">Este tipo de elemento configurable es un entero proporcionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="10c63-105">This type of configurable item is an integer provided by the user.</span></span> <span data-ttu-id="10c63-106">La herramienta de combinación sustituye este entero en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="10c63-106">The merge tool substitutes this integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="10c63-107">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "2" en la columna formato y dejar en blanco las columnas Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="10c63-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "2" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="10c63-108">Las columnas Type y ContextData están reservadas y deben ser null.</span><span class="sxs-lookup"><span data-stu-id="10c63-108">The Type and ContextData columns are reserved and must be null.</span></span>

 

 



