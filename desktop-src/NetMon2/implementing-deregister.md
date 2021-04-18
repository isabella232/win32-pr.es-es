---
description: Monitor de red pasa todos los marcos de una captura a los analizadores y, a continuación, comienza a llamar a la función de eliminación de registros para todos los protocolos que identifica. Cada DLL del analizador debe implementar una función de eliminación de registro para cada protocolo que admita el archivo DLL del analizador.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementación de unregister
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652404"
---
# <a name="implementing-deregister"></a><span data-ttu-id="fdef9-104">Implementación de unregister</span><span class="sxs-lookup"><span data-stu-id="fdef9-104">Implementing Deregister</span></span>

<span data-ttu-id="fdef9-105">Monitor de red pasa todos los marcos de una captura a los analizadores y, a continuación, comienza a llamar a la función de [**eliminación de registros**](deregister.md) para todos los protocolos que identifica.</span><span class="sxs-lookup"><span data-stu-id="fdef9-105">Network Monitor passes all the frames of a capture to the parsers, and then starts calling the [**Deregister**](deregister.md) function for all the protocols it identifies.</span></span> <span data-ttu-id="fdef9-106">Cada DLL del analizador debe implementar una función de **eliminación de registro** para cada protocolo que admita el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="fdef9-106">Each parser DLL must implement a **Deregister** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="fdef9-107">Cada implementación de la función de [**eliminación de registros**](deregister.md) debe llamar a la función [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar los recursos que se usan para crear la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fdef9-107">Each implementation of the [**Deregister**](deregister.md) function must call the [**DestroyProtocolDatabase**](destroypropertydatabase.md) function to release the resources that are used to create the database.</span></span>

<span data-ttu-id="fdef9-108">En el procedimiento siguiente se identifica el paso necesario para implementar [**unregister**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="fdef9-108">The following procedure identifies the one step necessary to implement [**Deregister**](deregister.md).</span></span>

<span data-ttu-id="fdef9-109">**Para implementar el anulación del registro para un protocolo**</span><span class="sxs-lookup"><span data-stu-id="fdef9-109">**To implement Deregister for one protocol**</span></span>

-   <span data-ttu-id="fdef9-110">Llame a [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar los recursos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fdef9-110">Call [**DestroyProtocolDatabase**](destroypropertydatabase.md) to release the database resources.</span></span>

<span data-ttu-id="fdef9-111">La siguiente es una implementación básica de [**unregister**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="fdef9-111">The following is a basic implementation of [**Deregister**](deregister.md).</span></span> <span data-ttu-id="fdef9-112">Tenga en cuenta que en el ejemplo de código se muestra la liberación de los recursos que se usan para crear una base de datos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fdef9-112">Note that the code example shows the release of resources that are used to create a property database.</span></span>

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



