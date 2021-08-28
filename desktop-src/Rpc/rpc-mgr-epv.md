---
title: RPC_MGR_EPV (Rpcdce.h)
description: El tipo de datos RPC \_ MGR \_ EPV define un vector de punto de entrada de administrador.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e40b883192adc53b11f9965f1a92f4637b320d32b5fd6909e2b6d615437a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926299"
---
# <a name="rpc_mgr_epv"></a>RPC \_ MGR \_ EPV

El tipo de **datos RPC \_ MGR \_ EPV define** un vector de punto de entrada de administrador.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Miembros

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**if-name**
</dt> <dd>

Especifica el nombre de la interfaz

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**
</dt> <dd>

Especifica el tipo devuelto por la función **Functionname** indicada en el archivo IDL.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Nombrefunción**
</dt> <dd>

Especifica el nombre de la función indicada en el archivo IDL.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**
</dt> <dd>

Especifica los parámetros indicados para la función **Functionname** en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El vector de punto de entrada (EPV) del administrador es una matriz de punteros de función. La matriz contiene punteros a las implementaciones de las funciones especificadas en el archivo IDL. El número de elementos de la matriz se establece en el número de funciones especificadas en el archivo IDL. Una aplicación también puede tener varios EPV, que representan varias implementaciones de las funciones especificadas en la interfaz .

El compilador MIDL genera un tipo de datos **EPV** predeterminado denominado *if-name***\_ SERVER \_ EPV,** donde *if-name* especifica el identificador de interfaz en el archivo IDL. El compilador MIDL inicializa este **EPV** predeterminado para contener punteros de función para cada uno de los procedimientos especificados en el archivo IDL.

Cuando el servidor ofrece varias implementaciones de la misma interfaz, la aplicación de servidor debe declarar e inicializar una variable de tipo *if-name** \_ SERVER \_ EPV** para cada implementación de la interfaz. Cada **EPV** debe contener un punto de entrada (puntero de función) para cada procedimiento definido en el archivo IDL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





