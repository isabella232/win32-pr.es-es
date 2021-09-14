---
title: RPC_IF_HANDLE (Rpcdce.h)
description: El tipo \_ de datos RPC IF HANDLE declara un identificador de \_ interfaz.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250508"
---
# <a name="rpc_if_handle"></a>RPC \_ IF \_ HANDLE

El **tipo de datos RPC IF \_ \_ HANDLE** declara un identificador de interfaz.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Observaciones

La biblioteca en tiempo de ejecución rpc usa identificadores de interfaz para acceder a la estructura de datos de especificación de interfaz. El compilador MIDL crea automáticamente una estructura de datos de especificación de interfaz a partir de cada archivo IDL y crea una variable global de tipo RPC IF HANDLE para la especificación \_ \_ de interfaz.

El compilador MIDL incluye un identificador de interfaz en cada archivo de encabezado generado para la interfaz. Las funciones que requieren la especificación de interfaz como parámetro muestran un tipo de datos **de RPC \_ IF \_ HANDLE**. El formato de cada nombre de identificador de interfaz es el siguiente:

-   *if-name* \_ ClientIfHandle (para el cliente)
-   *if-name* \_ ServerIfHandle (para el servidor)

La *parte if-name* especifica el identificador de interfaz en el archivo IDL.

Por ejemplo:

hello \_ ClientIfHandle

hello \_ ServerIfHandle

> [!Note]  
> La longitud máxima del nombre del identificador de interfaz es de 31 caracteres.

 

Dado que las partes \_ "ClientIfHandle" y "ServerIfHandle" de los nombres requieren \_ 15 caracteres, el *elemento if-name* no puede tener más de 16 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



 

 





