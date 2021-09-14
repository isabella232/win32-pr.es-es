---
description: La clase CBaseRendererInputPin implementa un pin de entrada para la clase CBaseRenderer. Excepto donde se indica, los métodos de esta clase delegan a los métodos correspondientes en la clase CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: CRendererInputPin (clase, Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362459"
---
# <a name="crendererinputpin-class"></a>CRendererInputPin (clase)

![Jerarquía de clases pin crendererinput](images/rbase01.png)

La **clase CBaseRendererInputPin** implementa un pin de entrada para la [**clase CBaseRenderer.**](cbaserenderer.md) Excepto donde se indica, los métodos de esta clase delegan a los métodos correspondientes en la **clase CBaseRenderer.**



| Variables miembro protegidas                                       | Descripción                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pRenderer**](crendererinputpin-m-prenderer.md)            | Puntero al filtro.                                                                 |
| Métodos públicos                                                   | Descripción                                                                            |
| [**CRendererInputPin**](crendererinputpin-crendererinputpin.md) | Método constructor.                                                                    |
| [**BreakConnect**](crendererinputpin-breakconnect.md)           | Agrega código personalizado al romper una conexión.                                       |
| [**CompleteConnect**](crendererinputpin-completeconnect.md)     | Completa la conexión.                                                              |
| [**CheckMediaType**](crendererinputpin-checkmediatype.md)       | Determina si el pin puede admitir un tipo de medio específico.                               |
| [**Activo**](crendererinputpin-active.md)                       | Cambia el pin al modo activo (en pausa o en ejecución).                               |
| [**Inactivo**](crendererinputpin-inactive.md)                   | Cambia el pin a un estado inactivo y libera la memoria del asignador.        |
| [**SetMediaType**](crendererinputpin-setmediatype.md)           | Establece el tipo de medio de la marca.                                                        |
| [**Asignador**](crendererinputpin-allocator.md)                 | Recupera un puntero al asignador de memoria predeterminado.                                   |
| Métodos de IPin                                                     | Descripción                                                                            |
| [**QueryId**](crendererinputpin-queryid.md)                     | Recupera un identificador para el pin.                                                   |
| [**EndOfStream**](crendererinputpin-endofstream.md)             | Informa al pin de que no se esperan datos adicionales hasta que se emite un nuevo comando de ejecución. |
| [**BeginFlush**](crendererinputpin-beginflush.md)               | Informa al pin para iniciar una operación de vaciado.                                            |
| [**EndFlush**](crendererinputpin-endflush.md)                   | Informa al pin para finalizar una operación de vaciado.                                              |
| Métodos IMemInputPin                                             | Descripción                                                                            |
| [**Recepción**](crendererinputpin-receive.md)                     | Recupera el siguiente bloque de datos de la secuencia.                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




