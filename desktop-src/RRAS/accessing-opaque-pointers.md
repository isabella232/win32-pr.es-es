---
title: Obtener acceso a punteros opacos
description: Los clientes pueden tener acceso a la información almacenada en destinos mediante punteros opacos.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532260"
---
# <a name="accessing-opaque-pointers"></a><span data-ttu-id="4f599-103">Obtener acceso a punteros opacos</span><span class="sxs-lookup"><span data-stu-id="4f599-103">Accessing Opaque Pointers</span></span>

<span data-ttu-id="4f599-104">Los clientes pueden tener acceso a la información almacenada en destinos mediante punteros opacos.</span><span class="sxs-lookup"><span data-stu-id="4f599-104">Clients are able to access the information stored in destinations by using opaque pointers.</span></span> <span data-ttu-id="4f599-105">Para usar el almacenamiento, el cliente debe llamar primero a [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) para obtener el puntero.</span><span class="sxs-lookup"><span data-stu-id="4f599-105">To use the storage, the client must first call [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) to obtain the pointer.</span></span> <span data-ttu-id="4f599-106">Cada vez que se necesita un cambio en la información, el cliente debe bloquear primero el destino llamando a [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) con el parámetro *LockDest* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="4f599-106">Whenever a change to the information is necessary, the client must first lock the destination by calling [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) with the *LockDest* parameter set to **TRUE**.</span></span> <span data-ttu-id="4f599-107">Una vez que el destino está bloqueado, el cliente puede realizar el cambio necesario.</span><span class="sxs-lookup"><span data-stu-id="4f599-107">Once the destination is locked, the client can make the necessary change.</span></span> <span data-ttu-id="4f599-108">El destino se puede desbloquear mediante otra llamada a **RtmLockDestination** con el parámetro *LockDest* establecido en **false**.</span><span class="sxs-lookup"><span data-stu-id="4f599-108">The destination can be unlocked using another call to **RtmLockDestination** with the *LockDest* parameter set to **FALSE**.</span></span>

<span data-ttu-id="4f599-109">La función [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) también permite que un cliente use un bloqueo de lectura o de escritura, mediante el parámetro *Exclusive* .</span><span class="sxs-lookup"><span data-stu-id="4f599-109">The [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) function also allows a client to use either a read lock or a write lock, using the *Exclusive* parameter.</span></span> <span data-ttu-id="4f599-110">Un cliente debe utilizar el bloqueo de escritura solo cuando está realizando cambios en la información que se mantiene con el puntero opaco.</span><span class="sxs-lookup"><span data-stu-id="4f599-110">A client should use the write lock only when it is making changes to the information kept using the opaque pointer.</span></span> <span data-ttu-id="4f599-111">Los clientes pueden usar el bloqueo de lectura para ver la información de puntero opaco almacenada en un destino.</span><span class="sxs-lookup"><span data-stu-id="4f599-111">Clients can use the read lock to view the opaque pointer information stored in a destination.</span></span>

<span data-ttu-id="4f599-112">Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [acceso al puntero opaco en un destino](access-the-opaque-pointer-in-a-destination.md).</span><span class="sxs-lookup"><span data-stu-id="4f599-112">For sample code that shows how to use these functions, see [Access the Opaque Pointer in a Destination](access-the-opaque-pointer-in-a-destination.md).</span></span>

 

 




