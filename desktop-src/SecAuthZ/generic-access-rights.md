---
description: Los objetos protegibles utilizan un formato de máscara de acceso en el que los cuatro bits de orden superior especifican derechos de acceso genéricos.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Derechos de acceso genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816022"
---
# <a name="generic-access-rights"></a><span data-ttu-id="03e8c-103">Derechos de acceso genéricos</span><span class="sxs-lookup"><span data-stu-id="03e8c-103">Generic Access Rights</span></span>

<span data-ttu-id="03e8c-104">Los objetos protegibles utilizan un [formato de máscara de acceso](access-mask-format.md) en el que los cuatro bits de orden superior especifican derechos de acceso genéricos.</span><span class="sxs-lookup"><span data-stu-id="03e8c-104">Securable objects use an [access mask format](access-mask-format.md) in which the four high-order bits specify generic access rights.</span></span> <span data-ttu-id="03e8c-105">Cada tipo de objeto protegible asigna estos bits a un conjunto de sus derechos de acceso estándar y específicos del objeto.</span><span class="sxs-lookup"><span data-stu-id="03e8c-105">Each type of securable object maps these bits to a set of its standard and object-specific access rights.</span></span> <span data-ttu-id="03e8c-106">Por ejemplo, un objeto de archivo de Windows asigna el \_ bit de lectura genérico al control de lectura \_ y sincroniza los derechos de acceso estándar, así como los \_ \_ \_ \_ \_ \_ derechos de acceso de archivo lectura de datos, archivo de escritura EA y lectura de archivos.</span><span class="sxs-lookup"><span data-stu-id="03e8c-106">For example, a Windows file object maps the GENERIC\_READ bit to the READ\_CONTROL and SYNCHRONIZE standard access rights and to the FILE\_READ\_DATA, FILE\_READ\_EA, and FILE\_READ\_ATTRIBUTES object-specific access rights.</span></span> <span data-ttu-id="03e8c-107">Otros tipos de objetos asignan el \_ bit de lectura genérico a cualquier conjunto de derechos de acceso adecuado para ese tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="03e8c-107">Other types of objects map the GENERIC\_READ bit to whatever set of access rights is appropriate for that type of object.</span></span>

<span data-ttu-id="03e8c-108">Puede usar derechos de acceso genéricos para especificar el tipo de acceso que necesita al abrir un identificador de un objeto.</span><span class="sxs-lookup"><span data-stu-id="03e8c-108">You can use generic access rights to specify the type of access you need when you are opening a handle to an object.</span></span> <span data-ttu-id="03e8c-109">Normalmente es más sencillo que especificar todos los derechos estándar y específicos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="03e8c-109">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span>

<span data-ttu-id="03e8c-110">En la tabla siguiente se muestran las constantes definidas para los derechos de acceso genéricos.</span><span class="sxs-lookup"><span data-stu-id="03e8c-110">The following table shows the constants defined for the generic access rights.</span></span>



| <span data-ttu-id="03e8c-111">Constante</span><span class="sxs-lookup"><span data-stu-id="03e8c-111">Constant</span></span>         | <span data-ttu-id="03e8c-112">Significado genérico</span><span class="sxs-lookup"><span data-stu-id="03e8c-112">Generic meaning</span></span>            |
|------------------|----------------------------|
| <span data-ttu-id="03e8c-113">todos GENÉRICOs \_</span><span class="sxs-lookup"><span data-stu-id="03e8c-113">GENERIC\_ALL</span></span>     | <span data-ttu-id="03e8c-114">Todos los derechos de acceso posibles</span><span class="sxs-lookup"><span data-stu-id="03e8c-114">All possible access rights</span></span> |
| <span data-ttu-id="03e8c-115">\_ejecución genérica</span><span class="sxs-lookup"><span data-stu-id="03e8c-115">GENERIC\_EXECUTE</span></span> | <span data-ttu-id="03e8c-116">Ejecutar acceso</span><span class="sxs-lookup"><span data-stu-id="03e8c-116">Execute access</span></span>             |
| <span data-ttu-id="03e8c-117">\_lectura genérica</span><span class="sxs-lookup"><span data-stu-id="03e8c-117">GENERIC\_READ</span></span>    | <span data-ttu-id="03e8c-118">acceso de lectura</span><span class="sxs-lookup"><span data-stu-id="03e8c-118">Read access</span></span>                |
| <span data-ttu-id="03e8c-119">\_escritura genérica</span><span class="sxs-lookup"><span data-stu-id="03e8c-119">GENERIC\_WRITE</span></span>   | <span data-ttu-id="03e8c-120">Acceso de escritura</span><span class="sxs-lookup"><span data-stu-id="03e8c-120">Write access</span></span>               |



 

<span data-ttu-id="03e8c-121">Las aplicaciones que definen objetos protegibles privados también pueden usar los derechos de acceso genéricos.</span><span class="sxs-lookup"><span data-stu-id="03e8c-121">Applications that define private securable objects can also use the generic access rights.</span></span>

 

 



