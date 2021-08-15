---
title: RPC_IF_HANDLE (Rpcdce.h)
description: El tipo de datos RPC \_ IF HANDLE declara un identificador de \_ interfaz.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4652fbd08c583ad0a33638e52face9569e6ff701cb6dc2b775c7060134b60437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926444"
---
# <a name="rpc_if_handle"></a>RPC \_ IF \_ HANDLE

El **tipo de datos RPC IF \_ \_ HANDLE** declara un identificador de interfaz.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Comentarios

La biblioteca en tiempo de ejecución de RPC usa identificadores de interfaz para acceder a la estructura de datos de especificación de interfaz. El compilador MIDL crea automáticamente una estructura de datos de especificación de interfaz a partir de cada archivo IDL y crea una variable global de tipo RPC IF HANDLE para la especificación \_ \_ de interfaz.

El compilador MIDL incluye un identificador de interfaz en cada archivo de encabezado generado para la interfaz. Las funciones que requieren la especificación de interfaz como parámetro muestran un tipo de datos **de RPC \_ IF \_ HANDLE**. El formato de cada nombre de identificador de interfaz es el siguiente:

-   *if-name* \_ ClientIfHandle (para el cliente)
-   *if-name* \_ ServerIfHandle (para el servidor)

La *parte if-name* especifica el identificador de interfaz en el archivo IDL.

Por ejemplo:

hello \_ ClientIfHandle

hello \_ ServerIfHandle

> [!Note]  
> La longitud máxima del nombre del identificador de interfaz es de 31 caracteres.

 

Dado que las \_ partes "ClientIfHandle" y "ServerIfHandle" de los nombres requieren 15 caracteres, el elemento \_ *if-name* no puede tener más de 16 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



 

 





