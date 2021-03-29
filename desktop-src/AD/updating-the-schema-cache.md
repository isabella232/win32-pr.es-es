---
title: Actualización de la caché de esquema
description: Toda la información que se escribe en un servidor de Active Directory se valida con respecto al esquema.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Actualización de la caché de esquema AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773051"
---
# <a name="updating-the-schema-cache"></a><span data-ttu-id="5f6de-104">Actualización de la caché de esquema</span><span class="sxs-lookup"><span data-stu-id="5f6de-104">Updating the Schema Cache</span></span>

<span data-ttu-id="5f6de-105">Toda la información que se escribe en un servidor de Active Directory se valida con respecto al esquema.</span><span class="sxs-lookup"><span data-stu-id="5f6de-105">All information that is written to an Active Directory server is validated against the schema.</span></span> <span data-ttu-id="5f6de-106">El esquema se mantiene en memoria en los servidores de directorio (controladores de dominio) por motivos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5f6de-106">The schema is held in memory on directory servers (domain controllers) for performance reasons.</span></span> <span data-ttu-id="5f6de-107">La versión en memoria se actualiza automáticamente después de actualizar la versión en el disco.</span><span class="sxs-lookup"><span data-stu-id="5f6de-107">The in-memory version is updated automatically after the on-disk version has been updated.</span></span> <span data-ttu-id="5f6de-108">La actualización automática se produce cinco minutos después de aplicar el último cambio; al aplicar otro cambio en el esquema en la ventana de 5 minutos, se restablece el temporizador durante otros cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="5f6de-108">The automatic update occurs five minutes after the last change was applied; applying another change to the schema in the 5-minute window resets the timer for another 5 minutes.</span></span> <span data-ttu-id="5f6de-109">Este comportamiento mantiene la coherencia de la memoria caché, pero puede resultar confuso, ya que los cambios no aparecen en el esquema hasta que se actualice la memoria caché, aunque se hayan aplicado en el disco.</span><span class="sxs-lookup"><span data-stu-id="5f6de-109">This behavior keeps the cache consistent, but can be confusing, because changes do not appear in the schema until the cache is updated, even though they were applied on disk.</span></span>

<span data-ttu-id="5f6de-110">Para actualizar la memoria caché de esquemas de Active Directory después de una actualización de esquema, o si desea utilizar la actualización de esquema para las operaciones que no son de esquema inmediatamente, agregue el atributo **schemaUpdateNow** (es un atributo operativo) al DSE raíz (DN en blanco) con el valor 1.</span><span class="sxs-lookup"><span data-stu-id="5f6de-110">To update the Active Directory schema cache after a schema update, or if you want to use the schema update for non-schema operations immediately, add the **schemaUpdateNow** attribute (it is an operational attribute) to the root DSE (blank DN) with value 1.</span></span> <span data-ttu-id="5f6de-111">Una actualización de la caché de esquema se iniciará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5f6de-111">A schema cache update will start immediately.</span></span> <span data-ttu-id="5f6de-112">La llamada está bloqueando.</span><span class="sxs-lookup"><span data-stu-id="5f6de-112">The call is blocking.</span></span> <span data-ttu-id="5f6de-113">Si la llamada devuelve sin ningún error, la memoria caché se actualiza y todas las actualizaciones del esquema están listas para usarse.</span><span class="sxs-lookup"><span data-stu-id="5f6de-113">If the call returns with no error, the cache is updated and all schema updates are ready to be used.</span></span> <span data-ttu-id="5f6de-114">Un error devuelto indica que la actualización de la memoria caché no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5f6de-114">An error return indicates the cache update was unsuccessful.</span></span> <span data-ttu-id="5f6de-115">Las aplicaciones que deben usar esta característica deben diseñarse para adaptarse a la escritura de bloqueo, especialmente en el caso de los comentarios de los usuarios, si el programa o el script se ejecutan de forma interactiva.</span><span class="sxs-lookup"><span data-stu-id="5f6de-115">Applications that must use this feature should be designed to accommodate the blocking write, particularly in giving the user feedback, if the program or script executes interactively.</span></span>

<span data-ttu-id="5f6de-116">El ejemplo de código siguiente es un script de LDIFDE de ejemplo que muestra cómo desencadenar una recarga de caché.</span><span class="sxs-lookup"><span data-stu-id="5f6de-116">The following code example is a sample LDIFDE script that shows how to trigger a cache reload.</span></span>

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

<span data-ttu-id="5f6de-117">Para obtener más información sobre cómo actualizar la caché de esquema mediante programación, vea [el código de ejemplo para actualizar la caché de esquema](example-code-for-updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="5f6de-117">For more information about how to update the schema cache programmatically, see [Example Code for Updating the Schema Cache](example-code-for-updating-the-schema-cache.md).</span></span>

 

 




