---
description: Representa un identificador para un conjunto de funciones instalables de identificador de objeto (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3926b78359450b780a9952aeae9d957157ebb56973a7f428824b07cbb43e9a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006473"
---
# <a name="hcryptoidfuncset"></a>HCRYPTOIDFUNCSET

El **tipo de datos HCRYPTOIDFUNCSET** representa un identificador para un conjunto de funciones instalables de identificador de objeto (OID). [](../secgloss/o-gly.md) Las [**funciones CryptGetDefaultOIDFunctionAddress,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) [**CryptGetOIDFunctionAddress,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)y [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) usan este tipo de datos.


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
