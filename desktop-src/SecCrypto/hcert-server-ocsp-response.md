---
description: Representa un identificador para una respuesta OCSP asociada a una cadena de certificados de servidor.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265375"
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
| Encabezado<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 




