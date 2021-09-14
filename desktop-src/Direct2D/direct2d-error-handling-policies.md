---
title: Directivas de control de errores de Direct2D
description: 'En este tema se describen las directivas de control de errores de Direct2D. Contiene las siguientes secciones:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, control de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163382"
---
# <a name="direct2d-error-handling-policies"></a>Directivas de control de errores de Direct2D

En este tema se describen las directivas de control de errores de Direct2D. Contiene las siguientes secciones:

-   [Uso de HRESULT](#use-of-hresult)
-   [Valor devuelto de las funciones por lotes](#return-value-of-batched-functions)
-   [Entrada no válida](#invalid-input)
    -   [Puntero de salida](#output-pointer)
    -   [Parámetro requerido](#required-parameter)
-   [NaN y RECT de entrada mal ordenados](#nan-and-poorly-ordered-input-rects)
    -   [NaN como entrada](#nan-as-input)
    -   [RECT de entrada mal ordenados](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Uso de HRESULT

Si una función no está por lotes y puede tener un error en tiempo de ejecución, debe devolver **HRESULT** para indicar un error. Un error en tiempo de ejecución es cualquier error que no se puede evitar en tiempo de diseño, como memoria fuera de memoria.

## <a name="return-value-of-batched-functions"></a>Valor devuelto de las funciones por lotes

Las funciones por lotes en Direct2D son las funciones que se procesan como una sola unidad cuando se llama a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Close.**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) Son los comandos de dibujo entre [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) **y EndDraw** o comandos [**en GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Para estas funciones, los errores se notifican en el momento en que se completa el lote. El error se devuelve después **de EndDraw para** los comandos de dibujo y después de **Cerrar** para **GeometrySink.**

RenderTargets deja de dibujar si se establece un estado de error, pero una aplicación puede llamar a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) para restablecer el estado de error y reanudar el dibujo.

**Las funciones Get** **y Set** no tienen ningún valor devuelto. Sin embargo, si una **función Set** tiene una entrada no válida, la capa de depuración genera un mensaje. En este caso, no se establece ningún estado de error y la **función Set** no hace nada.

## <a name="invalid-input"></a>Entrada no válida

Direct2D desreferencia punteros de salida y parámetros necesarios que resultan en infracciones de acceso cuando los punteros no son válidos o **NULL.**

### <a name="output-pointer"></a>Puntero de salida

Direct2D desreferencia un puntero de salida y lo asigna a **NULL** inmediatamente después de entrar en la función. Esto provoca una infracción de acceso si un llamador pasa **NULL** como puntero al valor devuelto. Esta directiva también se aplica a las matrices de punteros. Para otros parámetros de salida, como un struct, la desreferencia se produce más adelante y también produce una infracción de acceso. Sin embargo, hay algunos métodos que tienen punteros de salida opcionales (es decir, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)que no provocarán una infracción de acceso.

### <a name="required-parameter"></a>Parámetro requerido

Si se pasa **NULL** a cualquier función que requiera un valor válido, la función desreferencia el puntero no válido al principio, lo que da lugar a una infracción de acceso. Para los parámetros de entrada opcionales, **NULL** es un valor válido que da como resultado algún valor predeterminado razonable.

## <a name="nan-and-poorly-ordered-input-rects"></a>NaN y RECT de entrada mal ordenados

En Direct2D, NaN se considera una entrada válida y los RECT de entrada mal ordenados están ordenados.

### <a name="nan-as-input"></a>NaN como entrada

NaN se considera una entrada válida, aunque normalmente da como resultado la primitiva que contiene el NaN no dibujado. La API de Direct2D no proporciona filtrado explícito de NaN para validar la entrada.

### <a name="poorly-ordered-input-rects"></a>RECT de entrada mal ordenados

Los RECT de entrada mal ordenados se ordenan para que las esquinas superior, izquierda e inferior derecha se especifiquen correctamente. Para la salida, los rectángulos vacíos tienen este aspecto: {Infinity, Infinity, FloatMax, FloatMax}.

 

 