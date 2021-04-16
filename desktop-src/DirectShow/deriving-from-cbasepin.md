---
description: Derivación de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivación de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677204"
---
# <a name="deriving-from-cbasepin"></a>Derivación de CBasePin

Para implementar un PIN mediante [**CBasePin**](cbasepin.md), debe derivar una nueva clase de la clase base e invalidar algunos de sus métodos. Debe invalidar los métodos siguientes:

-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Probablemente tendrá que invalidar estos métodos adicionales:

-   [**CBasePin:: Active**](cbasepin-active.md)
-   [**CBasePin::BreakConnect**](cbasepin-breakconnect.md)
-   [**CBasePin::CheckConnect**](cbasepin-checkconnect.md)
-   [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md)
-   [**CBasePin:: EndOfStream**](cbasepin-endofstream.md)
-   [**CBasePin:: inactivo**](cbasepin-inactive.md)
-   [**CBasePin:: Notify**](cbasepin-notify.md)
-   [**CBasePin:: Run**](cbasepin-run.md)

Por último, debe implementar los métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) y [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

Algunos de estos métodos se implementan en clases base que derivan de **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md) y [**CBaseOutputPin**](cbaseoutputpin.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



