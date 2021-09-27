---
title: HTTP_RESPONSE (Http.h)
description: La versión de la estructura HTTP RESPONSE depende de la versión de la cola de solicitudes que se usa como se muestra a continuación en la cola de solicitudes de LA API del servidor HTTP 1.0. Se trata de una estructura \_ HTTP \_ REQUEST \_ V1. Cola de solicitudes de LA API del servidor HTTP versión 2.0. Se trata de una estructura HTTP \_ REQUEST \_ V2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a2eb4f39dacabaaba25cc9ffa00a67a51386b4
ms.sourcegitcommit: 9af6ac4cb91d550a671511c4c05d970abc20226e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/26/2021
ms.locfileid: "129018347"
---
# <a name="http_response"></a>RESPUESTA \_ HTTP

La versión de la estructura **HTTP \_ RESPONSE** depende de la versión de la cola de solicitudes que se usa de la siguiente manera:

-   HTTP Server API Versión 1.0: [**estructura HTTP \_ RESPONSE \_ V1.**](/windows/win32/api/http/ns-http-http_response_v1)
-   HTTP Server API Versión 2.0: [**estructura HTTP \_ RESPONSE \_ V2.**](/windows/win32/api/http/ns-http-http_response_v2)

No use [**HTTP \_ RESPONSE \_ V1**](/windows/win32/api/http/ns-http-http_response_v1) y [**HTTP RESPONSE \_ \_ V2**](/windows/win32/api/http/ns-http-http_response_v2) directamente en el código; en su lugar, el uso de **HTTP \_ RESPONSE** garantiza que se use la versión adecuada de la estructura en función de la versión de la cola de solicitudes.


```C++
typedef HTTP_RESPONSE_V1 HTTP_RESPONSE;
typedef HTTP_RESPONSE_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**HTTP \_ RESPONSE_V1**
</dt> <dd>

La solicitud era de una cola de solicitudes v1.

</dd> <dt>

**HTTP \_ RESPONSE_V2**
</dt> <dd>

La solicitud era de una cola de solicitudes v2.

</dd> <dt>

**RESPUESTA \_ PHTTP**
</dt> <dd>

Puntero a una **estructura \_ HTTP RESPONSE.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Http.h</dt> </dl> |



 

 





