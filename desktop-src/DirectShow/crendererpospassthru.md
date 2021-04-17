---
description: La clase CRendererPosPassThru controla los comandos de búsqueda para los filtros de representador, pasándolos al siguiente filtro.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Clase CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670727"
---
# <a name="crendererpospassthru-class"></a>Clase CRendererPosPassThru

![jerarquía de clases crendererpospassthru](images/cutil14.png)

La `CRendererPosPassThru` clase controla los comandos de búsqueda para los filtros de representador, pasándolos al siguiente filtro.

Esta clase se deriva de la clase [**CPosPassThru**](cpospassthru.md) . Agrega compatibilidad para el almacenamiento en caché de las marcas de tiempo de los ejemplos a medida que llegan. Utilice esta clase de la misma forma que la clase **CPosPassThru** . Consulte la documentación de **CPosPassThru** para obtener más información.

El filtro de representador debe actualizar las `CRendererPosPassThru` marcas de tiempo almacenadas en caché del objeto, como se indica a continuación:

-   Para cada ejemplo que recibe el filtro, llame al método [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) .
-   Cuando se detenga el filtro o reciba una llamada **EndFlush** , llame al método [**CRendererPosPassThru:: ResetMediaTime**](crendererpospassthru-resetmediatime.md) .
-   Cuando el filtro recibe una notificación de final de secuencia, llame al método [**CRendererPosPassThru:: EOS**](crendererpospassthru-eos.md) .

Para obtener un ejemplo de cómo usar esta clase, consulte el código fuente de [**CBaseRenderer**](cbaserenderer.md) .



| Métodos públicos                                                            | Descripción                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**CRendererPosPassThru**](crendererpospassthru-crendererpospassthru.md) | Método de constructor.                                                 |
| [**GetMediaTime**](crendererpospassthru-getmediatime.md)                 | Recupera las marcas de tiempo en el ejemplo actual.                    |
| [**RegisterMediaTime**](crendererpospassthru-registermediatime.md)       | Almacena en memoria caché las marcas de tiempo del ejemplo actual.                     |
| [**ResetMediaTime**](crendererpospassthru-resetmediatime.md)             | Restablece el valor cero de las marcas de tiempo almacenadas en caché.                              |
| [**OCASIONA**](crendererpospassthru-eos.md)                                   | Actualiza las marcas de tiempo almacenadas en caché después de una notificación de final de secuencia. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




