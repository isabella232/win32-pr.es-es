---
title: Analizar excepciones
description: HTTP Server API proporciona claves del Registro para admitir el análisis de excepciones a la especificación HTTP/1.1 para la compatibilidad con versiones anteriores.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analizar excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b546c5473641bbd5d719908903c2d9e19db25ade2ff6677a5ce5ec7ea472d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950734"
---
# <a name="parsing-exceptions"></a>Analizar excepciones

HTTP Server API proporciona claves del Registro para admitir el análisis de excepciones a la especificación HTTP/1.1 para la compatibilidad con versiones anteriores. Estas excepciones no están habilitadas de forma predeterminada y solo deben habilitarse caso por caso, cuando el servidor experimenta problemas de compatibilidad con clientes HTTP. Estos valores se crean en la siguiente ubicación del Registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

En la tabla siguiente se enumeran las claves del Registro proporcionadas para admitir las excepciones enumeradas. Para habilitar una excepción, establezca el valor de clave correspondiente en 1 y reinicie el servicio HTTP.



| Nombre de clave                              | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)     | Permite que el analizador HTTP acepte nombres de encabezado con caracteres separadores como "?".                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)    | Permite que el analizador HTTP acepte valores de encabezado con caracteres de control sin formato (sin caracteres).                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)     | Permite que el analizador HTTP acepte métodos o verbos HTTP en minúsculas, como "get".                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD) | Permite que el analizador HTTP acepte caracteres de control en las cadenas abspath y query de la dirección URL. En el caso de una dirección URL absoluta, no se permitirán caracteres de control en el nombre de host. Todos los tipos de direcciones URL, es decir, UTF8, DBCS y ANSI, permitirán caracteres de control. Se permitirán todos los caracteres de control ASCII excepto NUL (0x00), LF (0x0a), CR (0x0d) y Horizontal Tab(0x09). |



 

 

 




