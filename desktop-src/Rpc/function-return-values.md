---
title: Valores devueltos de función
description: Los valores devueltos de función son similares a los parámetros de solo lectura, ya que la aplicación cliente no proporciona sus datos.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676484"
---
# <a name="function-return-values"></a>Valores devueltos de función

Los valores devueltos de función son similares a los parámetros de solo **\[ salida \]** porque la aplicación cliente no proporciona sus datos. Sin embargo, se administran de forma diferente. A diferencia de los parámetros de solo **\[ salida \]**, no es necesario que sean punteros. El procedimiento remoto puede devolver cualquier tipo de datos válido, excepto los punteros de referencia y las uniones no encapsuladas.

Sin embargo, se recomienda el uso de un parámetro **\[ out \]** en lugar de un valor devuelto para tipos de datos complejos. Al devolver tipos de datos complejos, el compilador MIDL generará un código auxiliar del modo/os. Como resultado, se pierde toda la información de comprobación de errores reciente proporcionada por/Robust.

Los valores devueltos de función que son tipos de puntero se asignan mediante el código auxiliar de cliente con una llamada a la [ \_ \_ asignación de usuarios de MIDL](/windows/desktop/Midl/midl-user-allocate-1). En consecuencia, solo se puede aplicar el atributo de puntero único o completo a un tipo de valor devuelto de función de puntero.

 

 