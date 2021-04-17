---
description: La clase CRenderedInputPin es una clase base para implementar un PIN de entrada en un representador.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Clase CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670984"
---
# <a name="crenderedinputpin-class"></a>Clase CRenderedInputPin

![jerarquía de clases crenderedinputpin](images/rbase04.png)

La clase **CRenderedInputPin** es una clase base para implementar un PIN de entrada en un representador. Esta clase está diseñada para los filtros de representador que no derivan de la clase [**CBaseRenderer**](cbaserenderer.md) . (Los filtros que derivan de **CBaseRenderer** deben usar la clase [**CRendererInputPin**](crendererinputpin.md) para el PIN de entrada).

Para usar esta clase, debe realizar al menos lo siguiente:

-   Declare una nueva clase de PIN que herede **CRenderedInputPin**.
-   En la clase PIN, declare un objeto de sección crítica para que contenga el bloqueo de streaming. Puede usar la clase [**CCritSec**](ccritsec.md) para este propósito. Para obtener más información, vea [subprocesos y secciones críticas](threads-and-critical-sections.md).
-   Invalide [**CRenderedInputPin:: EndOfStream**](crenderedinputpin-endofstream.md) para contener el bloqueo de streaming.
-   Implemente los métodos [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md)y [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .
-   En el filtro, implemente [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) para devolver una instancia de la clase de PIN.

Puede usar esta clase en un representador que tenga más de un PIN de entrada. Esta clase hereda la clase [**CBaseInputPin**](cbaseinputpin.md) .



| Variables de miembro protegidas                                            | Descripción                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**m \_ bAtEndOfStream**](crenderedinputpin-m-batendofstream.md)       | Indica si se ha alcanzado el final de la secuencia.                                                         |
| [**m \_ bCompleteNotified**](crenderedinputpin-m-bcompletenotified.md) | Indica si el PIN ha enviado un evento de [**\_ finalización de EC**](ec-complete.md) al administrador de gráficos de filtro. |
| Métodos públicos                                                        | Descripción                                                                                                  |
| [**Activo**](crenderedinputpin-active.md)                            | Notifica al pin que el filtro está activo ahora.                                                              |
| [**CRenderedInputPin**](crenderedinputpin-crenderedinputpin.md)      | Método de constructor.                                                                                          |
| [**Ejecutar**](crenderedinputpin-run.md)                                  | Notifica al pin que el filtro se está ejecutando ahora.                                                             |
| Métodos IPin                                                          | Descripción                                                                                                  |
| [**EndFlush**](crenderedinputpin-endflush.md)                        | Finaliza una operación de vaciado.                                                                                      |
| [**EndOfStream**](crenderedinputpin-endofstream.md)                  | Notifica al pin que no se espera ningún dato adicional hasta que el filtro recibe un nuevo comando de ejecución.            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amextra. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




