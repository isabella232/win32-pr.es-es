---
title: Funciones de adquisición de claves
description: De forma predeterminada, el SSP suministra claves de cifrado a los programas de servidor que las solicitan. Cada SSP implementa su propio sistema de generación de claves. El formato de las claves que genera el SSP es específico del SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903775"
---
# <a name="key-acquisition-functions"></a><span data-ttu-id="5cae7-105">Funciones de adquisición de claves</span><span class="sxs-lookup"><span data-stu-id="5cae7-105">Key Acquisition Functions</span></span>

<span data-ttu-id="5cae7-106">De forma predeterminada, el SSP suministra claves de cifrado a los programas de servidor que las solicitan.</span><span class="sxs-lookup"><span data-stu-id="5cae7-106">By default, the SSP supplies encryption keys to server programs that request them.</span></span> <span data-ttu-id="5cae7-107">Cada SSP implementa su propio sistema de generación de claves.</span><span class="sxs-lookup"><span data-stu-id="5cae7-107">Each SSP implements its own system of generating keys.</span></span> <span data-ttu-id="5cae7-108">El formato de las claves que genera el SSP es específico del SSP.</span><span class="sxs-lookup"><span data-stu-id="5cae7-108">The format of the keys that the SSP generates are specific to the SSP.</span></span>

<span data-ttu-id="5cae7-109">RPC le proporciona la capacidad de invalidar el método predeterminado de generación de claves de cifrado.</span><span class="sxs-lookup"><span data-stu-id="5cae7-109">RPC provides you with the ability to override the default method of generating encryption keys.</span></span> <span data-ttu-id="5cae7-110">La aplicación puede llamar a la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) y pasarle un puntero a una función de adquisición de clave.</span><span class="sxs-lookup"><span data-stu-id="5cae7-110">Your application can call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function and pass it a pointer to a key acquisition function.</span></span> <span data-ttu-id="5cae7-111">Puede escribir la función de adquisición de claves para que genere claves con cualquier método que elija.</span><span class="sxs-lookup"><span data-stu-id="5cae7-111">You can write the key acquisition function so that it generates keys using any method you choose.</span></span> <span data-ttu-id="5cae7-112">Sin embargo, la clave que pasa al programa de servidor debe coincidir con el formato que requiere el SSP.</span><span class="sxs-lookup"><span data-stu-id="5cae7-112">However, the key it passes to the server program must match the format that the SSP requires.</span></span>

> [!Note]  
> <span data-ttu-id="5cae7-113">La mayoría de las aplicaciones no necesitan usar funciones de adquisición clave y simplemente pueden proporcionar **null** a todos los parámetros en los que se solicita una función de adquisición de claves.</span><span class="sxs-lookup"><span data-stu-id="5cae7-113">Most applications do not need to use key acquisition functions, and can simply supply **NULL** to all parameters where a key acquisition function is requested.</span></span>

 

 

 




