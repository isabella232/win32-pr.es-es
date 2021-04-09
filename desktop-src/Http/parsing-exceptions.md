---
title: Analizar excepciones
description: La API del servidor HTTP proporciona claves del registro para admitir el análisis de excepciones a la especificación HTTP/1.1 por compatibilidad con versiones anteriores.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analizar excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994336"
---
# <a name="parsing-exceptions"></a>Analizar excepciones

La API del servidor HTTP proporciona claves del registro para admitir el análisis de excepciones a la especificación HTTP/1.1 por compatibilidad con versiones anteriores. Estas excepciones no están habilitadas de forma predeterminada y solo deben habilitarse en caso de que el servidor experimente problemas de compatibilidad con clientes HTTP. Estos valores se crean en la siguiente ubicación del registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

En la tabla siguiente se enumeran las claves del registro proporcionadas para admitir las excepciones que se muestran. Para habilitar una excepción, establezca el valor de clave correspondiente en 1 y reinicie el servicio HTTP.



| Nombre de clave                              | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)     | Permite que el analizador HTTP acepte nombres de encabezado con caracteres separadores como '? '.                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)    | Permite que el analizador HTTP acepte valores de encabezado con caracteres de control sin formato (sin escape).                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)     | Permite que el analizador HTTP acepte métodos o verbos HTTP en minúsculas, como "Get".                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD) | Permite que el analizador HTTP acepte caracteres de control en abspath y cadenas de consulta de la dirección URL. En el caso de una dirección URL absoluta, no se permitirán caracteres de control en el nombre de host. Todos los tipos de direcciones URL, es decir, UTF8, DBCS y ANSI, permitirán caracteres de control. Se permitirán todos los caracteres de control ASCII excepto NUL (0x00), LF (0x0a), CR (0x0d) y horizontal (0x09). |



 

 

 




