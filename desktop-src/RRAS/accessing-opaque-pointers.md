---
title: Acceso a punteros opacos
description: Los clientes pueden acceder a la información almacenada en destinos mediante punteros opacos.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b76e99a66b13c696951a0d46684726f79f29df5b0287e9c4923dc4054943e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030625"
---
# <a name="accessing-opaque-pointers"></a>Acceso a punteros opacos

Los clientes pueden acceder a la información almacenada en destinos mediante punteros opacos. Para usar el almacenamiento, el cliente debe llamar primero [**a RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) para obtener el puntero. Siempre que sea necesario realizar un cambio en la información, el cliente debe bloquear primero el destino llamando a [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) con el *parámetro LockDest* establecido en **TRUE.** Una vez bloqueado el destino, el cliente puede realizar el cambio necesario. El destino se puede desbloquear mediante otra llamada a **RtmLockDestination** con el *parámetro LockDest* establecido en **FALSE.**

La [**función RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) también permite que un cliente use un bloqueo de lectura o un bloqueo de escritura, mediante el *parámetro Exclusive.* Un cliente debe usar el bloqueo de escritura solo cuando realiza cambios en la información que se mantiene mediante el puntero opaco. Los clientes pueden usar el bloqueo de lectura para ver la información de puntero opaco almacenada en un destino.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Acceso al puntero opaco en un destino](access-the-opaque-pointer-in-a-destination.md).

 

 




