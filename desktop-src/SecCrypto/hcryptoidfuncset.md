---
description: Representa un identificador para un conjunto de funciones instalables de identificador de objeto (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265332"
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
| Encabezado<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
