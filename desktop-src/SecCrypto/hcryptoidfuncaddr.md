---
description: Representa un identificador para una función instalable de identificador de objeto (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171018"
---
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

El **tipo de datos HCRYPTOIDFUNCADDR representa** un identificador para una función instalable de identificador de objeto (OID). [](../secgloss/o-gly.md) Las [**funciones CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)y [**CryptFreeOIDFunctionAddress,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) y la estructura [**CERT STORE \_ \_ PROV \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) usan este tipo de datos.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
