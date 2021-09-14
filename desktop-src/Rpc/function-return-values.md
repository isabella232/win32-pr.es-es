---
title: Valores devueltos de función
description: Los valores devueltos de función son similares a \out\ -only parameters porque la aplicación cliente no proporciona sus datos.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259796"
---
# <a name="function-return-values"></a>Valores devueltos de función

Los valores devueltos de función son similares **\[ a los \]** parámetros out -only porque la aplicación cliente no proporciona sus datos. Sin embargo, se administran de forma diferente. A **\[ diferencia de \]** los parámetros out -only, no es necesario que sean punteros. El procedimiento remoto puede devolver cualquier tipo de datos válido, excepto punteros de referencia y uniones no superadas.

Sin embargo, se **\[ recomienda usar un parámetro out \]** en lugar de un valor devuelto para tipos de datos complejos. Al devolver tipos de datos complejos, el compilador midl generará un código auxiliar de modo /Os. Como resultado, se pierde toda la información reciente de comprobación de errores proporcionada por /robust.

El código auxiliar de cliente asigna los valores devueltos de función que son tipos de puntero con una llamada a [midl \_ user \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). En consecuencia, solo se puede aplicar el atributo de puntero único o completo a un tipo de valor devuelto de función de puntero.

 

 