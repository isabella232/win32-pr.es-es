---
description: Derivación de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivación de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061699"
---
# <a name="deriving-from-cbasepin"></a>Derivación de CBasePin

Para implementar un pin mediante [**CBasePin**](cbasepin.md), debe derivar una nueva clase de la clase base e invalidar varios de sus métodos. Debe invalidar los métodos siguientes:

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

 

 



