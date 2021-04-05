---
title: RPC_IF_HANDLE (Rpcdce. h)
description: El \_ tipo de datos RPC if \_ Handle declara un identificador de interfaz.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996856"
---
# <a name="rpc_if_handle"></a>identificador de RPC \_ If \_

El tipo de datos **RPC \_ If \_ Handle** declara un identificador de interfaz.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Observaciones

La biblioteca en tiempo de ejecución de RPC utiliza identificadores de interfaz para tener acceso a la estructura de datos de la especificación de interfaz. El compilador MIDL crea automáticamente una estructura de datos de especificación de interfaz a partir de cada archivo IDL y crea una variable global de tipo RPC \_ si es \_ el identificador de la especificación de interfaz.

El compilador MIDL incluye un identificador de interfaz en cada archivo de encabezado generado para la interfaz. Las funciones que requieren la especificación de interfaz como parámetro muestran un tipo de datos de **RPC si es el \_ \_ identificador**. El formato de cada nombre de identificador de interfaz es el siguiente:

-   *If-Name* \_ ClientIfHandle (para el cliente)
-   *If-Name* \_ ServerIfHandle (para el servidor)

La parte *If-Name* especifica el identificador de interfaz en el archivo IDL.

Por ejemplo:

Hola \_ ClientIfHandle

Hola \_ ServerIfHandle

> [!Note]  
> La longitud máxima del nombre del identificador de interfaz es de 31 caracteres.

 

Dado que las \_ partes "ClientIfHandle" y " \_ ServerIfHandle" de los nombres requieren 15 caracteres, el elemento *If-Name* no puede tener más de 16 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h (incluir RPC. h)</dt> </dl> |



 

 





