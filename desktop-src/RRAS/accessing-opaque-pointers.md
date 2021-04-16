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
# <a name="accessing-opaque-pointers"></a>Obtener acceso a punteros opacos

Los clientes pueden tener acceso a la información almacenada en destinos mediante punteros opacos. Para usar el almacenamiento, el cliente debe llamar primero a [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) para obtener el puntero. Cada vez que se necesita un cambio en la información, el cliente debe bloquear primero el destino llamando a [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) con el parámetro *LockDest* establecido en **true**. Una vez que el destino está bloqueado, el cliente puede realizar el cambio necesario. El destino se puede desbloquear mediante otra llamada a **RtmLockDestination** con el parámetro *LockDest* establecido en **false**.

La función [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) también permite que un cliente use un bloqueo de lectura o de escritura, mediante el parámetro *Exclusive* . Un cliente debe utilizar el bloqueo de escritura solo cuando está realizando cambios en la información que se mantiene con el puntero opaco. Los clientes pueden usar el bloqueo de lectura para ver la información de puntero opaco almacenada en un destino.

Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [acceso al puntero opaco en un destino](access-the-opaque-pointer-in-a-destination.md).

 

 




