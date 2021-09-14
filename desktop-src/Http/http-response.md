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
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266287"
---
# <a name="http_response"></a>RESPUESTA \_ HTTP

La versión de la estructura **HTTP \_ RESPONSE** depende de la versión de la cola de solicitudes que se usa de la siguiente manera:

-   Cola de solicitudes de LA API del servidor HTTP versión 1.0: se trata de una [**estructura HTTP \_ REQUEST \_ V1.**](/windows/desktop/api/Http/ns-http-http_request_v1)
-   Cola de solicitudes de LA API del servidor HTTP versión 2.0: se trata de una [**estructura HTTP \_ REQUEST \_ V2.**](/windows/desktop/api/Http/ns-http-http_request_v2)

No use [**HTTP \_ REQUEST \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) y [**HTTP REQUEST \_ \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directamente en el código; en su lugar, el uso de **HTTP \_ RESPONSE** garantiza el uso de la versión adecuada de la estructura en función de la versión de la cola de solicitudes.


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**RESPUESTA \_ HTTP**
</dt> <dd>

La solicitud era de una cola de solicitudes v1.

</dd> <dt>

**RESPUESTA \_ HTTP**
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



 

 





