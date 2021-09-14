---
description: Se usa como identificador para un proveedor de servicios criptográficos CryptoAPI (CSP) o CSP de CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265327"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>IDENTIFICADOR DE CLAVE HCRYPTPROV \_ \_ O NCRYPT \_ \_

El **tipo de datos HCRYPTPROV O \_ \_ NCRYPT KEY \_ \_ HANDLE** se usa como identificador para un proveedor de servicios criptográficos [*CryptoAPI*](../secgloss/c-gly.md) (CSP) o CSP de CNG. Este identificador debe ser un [**identificador HCRYPTPROV**](hcryptprov.md) creado mediante la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) o un identificador **NCRYPT \_ KEY \_ HANDLE** creado mediante la función [**NCryptOpenKey.**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) Las nuevas aplicaciones siempre deben pasar el identificador **de NCRYPT \_ KEY \_ HANDLE** a un CSP de CNG.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
