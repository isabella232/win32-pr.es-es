---
description: '&\# 0034; Bit de bits&\# 0034; tipo sin solicitudes de contexto que el usuario proporciona un entero cuyo valor se utiliza para establecer uno o varios bits en un campo de bits. Este texto puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos.'
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo de campo de bits arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156341"
---
# <a name="arbitrary-bitfield-type"></a><span data-ttu-id="47769-104">Tipo de campo de bits arbitrario</span><span class="sxs-lookup"><span data-stu-id="47769-104">Arbitrary Bitfield Type</span></span>

<span data-ttu-id="47769-105">El tipo "campo de bits" sin solicitudes de contexto que el usuario proporciona un entero cuyo valor se usa para establecer uno o varios bits en un campo de bits.</span><span class="sxs-lookup"><span data-stu-id="47769-105">The "Bitfield" type with no context requests that the user provide an integer whose value is used to set one or more bits in a bitfield.</span></span> <span data-ttu-id="47769-106">Este texto puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="47769-106">This text may be in any language compatible with the code page of the database.</span></span>

<span data-ttu-id="47769-107">El tipo de campo de bits arbitrario de [tipo semántico](semantic-types.md) es uno de los tipos de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="47769-107">The Arbitrary Bitfield Type of [semantic type](semantic-types.md) is one of the Bitfield Types.</span></span> <span data-ttu-id="47769-108">Este tipo consta de un entero elegido por el usuario a partir de un conjunto de opciones.</span><span class="sxs-lookup"><span data-stu-id="47769-108">This type consists of an integer chosen by the user from a set of choices.</span></span> <span data-ttu-id="47769-109">La herramienta de combinación sustituye el entero seleccionado en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="47769-109">The merge tool substitutes the selected integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="47769-110">Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento en la columna nombre, escriba "3" en la columna formato, deje la columna tipo en blanco y escriba la lista de enteros posibles en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="47769-110">To specify a configurable item of this type, module authors should enter the name of the item into the Name column, enter "3" into the Format column, leave the Type column blank, and enter the list of possible integers in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="47769-111">La columna de tipo está reservada y debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47769-111">The Type column is reserved and must be null.</span></span> <span data-ttu-id="47769-112">La entrada de la columna ContextData para todos los tipos de formato de campo de bits debe tener el formato " <mask> ;<Name>=</span><span class="sxs-lookup"><span data-stu-id="47769-112">The entry in the ContextData column for all Bitfield Format types must be in the form "<mask>;<Name>=</span></span><value><span data-ttu-id="47769-113">;<Name>=</span><span class="sxs-lookup"><span data-stu-id="47769-113">;<Name>=</span></span><value><span data-ttu-id="47769-114">.... ", donde <mask> es un valor entero que indica los bits de interés, <Name> es un nombre para mostrar localizable para la elección y</span><span class="sxs-lookup"><span data-stu-id="47769-114">....", where <mask> is an integer value indicating the bits of interest, <Name> is a localizable display name for the choice, and</span></span> <value> <span data-ttu-id="47769-115">es un valor entero decimal.</span><span class="sxs-lookup"><span data-stu-id="47769-115">is a decimal integer value.</span></span> <span data-ttu-id="47769-116">La columna de contexto está en uso en [formato especial CMsM](cmsm-special-format.md) y para todos los tipos de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="47769-116">The context column is in use [CMSM Special Format](cmsm-special-format.md) and for all bitfield types.</span></span> <span data-ttu-id="47769-117">Se puede escribir un carácter literal "=" o ";" en el <Name> campo anteponiendo un carácter de barra diagonal inversa (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="47769-117">A literal "=" or ";" character can be entered in the <Name> field by prefixing it with a backslash ('\\') character.</span></span>

 

 



