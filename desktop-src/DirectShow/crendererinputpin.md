---
description: La clase CBaseRendererInputPin implementa un PIN de entrada para la clase CBaseRenderer. Excepto donde se indique, los métodos de esta clase delegan a los métodos correspondientes en la clase CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Clase CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661283"
---
# <a name="crendererinputpin-class"></a>Clase CRendererInputPin

![jerarquía de clases crendererinput PIN](images/rbase01.png)

La clase **CBaseRendererInputPin** implementa un PIN de entrada para la clase [**CBaseRenderer**](cbaserenderer.md) . Excepto donde se indique, los métodos de esta clase delegan a los métodos correspondientes en la clase **CBaseRenderer** .



| Variables de miembro protegidas                                       | Descripción                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pRenderer**](crendererinputpin-m-prenderer.md)            | Puntero al filtro.                                                                 |
| Métodos públicos                                                   | Descripción                                                                            |
| [**CRendererInputPin**](crendererinputpin-crendererinputpin.md) | Método de constructor.                                                                    |
| [**BreakConnect**](crendererinputpin-breakconnect.md)           | Agrega código personalizado al interrumpir una conexión.                                       |
| [**CompleteConnect**](crendererinputpin-completeconnect.md)     | Completa la conexión.                                                              |
| [**CheckMediaType**](crendererinputpin-checkmediatype.md)       | Determina si el pin puede admitir un tipo de medio específico.                               |
| [**Active**](crendererinputpin-active.md)                       | Cambia el PIN al modo activo (en pausa o en ejecución).                               |
| [**Inactivo**](crendererinputpin-inactive.md)                   | Cambia el PIN a un estado inactivo y libera la memoria del asignador.        |
| [**SetMediaType**](crendererinputpin-setmediatype.md)           | Establece el tipo de medio del PIN.                                                        |
| [**Asignador**](crendererinputpin-allocator.md)                 | Recupera un puntero al asignador de memoria predeterminado.                                   |
| Métodos IPin                                                     | Descripción                                                                            |
| [**QueryId**](crendererinputpin-queryid.md)                     | Recupera un identificador para el código PIN.                                                   |
| [**EndOfStream**](crendererinputpin-endofstream.md)             | Informa al pin de que no se esperan datos adicionales hasta que se emita un nuevo comando de ejecución. |
| [**BeginFlush**](crendererinputpin-beginflush.md)               | Informa al pin para iniciar una operación de vaciado.                                            |
| [**EndFlush**](crendererinputpin-endflush.md)                   | Informa al código PIN para finalizar una operación de vaciado.                                              |
| Métodos IMemInputPin                                             | Descripción                                                                            |
| [**Aparecen**](crendererinputpin-receive.md)                     | Recupera el siguiente bloque de datos de la secuencia.                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




