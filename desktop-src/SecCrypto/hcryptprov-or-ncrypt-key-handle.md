---
description: Se utiliza como identificador de un proveedor de servicios criptográficos (CSP) de CryptoAPI o CSP de CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668210"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>\_identificador de clave HCRYPTPROV o \_ NCRYPT \_ \_

El tipo de datos de **\_ identificador de clave HCRYPTPROV o \_ NCRYPT \_ \_** se utiliza como identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) de CryptoAPI o un CSP de CNG. Este identificador debe ser un identificador de [**HCRYPTPROV**](hcryptprov.md) que se haya creado mediante la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) o un identificador de **\_ \_ identificador de clave NCRYPT** que se haya creado mediante la función [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) . Las nuevas aplicaciones siempre deben pasar el identificador de **\_ \_ identificador de clave NCRYPT** a un CSP de CNG.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
