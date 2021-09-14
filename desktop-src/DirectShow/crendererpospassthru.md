---
description: La clase CRendererPosPassThru controla los comandos de búsqueda para los filtros del representador, pasándolos de nivel superior al filtro siguiente.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: CRendererPosPassThru (clase, Ctlutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160188"
---
# <a name="crendererpospassthru-class"></a>CRendererPosPassThru (clase)

![crendererpospassthru (jerarquía de clases)](images/cutil14.png)

La clase controla los comandos de búsqueda para los filtros `CRendererPosPassThru` del representador, pasándolos de nivel superior al filtro siguiente.

Esta clase se deriva de la [**clase CPosPassThru.**](cpospassthru.md) Agrega compatibilidad para almacenar en caché las marcas de tiempo de los ejemplos a medida que llegan. Use esta clase de la misma manera que la **clase CPosPassThru.** Consulte la documentación **de CPosPassThru** para obtener más información.

El filtro del representador debe actualizar las marcas de tiempo almacenadas en caché `CRendererPosPassThru` del objeto, como se muestra a continuación:

-   Para cada ejemplo que recibe el filtro, llame [**al método CRendererPosPassThru::RegisterMediaTime.**](crendererpospassthru-registermediatime.md)
-   Cuando se detenga el filtro o reciba una llamada **a EndFlush,** llame al método [**CRendererPosPassThru::ResetMediaTime.**](crendererpospassthru-resetmediatime.md)
-   Cuando el filtro recibe una notificación de fin de flujo, llame al método [**CRendererPosPassThru::EOS.**](crendererpospassthru-eos.md)

Para obtener un ejemplo de cómo usar esta clase, consulte el código fuente [**de CBaseRenderer.**](cbaserenderer.md)



| Métodos públicos                                                            | Descripción                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**CRendererPosPassThru**](crendererpospassthru-crendererpospassthru.md) | Método constructor.                                                 |
| [**GetMediaTime**](crendererpospassthru-getmediatime.md)                 | Recupera las marcas de tiempo del ejemplo actual.                    |
| [**RegisterMediaTime**](crendererpospassthru-registermediatime.md)       | Almacena en caché las marcas de tiempo del ejemplo actual.                     |
| [**ResetMediaTime**](crendererpospassthru-resetmediatime.md)             | Restablece las marcas de tiempo almacenadas en caché a cero.                              |
| [**EOS**](crendererpospassthru-eos.md)                                   | Actualiza las marcas de tiempo almacenadas en caché después de una notificación de fin de secuencia. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




