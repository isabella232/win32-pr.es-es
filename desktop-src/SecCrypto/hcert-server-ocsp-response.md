---
description: Representa un identificador para una respuesta OCSP asociada a una cadena de certificados de servidor.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a694b6165a3fb5f067fd64170b4b0275c3a06dad21d508f616ee63d6b27e4a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006463"
---
# <a name="hcert_server_ocsp_response"></a>RESPUESTA \_ \_ OCSP DEL SERVIDOR HCERT \_

El **tipo de datos \_ HCERT SERVER \_ OCSP \_ RESPONSE** representa un identificador para una respuesta OCSP asociada a una cadena de certificados de servidor.

Este tipo lo usan las siguientes API.

-   [**CertOpenServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [**CertAddRefServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [**CertCloseServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [**CertGetServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 




