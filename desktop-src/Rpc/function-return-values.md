---
title: Valores devueltos de función
description: Los valores devueltos de la función son similares a los parámetros \out\ -only porque la aplicación cliente no proporciona sus datos.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525c63422b058da5267003711efa612814907eb91ced353bd78ee78a820a7377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021005"
---
# <a name="function-return-values"></a>Valores devueltos de función

Los valores devueltos de la función son similares **\[ a los \]** parámetros out-only porque la aplicación cliente no proporciona sus datos. Sin embargo, se administran de forma diferente. A **\[ diferencia de \]** los parámetros out -only, no es necesario que sean punteros. El procedimiento remoto puede devolver cualquier tipo de datos válido, excepto punteros de referencia y uniones nocapsuladas.

Sin embargo, se **\[ recomienda usar un parámetro out \]** en lugar de un valor devuelto para tipos de datos complejos. Al devolver tipos de datos complejos, el compilador MIDL generará un código auxiliar de modo /Os. Como resultado, se pierde toda la información reciente de comprobación de errores proporcionada por /robust.

El código auxiliar de cliente asigna valores devueltos de función que son tipos de puntero con una llamada a [midl \_ user \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). En consecuencia, solo se puede aplicar el atributo de puntero único o completo a un tipo de valor devuelto de función de puntero.

 

 