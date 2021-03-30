---
title: " in, String y out, prototipo de cadena"
description: 'El prototipo de función siguiente usa dos parámetros: \ in, String \ Parameter y un parámetro \ out, String \.'
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995570"
---
# <a name="in-string-and-out-string-prototype"></a>\[in, String \] y \[ out, prototipo de cadena \]

El prototipo de función siguiente usa dos parámetros: \[ [**en**](/windows/desktop/Midl/in), parámetro de [**cadena**](/windows/desktop/Midl/string) \] y un \[ parámetro [**out**](/windows/desktop/Midl/out-idl)de **cadena** \] .

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

El primer parámetro es \[ solo [**en**](/windows/desktop/Midl/in) \] . Esta cadena de entrada solo se transmite desde el cliente al servidor. El servidor lo utiliza como base para su posterior procesamiento. La cadena no se modifica y el cliente no la necesita, por lo que no tiene que devolverse al cliente.

El segundo parámetro, que representa la respuesta del médico, \[ solo está [**fuera**](/windows/desktop/Midl/out-idl) \] . Esta cadena de respuesta solo se transmite desde el servidor al cliente. Se proporciona el tamaño de asignación para que el código auxiliar del servidor pueda asignar memoria para él. Puesto que *pszOutput* es un puntero de \[ [**referencia**](/windows/desktop/Midl/ref) \] , el cliente debe tener suficiente memoria asignada para la cadena antes de la llamada. La cadena de respuesta se escribe en esta área de memoria cuando se devuelve el procedimiento remoto.

 

 