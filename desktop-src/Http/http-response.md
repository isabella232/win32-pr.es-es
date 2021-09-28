---
title: HTTP_RESPONSE (Http.h)
description: La versión de la estructura HTTP \_ RESPONSE depende de la versión de la cola de solicitudes utilizada por la API del servidor HTTP. La versión 1.0 usa la estructura HTTP \_ RESPONSE \_ V1. La versión 2.0 usa la estructura HTTP \_ RESPONSE \_ V2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- _HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 344569e6efae5706c3bc1cc238657c12230be2b1
ms.sourcegitcommit: e3dd89486530e3657279bee8d66d923b613703e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2021
ms.locfileid: "129146743"
---
# <a name="http_response"></a>RESPUESTA \_ HTTP

La versión de la estructura **HTTP \_ RESPONSE** depende de la versión de la cola de solicitudes que se usa de la siguiente manera:

-   API de servidor HTTP versión 1.0: [**estructura HTTP \_ RESPONSE \_ V1.**](/windows/win32/api/http/ns-http-http_response_v1)
-   API de servidor HTTP versión 2.0: [**estructura HTTP \_ RESPONSE \_ V2.**](/windows/win32/api/http/ns-http-http_response_v2)

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

Puntero a una **estructura \_ DE RESPUESTA HTTP.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Http.h</dt> </dl> |



 

 





