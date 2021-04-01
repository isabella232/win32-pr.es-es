---
title: Directivas de control de errores de Direct2D
description: 'En este tema se describen las directivas de control de errores de Direct2D. Contiene las siguientes secciones:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, control de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995539"
---
# <a name="direct2d-error-handling-policies"></a>Directivas de control de errores de Direct2D

En este tema se describen las directivas de control de errores de Direct2D. Contiene las siguientes secciones:

-   [Uso de HRESULT](#use-of-hresult)
-   [Valor devuelto de las funciones por lotes](#return-value-of-batched-functions)
-   [Entrada no válida](#invalid-input)
    -   [Puntero de salida](#output-pointer)
    -   [Parámetro obligatorio](#required-parameter)
-   [NaN y RECTÁNGULOs de entrada mal ordenados](#nan-and-poorly-ordered-input-rects)
    -   [NaN como entrada](#nan-as-input)
    -   [RECTÁNGULOs de entrada mal ordenados](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Uso de HRESULT

Si una función no se procesa por lotes y puede tener un error en tiempo de ejecución, debe devolver **HRESULT** para indicar un error. Un error en tiempo de ejecución es cualquier error que no se puede evitar en tiempo de diseño, como memoria insuficiente.

## <a name="return-value-of-batched-functions"></a>Valor devuelto de las funciones por lotes

Las funciones por lotes en Direct2D son las funciones que se procesan como una sola unidad cuando se llama a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) . Son los comandos de dibujo entre los comandos [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y **EndDraw** o de [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). En el caso de estas funciones, se registran errores en el momento en que se completa el lote. El error se devuelve después de **EndDraw** para dibujar comandos y después de **Close** para **GeometrySink**.

RenderTargets detener dibujo si se establece un estado de error, pero una aplicación puede llamar a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) para restablecer el estado de error y reanudar el dibujo.

Las funciones **Get** y **set** no tienen ningún valor devuelto. Sin embargo, si una función de **conjunto** tiene una entrada no válida, la capa de depuración genera un mensaje. En este caso, no se establece ningún estado de error y la función **set** no hace nada.

## <a name="invalid-input"></a>Entrada no válida

Direct2D desreferencia los punteros de salida y los parámetros necesarios, lo que da lugar a infracciones de acceso cuando los punteros no son válidos o son **null**.

### <a name="output-pointer"></a>Puntero de salida

Direct2D desreferencia un puntero de salida y lo asigna a **null** inmediatamente al entrar en la función. Esto produce una infracción de acceso si un llamador pasa **null** como el puntero al valor devuelto. Esta Directiva también se aplica a las matrices de punteros. Para otros parámetros de salida, como un struct, la desreferenciación se produce más tarde y también produce una infracción de acceso. Sin embargo, hay algunos métodos que tienen punteros de salida opcionales (es decir, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) que no producirán una infracción de acceso.

### <a name="required-parameter"></a>Parámetro obligatorio

Si se pasa **null** a cualquier función que requiera un valor válido, la función desreferencia el puntero incorrecto y produce una infracción de acceso. En el caso de los parámetros de entrada opcionales, **null** es un valor válido que da como resultado un valor predeterminado razonable.

## <a name="nan-and-poorly-ordered-input-rects"></a>NaN y RECTÁNGULOs de entrada mal ordenados

En Direct2D, NaN se considera una entrada válida y los RECTÁNGULOs de entrada mal ordenados se ordenan.

### <a name="nan-as-input"></a>NaN como entrada

NaN se considera una entrada válida, aunque normalmente da como resultado el primitivo que contiene NaN que no se dibuja. La API de Direct2D no proporciona un filtrado explícito de NaN para validar la entrada.

### <a name="poorly-ordered-input-rects"></a>RECTÁNGULOs de entrada mal ordenados

Los RECTÁNGULOs de entrada mal ordenados se ordenan para que las esquinas superior, izquierda e inferior se especifiquen correctamente. Para la salida, los rectángulos vacíos tienen el siguiente aspecto: {Infinity, Infinity, FloatMax, FloatMax}.

 

 