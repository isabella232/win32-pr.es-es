---
description: Las siguientes funciones se usan con DDE de red.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funciones DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697866"
---
# <a name="network-dde-functions"></a><span data-ttu-id="8c9ce-103">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="8c9ce-103">Network DDE Functions</span></span>

<span data-ttu-id="8c9ce-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="8c9ce-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="8c9ce-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="8c9ce-106">Las siguientes funciones se usan con DDE de red.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-106">The following functions are used with network DDE.</span></span>



| <span data-ttu-id="8c9ce-107">Función</span><span class="sxs-lookup"><span data-stu-id="8c9ce-107">Function</span></span>                                                   | <span data-ttu-id="8c9ce-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c9ce-108">Description</span></span>                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c9ce-109">**NDdeGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-109">**NDdeGetErrorString**</span></span>](nddegeterrorstring.md)           | <span data-ttu-id="8c9ce-110">Convierte un código de error devuelto por una función DDE de red en una cadena de error que explica el código de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-110">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span> |
| [<span data-ttu-id="8c9ce-111">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-111">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)       | <span data-ttu-id="8c9ce-112">Recupera el descriptor de seguridad asociado al recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-112">Retrieves the security descriptor associated with the DDE share.</span></span>                                                      |
| [<span data-ttu-id="8c9ce-113">**NDdeGetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-113">**NDdeGetTrustedShare**</span></span>](nddegettrustedshare.md)         | <span data-ttu-id="8c9ce-114">Recupera las opciones asociadas a un recurso compartido DDE que se encuentra en la lista de recursos compartidos de confianza del usuario del servidor.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-114">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>                |
| [<span data-ttu-id="8c9ce-115">**NDdeIsValidAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-115">**NDdeIsValidAppTopicList**</span></span>](nddeisvalidapptopiclist.md) | <span data-ttu-id="8c9ce-116">Determina si una aplicación y una cadena de tema ("*appname* \| *TopicName*") utiliza la sintaxis correcta.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-116">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>                 |
| [<span data-ttu-id="8c9ce-117">**NDdeIsValidShareName**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-117">**NDdeIsValidShareName**</span></span>](nddeisvalidsharename.md)       | <span data-ttu-id="8c9ce-118">Determina si un nombre de recurso compartido utiliza la sintaxis correcta.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-118">Determines whether a share name uses the proper syntax.</span></span>                                                               |
| [<span data-ttu-id="8c9ce-119">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-119">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)       | <span data-ttu-id="8c9ce-120">Establece el descriptor de seguridad asociado al recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-120">Sets the security descriptor associated with the DDE share.</span></span>                                                           |
| [<span data-ttu-id="8c9ce-121">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-121">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)         | <span data-ttu-id="8c9ce-122">Concede el estado de confianza del recurso compartido DDE especificado en el contexto del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-122">Grants the specified DDE share trusted status within the current user's context.</span></span>                                      |
| [<span data-ttu-id="8c9ce-123">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-123">**NDdeShareAdd**</span></span>](nddeshareadd.md)                       | <span data-ttu-id="8c9ce-124">Crea y agrega un nuevo recurso compartido DDE al administrador de bases de datos de recursos compartidos DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="8c9ce-124">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>                                            |
| [<span data-ttu-id="8c9ce-125">**NDdeShareDel**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-125">**NDdeShareDel**</span></span>](nddesharedel.md)                       | <span data-ttu-id="8c9ce-126">Elimina un recurso compartido DDE del DSDM.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-126">Deletes a DDE share from the DSDM.</span></span>                                                                                    |
| [<span data-ttu-id="8c9ce-127">**NDdeShareEnum**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-127">**NDdeShareEnum**</span></span>](nddeshareenum.md)                     | <span data-ttu-id="8c9ce-128">Recupera la lista de recursos compartidos DDE disponibles.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-128">Retrieves the list of available DDE shares.</span></span>                                                                           |
| [<span data-ttu-id="8c9ce-129">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-129">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)               | <span data-ttu-id="8c9ce-130">Recupera la información del recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-130">Retrieves DDE share information.</span></span>                                                                                      |
| [<span data-ttu-id="8c9ce-131">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-131">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)               | <span data-ttu-id="8c9ce-132">Establece la información de recursos compartidos DDE.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-132">Sets DDE share information.</span></span>                                                                                           |
| [<span data-ttu-id="8c9ce-133">**NDdeTrustedShareEnum**</span><span class="sxs-lookup"><span data-stu-id="8c9ce-133">**NDdeTrustedShareEnum**</span></span>](nddetrustedshareenum.md)       | <span data-ttu-id="8c9ce-134">Recupera los nombres de todos los recursos compartidos DDE de red que son de confianza en el contexto del proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-134">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>                 |



 

 

 



