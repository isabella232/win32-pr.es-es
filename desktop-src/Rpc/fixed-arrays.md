---
title: Matrices fijas
description: Si la interfaz especifica una matriz con un número específico de elementos como parámetro, usa una matriz fija. Cuando se usa MIDL, se definen matrices fijas de la misma manera que se definen en C. Especifique el tipo, el nombre y el tamaño de la matriz.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1040e417cc896b9f4bd2271dc69e23033332354357b2aad32053724d94b79035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929984"
---
# <a name="fixed-arrays"></a>Matrices fijas

Si la interfaz especifica una matriz con un número específico de elementos como parámetro, usa una matriz fija. Cuando se usa MIDL, se definen matrices fijas de la misma manera que se definen en C. Especifique el tipo, el nombre y el tamaño de la matriz.

En el ejemplo siguiente se muestra cómo definir una matriz fija.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

Cuando un programa cliente pasa una matriz fija a un programa de servidor, el código auxiliar de cliente envía toda la matriz al código auxiliar del servidor. El código auxiliar del servidor asigna memoria para la matriz y almacena los datos de la matriz que recibe a través de la red en la memoria asignada. A continuación, pasa la matriz al procedimiento remoto en el servidor. El servidor puede modificar los datos de la matriz.

Cuando finaliza el procedimiento remoto, el código auxiliar del servidor devuelve el contenido de la matriz al cliente. El código auxiliar del cliente copia los datos recibidos del código auxiliar del servidor en la matriz original. A continuación, el programa cliente puede usar los datos como lo haría si recibiera los datos de una llamada a procedimiento local.

 

 




