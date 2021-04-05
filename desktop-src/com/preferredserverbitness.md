---
title: PreferredServerBitness
description: Establece la arquitectura preferida, 32 bits o 64 bits, para este servidor COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- Valor del registro PreferredServerBitness COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359444"
---
# <a name="preferredserverbitness"></a><span data-ttu-id="16370-104">PreferredServerBitness</span><span class="sxs-lookup"><span data-stu-id="16370-104">PreferredServerBitness</span></span>

<span data-ttu-id="16370-105">Establece la arquitectura preferida, 32 bits o 64 bits, para este servidor COM.</span><span class="sxs-lookup"><span data-stu-id="16370-105">Sets the preferred architecture, 32-bit or 64-bit, for this COM server.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="16370-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="16370-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a><span data-ttu-id="16370-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16370-107">Remarks</span></span>

<span data-ttu-id="16370-108">Se trata de un valor de **Registro \_ DWORD** que solo está disponible en las versiones de 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="16370-108">This is a **REG\_DWORD** value that is available only on 64-bit versions of Windows.</span></span>



| <span data-ttu-id="16370-109">Value</span><span class="sxs-lookup"><span data-stu-id="16370-109">Value</span></span> | <span data-ttu-id="16370-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="16370-110">Description</span></span>                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16370-111">1</span><span class="sxs-lookup"><span data-stu-id="16370-111">1</span></span>     | <span data-ttu-id="16370-112">Haga coincidir la arquitectura de servidor con la arquitectura de cliente.</span><span class="sxs-lookup"><span data-stu-id="16370-112">Match the server architecture to the client architecture.</span></span> <span data-ttu-id="16370-113">Por ejemplo, si el cliente es de 32 bits, utilice una versión de 32 bits del servidor, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="16370-113">For example, if the client is 32-bit, use a 32-bit version of the server, if it is available.</span></span> <span data-ttu-id="16370-114">De lo contrario, se producirá un error en la solicitud de activación del cliente.</span><span class="sxs-lookup"><span data-stu-id="16370-114">If not, the client's activation request will fail.</span></span> |
| <span data-ttu-id="16370-115">2</span><span class="sxs-lookup"><span data-stu-id="16370-115">2</span></span>     | <span data-ttu-id="16370-116">Use una versión de 32 bits del servidor.</span><span class="sxs-lookup"><span data-stu-id="16370-116">Use a 32-bit version of the server.</span></span> <span data-ttu-id="16370-117">Si no existe ninguna, se producirá un error en la solicitud de activación del cliente.</span><span class="sxs-lookup"><span data-stu-id="16370-117">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |
| <span data-ttu-id="16370-118">3</span><span class="sxs-lookup"><span data-stu-id="16370-118">3</span></span>     | <span data-ttu-id="16370-119">Use una versión de 64 bits del servidor.</span><span class="sxs-lookup"><span data-stu-id="16370-119">Use a 64-bit version of the server.</span></span> <span data-ttu-id="16370-120">Si no existe ninguna, se producirá un error en la solicitud de activación del cliente.</span><span class="sxs-lookup"><span data-stu-id="16370-120">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |



 

<span data-ttu-id="16370-121">Si este valor no está presente, entonces:</span><span class="sxs-lookup"><span data-stu-id="16370-121">If this value is not present, then:</span></span>

-   <span data-ttu-id="16370-122">Si el equipo que hospeda el servidor está ejecutando Windows XP o Windows Server 2003 sin SP1 o posterior instalado, COM preferirá una versión de 64 bits del servidor si está disponible; en caso contrario, activará una versión de 32 bits del servidor.</span><span class="sxs-lookup"><span data-stu-id="16370-122">If the computer that hosts the server is running Windows XP or Windows Server 2003 without SP1 or later installed, then COM will prefer a 64-bit version of the server if available; otherwise it will activate a 32-bit version of the server.</span></span>
-   <span data-ttu-id="16370-123">Si el equipo que hospeda el servidor está ejecutando Windows Server 2003 con SP1 o una versión posterior instalada, COM intentará hacer coincidir la arquitectura de servidor con la arquitectura de cliente.</span><span class="sxs-lookup"><span data-stu-id="16370-123">If the computer that hosts the server is running Windows Server 2003 with SP1 or later installed, then COM will try to match the server architecture to the client architecture.</span></span> <span data-ttu-id="16370-124">En otras palabras, para un cliente de 32 bits, COM activará un servidor de 32 bits si está disponible; en caso contrario, activará una versión de 64 bits del servidor.</span><span class="sxs-lookup"><span data-stu-id="16370-124">In other words, for a 32-bit client, COM will activate a 32-bit server if available; otherwise it will activate a 64-bit version of the server.</span></span> <span data-ttu-id="16370-125">Para un cliente de 64 bits, COM activará un servidor de 64 bits si está disponible; en caso contrario, activará un servidor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="16370-125">For a 64-bit client, COM will activate a 64-bit server if available; otherwise it will activate a 32-bit server.</span></span>

<span data-ttu-id="16370-126">El cliente también puede especificar su propia preferencia de arquitectura a través de las \_ marcas de servidor CLSCTX activar \_ 32 \_ bits \_ y CLSCTX \_ activar \_ 64 \_ bits \_ , y esto invalidará las preferencias del servidor.</span><span class="sxs-lookup"><span data-stu-id="16370-126">The client can also specify its own architecture preference via the CLSCTX\_ACTIVATE\_32\_BIT\_SERVER and CLSCTX\_ACTIVATE\_64\_BIT\_SERVER flags, and these will override the server's preference.</span></span> <span data-ttu-id="16370-127">Para obtener más información y un gráfico de posibles interacciones entre las preferencias de la arquitectura de cliente y de servidor, vea [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span><span class="sxs-lookup"><span data-stu-id="16370-127">For more information, and a chart of possible interactions between client and server architecture preferences, see [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="16370-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16370-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16370-129">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="16370-129">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 