---
description: Derivar de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivar de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07eb76fc2913152a69ec729f49826e8b35f1524a3841c5e0d3085ea0634f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079265"
---
# <a name="deriving-from-cbasepin"></a>Derivar de CBasePin

Para implementar un pin mediante [**CBasePin,**](cbasepin.md)debe derivar una nueva clase de la clase base e invalidar varios de sus métodos. Debe invalidar los métodos siguientes:

-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Probablemente tendrá que invalidar estos métodos adicionales:

-   [**CBasePin::Active**](cbasepin-active.md)
-   [**CBasePin::BreakConnect**](cbasepin-breakconnect.md)
-   [**CBasePin::CheckConnect**](cbasepin-checkconnect.md)
-   [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md)
-   [**CBasePin::EndOfStream**](cbasepin-endofstream.md)
-   [**CBasePin::Inactive**](cbasepin-inactive.md)
-   [**CBasePin::Notify**](cbasepin-notify.md)
-   [**CBasePin::Run**](cbasepin-run.md)

Por último, debe implementar los métodos [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) [**e IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

Algunos de estos métodos se implementan en clases base que derivan de **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md) y [**CBaseOutputPin**](cbaseoutputpin.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



