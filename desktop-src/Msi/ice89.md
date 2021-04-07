---
description: ICE89 valida que el valor de la \_ columna primaria ProgID de la tabla ProgID sea una clave externa válida en la columna ProgID de la tabla ProgID. Cada ProgId primario debe tener un registro en la tabla ProgId.
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d14ec5b17a20b9046625feb464865bd0c08419e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002695"
---
# <a name="ice89"></a><span data-ttu-id="bdac1-104">ICE89</span><span class="sxs-lookup"><span data-stu-id="bdac1-104">ICE89</span></span>

<span data-ttu-id="bdac1-105">ICE89 valida que el valor de la \_ columna primaria ProgID de la [tabla ProgID](progid-table.md) sea una clave externa válida en la columna ProgID de la tabla ProgID.</span><span class="sxs-lookup"><span data-stu-id="bdac1-105">ICE89 validates that the value in the Progid\_Parent column in [ProgId table](progid-table.md) is a valid foreign key into the ProgId column in ProgId table.</span></span> <span data-ttu-id="bdac1-106">Cada ProgId primario debe tener un registro en la tabla ProgId.</span><span class="sxs-lookup"><span data-stu-id="bdac1-106">Every ProgId parent should have a record in the ProgId table.</span></span>

## <a name="result"></a><span data-ttu-id="bdac1-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="bdac1-107">Result</span></span>

<span data-ttu-id="bdac1-108">ICE89 expone los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="bdac1-108">ICE89 posts the following errors.</span></span>



| <span data-ttu-id="bdac1-109">Error ICE89</span><span class="sxs-lookup"><span data-stu-id="bdac1-109">ICE89 error</span></span>                                                           | <span data-ttu-id="bdac1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdac1-110">Description</span></span>                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="bdac1-111">El \_ elemento primario ProgID ' \[ 1 \] ' de la tabla ProgID no es un ProgID válido.</span><span class="sxs-lookup"><span data-stu-id="bdac1-111">The ProgId\_Parent '\[1\]' in the ProgId table is not a valid ProgId.</span></span> | <span data-ttu-id="bdac1-112">Hay un elemento primario ProgId especificado que no aparece en la tabla ProgId.</span><span class="sxs-lookup"><span data-stu-id="bdac1-112">There is a ProgId parent specified that is not listed in the ProgId table.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bdac1-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bdac1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdac1-114">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="bdac1-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



