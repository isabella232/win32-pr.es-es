---
description: Los tipos de formato de texto de los datos configurables pueden ser cadenas de texto de cualquier longitud. No se permiten valores NULL incrustados.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Tipos de formato de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653078"
---
# <a name="text-format-types"></a><span data-ttu-id="a45ce-104">Tipos de formato de texto</span><span class="sxs-lookup"><span data-stu-id="a45ce-104">Text Format Types</span></span>

<span data-ttu-id="a45ce-105">Los tipos de formato de texto de los datos configurables pueden ser cadenas de texto de cualquier longitud.</span><span class="sxs-lookup"><span data-stu-id="a45ce-105">The text format types of configurable data may be text strings of any length.</span></span> <span data-ttu-id="a45ce-106">No se permiten valores NULL incrustados.</span><span class="sxs-lookup"><span data-stu-id="a45ce-106">Embedded nulls are not allowed.</span></span>

<span data-ttu-id="a45ce-107">Existen los siguientes tipos de formato de texto:</span><span class="sxs-lookup"><span data-stu-id="a45ce-107">The following Text Format types exist:</span></span>

[<span data-ttu-id="a45ce-108">Texto arbitrario</span><span class="sxs-lookup"><span data-stu-id="a45ce-108">Arbitrary Text</span></span>](arbitrary-text-type.md)

[<span data-ttu-id="a45ce-109">RTF</span><span class="sxs-lookup"><span data-stu-id="a45ce-109">RTF</span></span>](rtf-type.md)

[<span data-ttu-id="a45ce-110">Formatea</span><span class="sxs-lookup"><span data-stu-id="a45ce-110">Formatted</span></span>](formatted-type.md)

[<span data-ttu-id="a45ce-111">Enum</span><span class="sxs-lookup"><span data-stu-id="a45ce-111">Enum</span></span>](enum-type.md)

[<span data-ttu-id="a45ce-112">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="a45ce-112">Identifier Type</span></span>](identifier-type.md)

<span data-ttu-id="a45ce-113">Los elementos configurables del tipo de formato de texto se utilizan en campos de base de datos no binarios y, en general, podrían reemplazarse por cualquier cadena de cualquier longitud.</span><span class="sxs-lookup"><span data-stu-id="a45ce-113">Configurable items of the Text Format Type are used in non-binary database fields and in general could be replaced by any string of any length.</span></span> <span data-ttu-id="a45ce-114">Sin embargo, los elementos configurables concretos también tienen restricciones semánticas.</span><span class="sxs-lookup"><span data-stu-id="a45ce-114">However, particular configurable items also have semantic restrictions.</span></span> <span data-ttu-id="a45ce-115">Por ejemplo, un elemento configurable que debe ser una clave externa en una tabla específica tiene restricciones semánticas adicionales.</span><span class="sxs-lookup"><span data-stu-id="a45ce-115">For example, a configurable item that is required to be a foreign key into a specific table has additional semantic restrictions.</span></span> <span data-ttu-id="a45ce-116">Las restricciones semánticas no se aplican mediante Mergemod.dll y, por tanto, los autores de módulos deben estar preparados para controlar cualquier cadena que satisfaga el tipo de formato de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="a45ce-116">Such semantic restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Text Format type.</span></span>

 

 



