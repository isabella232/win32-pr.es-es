---
description: Representa un identificador de una función instalable de identificador de objeto (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb36bdd98332842d89533c9c34a880aecdc8555cd64bb03888c0bd146cea3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006553"
---
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

El **tipo de datos HCRYPTOIDFUNCADDR** representa un identificador para una función instalable de identificador de objeto (OID). [](../secgloss/o-gly.md) Las [**funciones CryptGetDefaultOIDFunctionAddress,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)y [**CryptFreeOIDFunctionAddress,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) y la estructura [**CERT STORE \_ \_ PROV \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) usan este tipo de datos.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
