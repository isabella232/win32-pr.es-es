---
description: El tipo de datos HCRYPTKEY se usa para representar los identificadores de las claves criptográficas.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265340"
---
# <a name="hcryptkey"></a>HCRYPTKEY

El **tipo de datos HCRYPTKEY** se usa para representar los identificadores de las claves [*criptográficas.*](../secgloss/c-gly.md) Estos identificadores se usan para indicar al módulo CSP qué clave se usa en una operación específica. El módulo CSP no habilita el acceso directo a los valores de clave. En su lugar, el usuario realiza funciones mediante el valor de clave a través del identificador de clave.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
