---
description: La tabla CCPSearch contiene la lista de firmas de archivo que se usan para el programa de comprobación de cumplimiento (CCP). Al menos uno de estos archivos debe estar presente en el equipo de un usuario para que el usuario cumpla con el programa.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Tabla CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667005"
---
# <a name="ccpsearch-table"></a><span data-ttu-id="8e80f-104">Tabla CCPSearch</span><span class="sxs-lookup"><span data-stu-id="8e80f-104">CCPSearch Table</span></span>

<span data-ttu-id="8e80f-105">La tabla CCPSearch contiene la lista de firmas de archivo que se usan para el programa de comprobación de cumplimiento (CCP).</span><span class="sxs-lookup"><span data-stu-id="8e80f-105">The CCPSearch table contains the list of file signatures used for the Compliance Checking Program (CCP).</span></span> <span data-ttu-id="8e80f-106">Al menos uno de estos archivos debe estar presente en el equipo de un usuario para que el usuario cumpla con el programa.</span><span class="sxs-lookup"><span data-stu-id="8e80f-106">At least one of these files needs to be present on a user's computer for the user to be in compliance with the program.</span></span>

<span data-ttu-id="8e80f-107">La tabla CCPSearch tiene la siguiente columna.</span><span class="sxs-lookup"><span data-stu-id="8e80f-107">The CCPSearch table has the following column.</span></span>



| <span data-ttu-id="8e80f-108">Columna</span><span class="sxs-lookup"><span data-stu-id="8e80f-108">Column</span></span>      | <span data-ttu-id="8e80f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e80f-109">Type</span></span>                         | <span data-ttu-id="8e80f-110">Clave</span><span class="sxs-lookup"><span data-stu-id="8e80f-110">Key</span></span> | <span data-ttu-id="8e80f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="8e80f-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="8e80f-112">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="8e80f-112">Signature\_</span></span> | [<span data-ttu-id="8e80f-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="8e80f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="8e80f-114">Y</span><span class="sxs-lookup"><span data-stu-id="8e80f-114">Y</span></span>   | <span data-ttu-id="8e80f-115">N</span><span class="sxs-lookup"><span data-stu-id="8e80f-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="8e80f-116">Columna</span><span class="sxs-lookup"><span data-stu-id="8e80f-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="8e80f-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_</span><span class="sxs-lookup"><span data-stu-id="8e80f-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="8e80f-118">La firma \_ representa una firma de archivo única y también es la clave externa en las tablas [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)y [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8e80f-118">The Signature\_ represents a unique file signature and is also the external key into the [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e80f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e80f-119">Remarks</span></span>

<span data-ttu-id="8e80f-120">Se hace referencia a esta tabla cuando se ejecuta la acción [CCPSearch](ccpsearch-action.md) o la [acción RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8e80f-120">This table is referred to when the [CCPSearch action](ccpsearch-action.md) or the [RMCCPSearch action](rmccpsearch-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="8e80f-121">Validación</span><span class="sxs-lookup"><span data-stu-id="8e80f-121">Validation</span></span>

<dl>

[<span data-ttu-id="8e80f-122">ICE03</span><span class="sxs-lookup"><span data-stu-id="8e80f-122">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8e80f-123">ICE06</span><span class="sxs-lookup"><span data-stu-id="8e80f-123">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8e80f-124">ICE32</span><span class="sxs-lookup"><span data-stu-id="8e80f-124">ICE32</span></span>](ice32.md)  
</dl>

 

 



