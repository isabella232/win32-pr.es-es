---
description: Se usa como identificador de un proveedor de servicios criptográficos (CSP) cryptoAPI o CSP de CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982ab2a37c1a2d6035f76cac5c55dcdae44c4cf38f86138c52590c73724b53e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006343"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>IDENTIFICADOR DE CLAVE HCRYPTPROV \_ \_ O NCRYPT \_ \_

El tipo de datos **HCRYPTPROV \_ O \_ NCRYPT \_ KEY \_ HANDLE** se usa como identificador para un proveedor de servicios criptográficos [*CryptoAPI*](../secgloss/c-gly.md) (CSP) o CSP de CNG. Este identificador debe ser un identificador [**HCRYPTPROV**](hcryptprov.md) creado mediante la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) o un identificador **NCRYPT \_ KEY \_ HANDLE** creado mediante la función [**NCryptOpenKey.**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) Las nuevas aplicaciones siempre deben pasar el identificador **NCRYPT \_ KEY \_ HANDLE** a un CSP de CNG.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
