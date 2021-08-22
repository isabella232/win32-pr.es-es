---
description: El tipo de datos HCRYPTKEY se usa para representar identificadores en claves criptográficas.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78d50f7fb005d877f6520172631b4546b8d498c415de58502defd26831c65fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006443"
---
# <a name="hcryptkey"></a>HCRYPTKEY

El **tipo de datos HCRYPTKEY** se usa para representar identificadores en claves [*criptográficas.*](../secgloss/c-gly.md) Estos identificadores se usan para indicar al módulo CSP qué clave se usa en una operación específica. El módulo CSP no habilita el acceso directo a los valores de clave. En su lugar, el usuario realiza funciones mediante el valor de clave a través del identificador de clave.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
