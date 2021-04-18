---
description: Al abrir un identificador de un objeto, el identificador devuelto tiene una combinación de derechos de acceso al objeto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Solicitar derechos de acceso a un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666665"
---
# <a name="requesting-access-rights-to-an-object"></a><span data-ttu-id="6afc5-103">Solicitar derechos de acceso a un objeto</span><span class="sxs-lookup"><span data-stu-id="6afc5-103">Requesting Access Rights to an Object</span></span>

<span data-ttu-id="6afc5-104">Al abrir un identificador de un objeto, el identificador devuelto tiene una combinación de derechos de acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="6afc5-104">When you open a handle to an object, the returned handle has some combination of access rights to the object.</span></span> <span data-ttu-id="6afc5-105">Algunas funciones, como [**createsemaphore (**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), no requieren un conjunto específico de derechos de acceso solicitados.</span><span class="sxs-lookup"><span data-stu-id="6afc5-105">Some functions, such as [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), do not require a specific set of requested access rights.</span></span> <span data-ttu-id="6afc5-106">Estas funciones siempre intentan abrir el identificador de acceso completo.</span><span class="sxs-lookup"><span data-stu-id="6afc5-106">These functions always try to open the handle for full access.</span></span> <span data-ttu-id="6afc5-107">Otras funciones, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), permiten especificar el conjunto de derechos de acceso que se desea.</span><span class="sxs-lookup"><span data-stu-id="6afc5-107">Other functions, such as [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), allow you to specify the set of access rights that you want.</span></span> <span data-ttu-id="6afc5-108">Debe solicitar solo los derechos de acceso que necesita, en lugar de abrir un identificador de acceso completo.</span><span class="sxs-lookup"><span data-stu-id="6afc5-108">You should request only the access rights that you need, rather than opening a handle for full access.</span></span> <span data-ttu-id="6afc5-109">Esto evita el uso del identificador de manera no intencionada y aumenta las posibilidades de que la solicitud de acceso se realice correctamente si la DACL del objeto solo permite el acceso limitado.</span><span class="sxs-lookup"><span data-stu-id="6afc5-109">This prevents using the handle in an unintended way, and increases the chances that the access request will succeed if the object's DACL only allows limited access.</span></span>

<span data-ttu-id="6afc5-110">Use los [derechos de acceso genéricos](generic-access-rights.md) para especificar el tipo de acceso necesario al abrir un identificador de un objeto.</span><span class="sxs-lookup"><span data-stu-id="6afc5-110">Use [generic access rights](generic-access-rights.md) to specify the type of access needed when opening a handle to an object.</span></span> <span data-ttu-id="6afc5-111">Normalmente es más sencillo que especificar todos los derechos estándar y específicos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6afc5-111">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span> <span data-ttu-id="6afc5-112">También puede usar la constante MAXIMUM \_ allowed para solicitar que el objeto se abra con todos los derechos de acceso que son válidos para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6afc5-112">Alternatively, use the MAXIMUM\_ALLOWED constant to request that the object be opened with all the access rights that are valid for the caller.</span></span>

> [!Note]  
> <span data-ttu-id="6afc5-113">\_No se puede usar la constante máxima permitida en una ACE.</span><span class="sxs-lookup"><span data-stu-id="6afc5-113">The MAXIMUM\_ALLOWED constant cannot be used in an ACE.</span></span>

 

<span data-ttu-id="6afc5-114">Para obtener o establecer la SACL en el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto, solicite el [derecho de acceso de \_ \_ seguridad del sistema de acceso](sacl-access-right.md) al abrir un identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="6afc5-114">To get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), request the [ACCESS\_SYSTEM\_SECURITY access right](sacl-access-right.md) when opening a handle to the object.</span></span>

 

 
