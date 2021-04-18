---
description: Los tipos de formato de clave de los datos configurables se pueden usar en campos de texto para proporcionar una clave en una tabla de base de datos.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Tipos de formato de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686805"
---
# <a name="key-format-types"></a><span data-ttu-id="999f8-103">Tipos de formato de clave</span><span class="sxs-lookup"><span data-stu-id="999f8-103">Key Format Types</span></span>

<span data-ttu-id="999f8-104">Los tipos de formato de clave de los datos configurables se pueden usar en campos de texto para proporcionar una clave en una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="999f8-104">The Key Format Types of configurable data may be used in text fields to provide a key into a database table.</span></span> <span data-ttu-id="999f8-105">El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo.</span><span class="sxs-lookup"><span data-stu-id="999f8-105">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="999f8-106">Null nunca es un valor válido para este tipo.</span><span class="sxs-lookup"><span data-stu-id="999f8-106">Null is never a valid value for this type.</span></span> <span data-ttu-id="999f8-107">Las respuestas a todos los elementos de formato de clave deben estar en [formato especial de CMsM](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="999f8-107">Responses to all Key format items must be in [CMSM Special Format](cmsm-special-format.md).</span></span>

<span data-ttu-id="999f8-108">Existen los siguientes tipos de formato de clave:</span><span class="sxs-lookup"><span data-stu-id="999f8-108">The following Key Format types exist:</span></span>

[<span data-ttu-id="999f8-109">Tipo de directorio</span><span class="sxs-lookup"><span data-stu-id="999f8-109">Directory Type</span></span>](directory-type.md)

[<span data-ttu-id="999f8-110">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="999f8-110">File Type</span></span>](file-type.md)

[<span data-ttu-id="999f8-111">Tipo de propiedad</span><span class="sxs-lookup"><span data-stu-id="999f8-111">Property Type</span></span>](property-type.md)

[<span data-ttu-id="999f8-112">Tipo de cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="999f8-112">Dialog Type</span></span>](dialog-type.md)

[<span data-ttu-id="999f8-113">Tipo binario</span><span class="sxs-lookup"><span data-stu-id="999f8-113">Binary Type</span></span>](binary-type.md)

[<span data-ttu-id="999f8-114">Tipo de icono</span><span class="sxs-lookup"><span data-stu-id="999f8-114">Icon Type</span></span>](icon-type.md)

<span data-ttu-id="999f8-115">Los elementos configurables del tipo de formato de clave se usan en las columnas de texto para proporcionar una clave de base de datos y, en general, podrían reemplazarse por cualquier cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="999f8-115">Configurable items of the Key Format Type are used in text columns to provide a database key and in general could be replaced by any text string.</span></span> <span data-ttu-id="999f8-116">Los tipos individuales pueden tener restricciones sintácticas adicionales, pero las restricciones no se aplican mediante Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="999f8-116">The individual types may have additional syntactic restrictions, but these restrictions are not enforced by Mergemod.dll.</span></span> <span data-ttu-id="999f8-117">Los elementos configurables concretos también pueden tener restricciones semánticas característicos.</span><span class="sxs-lookup"><span data-stu-id="999f8-117">Particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="999f8-118">Por ejemplo, puede ser necesario que un elemento configurable determinado sea una clave de la [tabla binaria](binary-table.md) en una fila que contenga una imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="999f8-118">For example, a particular configurable item may be required to be a key into the [Binary table](binary-table.md) to a row containing a bitmap image.</span></span> <span data-ttu-id="999f8-119">Estas restricciones no se aplican mediante Mergemod.dll y, por tanto, los autores de módulos deben estar preparados para controlar cualquier cadena que satisfaga el tipo de formato de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="999f8-119">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Key Format type.</span></span> <span data-ttu-id="999f8-120">A menos que se especifique lo contrario por los atributos o el significado semántico, NULL es una respuesta válida.</span><span class="sxs-lookup"><span data-stu-id="999f8-120">Unless otherwise specified by semantic meaning or attributes, null is a valid response.</span></span>

 

 



