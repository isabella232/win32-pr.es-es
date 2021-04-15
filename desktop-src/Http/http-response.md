---
title: HTTP_RESPONSE (http. h)
description: La versión de la \_ estructura de respuesta http depende de la versión de la cola de solicitudes utilizada como sigue la API de servidor http versión 1,0, que es una \_ estructura de solicitud HTTP \_ v1. API de servidor HTTP versión 2,0 cola de solicitudes es una \_ estructura de solicitud HTTP \_ V2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422183"
---
# <a name="http_response"></a>\_respuesta http

La versión de la estructura de **\_ respuesta http** depende de la versión de la cola de solicitudes utilizada como se indica a continuación:

-   API de servidor HTTP versión 1,0 cola de solicitudes: se trata de una estructura de [**\_ solicitud HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) .
-   API de servidor HTTP versión 2,0 cola de solicitudes: se trata de una estructura de [**\_ solicitud HTTP \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) .

No use la [**\_ solicitud HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) y [**la \_ solicitud HTTP \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directamente en el código; mediante el uso de la **\_ respuesta http** , se asegura de que se usa la versión adecuada de la estructura en función de la versión de la cola de solicitudes.


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**\_respuesta http**
</dt> <dd>

La solicitud fue de una cola de solicitudes v1.

</dd> <dt>

**\_respuesta http**
</dt> <dd>

La solicitud fue de una cola de solicitudes V2.

</dd> <dt>

**respuesta de PHTTP \_**
</dt> <dd>

Puntero a una estructura de **\_ respuesta http** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Http. h</dt> </dl> |



 

 





