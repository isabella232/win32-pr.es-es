---
title: RPC_MGR_EPV (Rpcdce. h)
description: El tipo de datos RPC \_ Mgr \_ EPV define un vector de punto de entrada del administrador.
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
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801310"
---
# <a name="rpc_mgr_epv"></a>\_EPV de administrador de RPC \_

El tipo de datos **RPC \_ Mgr \_ EPV** define un vector de punto de entrada del administrador.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Miembros

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**If-Name**
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**tipo de valor devuelto**
</dt> <dd>

Especifica el tipo devuelto por la función **functionname** indicada en el archivo IDL.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Nombrefunción**
</dt> <dd>

Especifica el nombre de la función indicada en el archivo IDL.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**lista de parámetros**
</dt> <dd>

Especifica los parámetros indicados para la función **functionname** en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El vector de punto de entrada (EPV) del administrador es una matriz de punteros de función. La matriz contiene punteros a las implementaciones de las funciones especificadas en el archivo IDL. El número de elementos de la matriz se establece en el número de funciones especificadas en el archivo IDL. Una aplicación también puede tener varios EPVs, que representan varias implementaciones de las funciones especificadas en la interfaz.

El compilador MIDL genera un tipo de datos **EPV** predeterminado denominado * if-name ***\_ Server \_ EPV**, donde *-Name* especifica el identificador de interfaz en el archivo IDL. El compilador MIDL inicializa este **EPV** predeterminado para contener punteros de función para cada uno de los procedimientos especificados en el archivo IDL.

Cuando el servidor ofrece varias implementaciones de la misma interfaz, la aplicación de servidor debe declarar e inicializar una variable de tipo *If-name * * * \_ Server \_ EPV** para cada implementación de la interfaz. Cada **EPV** debe contener un punto de entrada (puntero de función) para cada procedimiento definido en el archivo IDL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h (incluir RPC. h)</dt> </dl> |



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

 

 





