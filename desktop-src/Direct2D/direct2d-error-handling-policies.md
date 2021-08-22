---
title: Directivas de control de errores de Direct2D
description: 'En este tema se describen las directivas de control de errores de Direct2D. Contiene las siguientes secciones:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, control de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3be48c5d80cbbd971f63392efaf6b902ff6187e0a2687df25ccc728efafbfab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318035"
---
# <a name="direct2d-error-handling-policies"></a>Directivas de control de errores de Direct2D

En este tema se describen las directivas de control de errores de Direct2D. Contiene las siguientes secciones:

-   [Uso de HRESULT](#use-of-hresult)
-   [Valor devuelto de las funciones por lotes](#return-value-of-batched-functions)
-   [Entrada no válida](#invalid-input)
    -   [Puntero de salida](#output-pointer)
    -   [Parámetro requerido](#required-parameter)
-   [NaN y rects de entrada mal ordenados](#nan-and-poorly-ordered-input-rects)
    -   [NaN como entrada](#nan-as-input)
    -   [RECT de entrada mal ordenados](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Uso de HRESULT

Si una función no está por lotes y puede tener un error en tiempo de ejecución, debe devolver **HRESULT** para indicar un error. Un error en tiempo de ejecución es cualquier error que no se puede evitar en tiempo de diseño, como memoria fuera de memoria.

## <a name="return-value-of-batched-functions"></a>Valor devuelto de las funciones por lotes

Las funciones por lotes en Direct2D son las funciones que se procesan como una sola unidad cuando se llama a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Close.**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) Son los comandos de dibujo entre [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) **y EndDraw** o comandos [**en GeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) Para estas funciones, los errores se notifican en el momento en que se completa el lote. El error se devuelve después **de EndDraw para** los comandos de dibujo y después de **Cerrar** para **GeometrySink.**

RenderTargets deja de dibujar si se establece un estado de error, pero una aplicación puede llamar a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) para restablecer el estado de error y reanudar el dibujo.

**Las funciones Get** **y Set** no tienen ningún valor devuelto. Sin embargo, si una **función Set** tiene una entrada no válida, la capa de depuración genera un mensaje. En este caso, no se establece ningún estado de error y la **función Set** no hace nada.

## <a name="invalid-input"></a>Entrada no válida

Direct2D desreferencia los punteros de salida y los parámetros necesarios, lo que da lugar a infracciones de acceso cuando los punteros no son válidos o **NULL.**

### <a name="output-pointer"></a>Puntero de salida

Direct2D desreferencia un puntero de salida y lo asigna a **NULL** inmediatamente después de entrar en la función. Esto produce una infracción de acceso si un autor de la llamada pasa **NULL** como puntero al valor devuelto. Esta directiva también se aplica a las matrices de punteros. Para otros parámetros de salida, como un struct, la desreferencia se produce más adelante y también produce una infracción de acceso. Sin embargo, hay algunos métodos que tienen punteros de salida opcionales (es decir, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)que no provocarán una infracción de acceso.

### <a name="required-parameter"></a>Parámetro requerido

Si **se pasa NULL** a cualquier función que requiera un valor válido, la función desreferencia el puntero no válido al principio, lo que da lugar a una infracción de acceso. Para los parámetros de entrada opcionales, **NULL** es un valor válido que da como resultado un valor predeterminado razonable.

## <a name="nan-and-poorly-ordered-input-rects"></a>NaN y rects de entrada mal ordenados

En Direct2D, NaN se considera una entrada válida y se ordenan los RECT de entrada mal ordenados.

### <a name="nan-as-input"></a>NaN como entrada

NaN se considera una entrada válida, aunque normalmente da como resultado el primitivo que contiene el NaN no dibujado. La API de Direct2D no proporciona filtrado explícito de NaN para validar la entrada.

### <a name="poorly-ordered-input-rects"></a>RECT de entrada mal ordenados

Los RECT de entrada mal ordenados están ordenados para que las esquinas superior, izquierda e inferior derecha se especifiquen correctamente. Para la salida, los rectángulos vacíos tienen este aspecto: {Infinity, Infinity, FloatMax, FloatMax}.

 

 