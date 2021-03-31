---
description: Cada tipo de objeto protegible tiene un conjunto de derechos de acceso que corresponden a las operaciones específicas de ese tipo de objeto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Derechos de acceso estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908167"
---
# <a name="standard-access-rights"></a><span data-ttu-id="dc9cf-103">Derechos de acceso estándar</span><span class="sxs-lookup"><span data-stu-id="dc9cf-103">Standard Access Rights</span></span>

<span data-ttu-id="dc9cf-104">Cada tipo de objeto protegible tiene un conjunto de derechos de acceso que corresponden a las operaciones específicas de ese tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-104">Each type of securable object has a set of access rights that correspond to operations specific to that type of object.</span></span> <span data-ttu-id="dc9cf-105">Además de estos derechos de acceso específicos del objeto, existe un conjunto de derechos de acceso estándar que se corresponden con operaciones comunes a la mayoría de los tipos de objetos protegibles.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-105">In addition to these object-specific access rights, there is a set of standard access rights that correspond to operations common to most types of securable objects.</span></span>

<span data-ttu-id="dc9cf-106">El [formato de máscara de acceso](access-mask-format.md) incluye un conjunto de bits para los derechos de acceso estándar.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-106">The [access mask format](access-mask-format.md) includes a set of bits for the standard access rights.</span></span> <span data-ttu-id="dc9cf-107">Las siguientes constantes de Windows para los derechos de acceso estándar se definen en Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-107">The following Windows constants for standard access rights are defined in Winnt.h.</span></span>



| <span data-ttu-id="dc9cf-108">Constante</span><span class="sxs-lookup"><span data-stu-id="dc9cf-108">Constant</span></span>      | <span data-ttu-id="dc9cf-109">Significado</span><span class="sxs-lookup"><span data-stu-id="dc9cf-109">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9cf-110">Delete</span><span class="sxs-lookup"><span data-stu-id="dc9cf-110">DELETE</span></span>        | <span data-ttu-id="dc9cf-111">Derecho a eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-111">The right to delete the object.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="dc9cf-112">CONTROL de lectura \_</span><span class="sxs-lookup"><span data-stu-id="dc9cf-112">READ\_CONTROL</span></span> | <span data-ttu-id="dc9cf-113">Derecho para leer la información del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)del objeto, sin incluir la información de la [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="dc9cf-113">The right to read the information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), not including the information in the [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> |
| <span data-ttu-id="dc9cf-114">SYNCHRONIZE</span><span class="sxs-lookup"><span data-stu-id="dc9cf-114">SYNCHRONIZE</span></span>   | <span data-ttu-id="dc9cf-115">Derecho a utilizar el objeto para la sincronización.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-115">The right to use the object for synchronization.</span></span> <span data-ttu-id="dc9cf-116">Esto permite a un subproceso esperar hasta que el objeto se encuentra en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-116">This enables a thread to wait until the object is in the signaled state.</span></span> <span data-ttu-id="dc9cf-117">Algunos tipos de objetos no admiten este derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-117">Some object types do not support this access right.</span></span>                                                                                                                                                                |
| <span data-ttu-id="dc9cf-118">ESCRIBIR \_ DAC</span><span class="sxs-lookup"><span data-stu-id="dc9cf-118">WRITE\_DAC</span></span>    | <span data-ttu-id="dc9cf-119">Derecho a modificar la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) en el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-119">The right to modify the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) in the object's security descriptor.</span></span>                                                                                                                    |
| <span data-ttu-id="dc9cf-120">propietario de escritura \_</span><span class="sxs-lookup"><span data-stu-id="dc9cf-120">WRITE\_OWNER</span></span>  | <span data-ttu-id="dc9cf-121">Derecho a cambiar el propietario que figura en el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-121">The right to change the owner in the object's security descriptor.</span></span>                                                                                                                                                                                                                                                                           |



 

<span data-ttu-id="dc9cf-122">Winnt. h también define las siguientes combinaciones de las constantes de derechos de acceso estándar.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-122">Winnt.h also defines the following combinations of the standard access rights constants.</span></span>



| <span data-ttu-id="dc9cf-123">Constante</span><span class="sxs-lookup"><span data-stu-id="dc9cf-123">Constant</span></span>                   | <span data-ttu-id="dc9cf-124">Significado</span><span class="sxs-lookup"><span data-stu-id="dc9cf-124">Meaning</span></span>                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dc9cf-125">\_ \_ todos los derechos estándar</span><span class="sxs-lookup"><span data-stu-id="dc9cf-125">STANDARD\_RIGHTS\_ALL</span></span>      | <span data-ttu-id="dc9cf-126">Combina la eliminación, el \_ control de lectura, la \_ DAC de escritura, el propietario de escritura \_ y el acceso de sincronización.</span><span class="sxs-lookup"><span data-stu-id="dc9cf-126">Combines DELETE, READ\_CONTROL, WRITE\_DAC, WRITE\_OWNER, and SYNCHRONIZE access.</span></span> |
| <span data-ttu-id="dc9cf-127">se \_ ejecutan los derechos estándar \_</span><span class="sxs-lookup"><span data-stu-id="dc9cf-127">STANDARD\_RIGHTS\_EXECUTE</span></span>  | <span data-ttu-id="dc9cf-128">Definido actualmente para igualar el control de lectura \_ .</span><span class="sxs-lookup"><span data-stu-id="dc9cf-128">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="dc9cf-129">\_lectura de derechos estándar \_</span><span class="sxs-lookup"><span data-stu-id="dc9cf-129">STANDARD\_RIGHTS\_READ</span></span>     | <span data-ttu-id="dc9cf-130">Definido actualmente para igualar el control de lectura \_ .</span><span class="sxs-lookup"><span data-stu-id="dc9cf-130">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="dc9cf-131">\_derechos estándar \_ requeridos</span><span class="sxs-lookup"><span data-stu-id="dc9cf-131">STANDARD\_RIGHTS\_REQUIRED</span></span> | <span data-ttu-id="dc9cf-132">Combina la eliminación, el \_ control de lectura, la \_ DAC de escritura y el acceso de propietario de escritura \_ .</span><span class="sxs-lookup"><span data-stu-id="dc9cf-132">Combines DELETE, READ\_CONTROL, WRITE\_DAC, and WRITE\_OWNER access.</span></span>              |
| <span data-ttu-id="dc9cf-133">\_escritura de derechos estándar \_</span><span class="sxs-lookup"><span data-stu-id="dc9cf-133">STANDARD\_RIGHTS\_WRITE</span></span>    | <span data-ttu-id="dc9cf-134">Definido actualmente para igualar el control de lectura \_ .</span><span class="sxs-lookup"><span data-stu-id="dc9cf-134">Currently defined to equal READ\_CONTROL.</span></span>                                         |



 

 

 
