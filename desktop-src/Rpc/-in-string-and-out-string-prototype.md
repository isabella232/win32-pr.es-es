---
title: " in, string and out, string Prototype"
description: 'El siguiente prototipo de función usa dos parámetros: un parámetro \ in, string\ y un parámetro \ out, string\.'
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476634"
---
# <a name="in-string-and-out-string-prototype"></a>\[in, string \] and \[ out, string \] Prototype

El siguiente prototipo de función usa dos parámetros: un parámetro de cadena en , un \[ [](/windows/desktop/Midl/in)parámetro [**de**](/windows/desktop/Midl/string) cadena y \] un parámetro \[ [**out**](/windows/desktop/Midl/out-idl), **string.** \]

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

El primer parámetro está \[ [**solo en**](/windows/desktop/Midl/in) \] . Esta cadena de entrada solo se transmite desde el cliente al servidor. El servidor lo usa como base para su posterior procesamiento. La cadena no se modifica y no es necesaria de nuevo por el cliente, por lo que no tiene que devolverse al cliente.

El segundo parámetro, que representa la respuesta del médico, solo \[ [**está**](/windows/desktop/Midl/out-idl) \] fuera. Esta cadena de respuesta solo se transmite desde el servidor al cliente. El tamaño de asignación se proporciona para que los códigos auxiliares del servidor puedan asignar memoria para él. Puesto *que pszOutput* es un puntero ref, el cliente debe tener suficiente memoria \[ [](/windows/desktop/Midl/ref) \] asignada para la cadena antes de la llamada. La cadena de respuesta se escribe en esta área de memoria cuando se devuelve el procedimiento remoto.

 

 