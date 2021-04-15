---
description: Los siguientes códigos de error son específicos de la API de instalación.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Códigos de error (API de instalación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497903"
---
# <a name="error-codes-setup-api"></a><span data-ttu-id="80161-103">Códigos de error (API de instalación)</span><span class="sxs-lookup"><span data-stu-id="80161-103">Error Codes (Setup API)</span></span>

<span data-ttu-id="80161-104">Los siguientes códigos de error son específicos de la API de instalación.</span><span class="sxs-lookup"><span data-stu-id="80161-104">The following error codes are specific to the Setup API.</span></span>



| <span data-ttu-id="80161-105">Errores de análisis de INF</span><span class="sxs-lookup"><span data-stu-id="80161-105">INF Parsing Errors</span></span>              | <span data-ttu-id="80161-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="80161-106">Description</span></span>                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80161-107">ERROR \_ en \_ el nombre de sección esperado \_</span><span class="sxs-lookup"><span data-stu-id="80161-107">ERROR\_EXPECTED\_SECTION\_NAME</span></span>  | <span data-ttu-id="80161-108">Se esperaba un nombre de sección y no se encontró.</span><span class="sxs-lookup"><span data-stu-id="80161-108">A section name was expected and not found.</span></span>                                                                          |
| <span data-ttu-id="80161-109">ERROR \_ \_ en la \_ línea de nombre de sección incorrecta \_</span><span class="sxs-lookup"><span data-stu-id="80161-109">ERROR\_BAD\_SECTION\_NAME\_LINE</span></span> | <span data-ttu-id="80161-110">El nombre de la sección no tenía el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="80161-110">The section name was not of the correct format.</span></span> <span data-ttu-id="80161-111">(Por ejemplo, un nombre que no termina con un corchete de cierre ( \] ).</span><span class="sxs-lookup"><span data-stu-id="80161-111">(For example, a name not terminated by a right-hand bracket ( \] ).</span></span> |
| <span data-ttu-id="80161-112">nombre de sección de ERROR \_ \_ \_ demasiado \_ largo</span><span class="sxs-lookup"><span data-stu-id="80161-112">ERROR\_SECTION\_NAME\_TOO\_LONG</span></span> | <span data-ttu-id="80161-113">El nombre de sección superó la longitud máxima del nombre máximo de la sección longitud \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="80161-113">The section name exceeded the maximum length of MAX\_SECT\_NAME\_LEN.</span></span>                                               |
| <span data-ttu-id="80161-114">ERROR \_ General de \_ Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80161-114">ERROR\_GENERAL\_SYNTAX</span></span>          | <span data-ttu-id="80161-115">La sintaxis general es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="80161-115">The general syntax is incorrect.</span></span>                                                                                    |



 



| <span data-ttu-id="80161-116">Errores en tiempo de ejecución de INF</span><span class="sxs-lookup"><span data-stu-id="80161-116">INF Runtime Errors</span></span>         | <span data-ttu-id="80161-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="80161-117">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80161-118">ERROR \_ de \_ estilo INF incorrecto \_</span><span class="sxs-lookup"><span data-stu-id="80161-118">ERROR\_WRONG\_INF\_STYLE</span></span>   | <span data-ttu-id="80161-119">El archivo INF no es del tipo especificado en la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="80161-119">The INF file is not of the type specified in the function call.</span></span> <span data-ttu-id="80161-120">Por ejemplo, este error puede ser devuelto por la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) si el archivo INF estaba destinado a una versión anterior de Windows.</span><span class="sxs-lookup"><span data-stu-id="80161-120">For example, this error may be returned by the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function if the INF file was intended for an early version of Windows.</span></span> |
| <span data-ttu-id="80161-121">\_ \_ no \_ se encontró la sección de error</span><span class="sxs-lookup"><span data-stu-id="80161-121">ERROR\_SECTION\_NOT\_FOUND</span></span> | <span data-ttu-id="80161-122">No se encontró la sección en el archivo INF.</span><span class="sxs-lookup"><span data-stu-id="80161-122">The section was not found in the INF file.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="80161-123">\_ \_ no \_ se encontró la línea de error</span><span class="sxs-lookup"><span data-stu-id="80161-123">ERROR\_LINE\_NOT\_FOUND</span></span>    | <span data-ttu-id="80161-124">No se encontró la línea en la sección INF.</span><span class="sxs-lookup"><span data-stu-id="80161-124">The line was not found in the INF section.</span></span>                                                                                                                                                                                                     |



 

 

 



