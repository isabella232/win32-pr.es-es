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
# <a name="rpc_mgr_epv"></a><span data-ttu-id="5a36c-104">\_EPV de administrador de RPC \_</span><span class="sxs-lookup"><span data-stu-id="5a36c-104">RPC\_MGR\_EPV</span></span>

<span data-ttu-id="5a36c-105">El tipo de datos **RPC \_ Mgr \_ EPV** define un vector de punto de entrada del administrador.</span><span class="sxs-lookup"><span data-stu-id="5a36c-105">The data type **RPC\_MGR\_EPV** defines a manager entry-point vector.</span></span>

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a><span data-ttu-id="5a36c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a36c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a36c-107"><span id="if-name"></span><span id="IF-NAME"></span>**If-Name**</span><span class="sxs-lookup"><span data-stu-id="5a36c-107"><span id="if-name"></span><span id="IF-NAME"></span>**if-name**</span></span>
</dt> <dd>

<span data-ttu-id="5a36c-108">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5a36c-108">Specifies the name of the interface</span></span>

</dd> <dt>

<span data-ttu-id="5a36c-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**tipo de valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="5a36c-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**</span></span>
</dt> <dd>

<span data-ttu-id="5a36c-110">Especifica el tipo devuelto por la función **functionname** indicada en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5a36c-110">Specifies the type returned by the function **Functionname** indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="5a36c-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Nombrefunción**</span><span class="sxs-lookup"><span data-stu-id="5a36c-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**</span></span>
</dt> <dd>

<span data-ttu-id="5a36c-112">Especifica el nombre de la función indicada en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5a36c-112">Specifies the name of the function indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="5a36c-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**lista de parámetros**</span><span class="sxs-lookup"><span data-stu-id="5a36c-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**</span></span>
</dt> <dd>

<span data-ttu-id="5a36c-114">Especifica los parámetros indicados para la función **functionname** en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5a36c-114">Specifies the parameters indicated for the function **Functionname** in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a36c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a36c-115">Remarks</span></span>

<span data-ttu-id="5a36c-116">El vector de punto de entrada (EPV) del administrador es una matriz de punteros de función.</span><span class="sxs-lookup"><span data-stu-id="5a36c-116">The manager entry-point vector (EPV) is an array of function pointers.</span></span> <span data-ttu-id="5a36c-117">La matriz contiene punteros a las implementaciones de las funciones especificadas en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5a36c-117">The array contains pointers to the implementations of the functions specified in the IDL file.</span></span> <span data-ttu-id="5a36c-118">El número de elementos de la matriz se establece en el número de funciones especificadas en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5a36c-118">The number of elements in the array is set to the number of functions specified in the IDL file.</span></span> <span data-ttu-id="5a36c-119">Una aplicación también puede tener varios EPVs, que representan varias implementaciones de las funciones especificadas en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5a36c-119">An application can also have multiple EPVs, representing multiple implementations of the functions specified in the interface.</span></span>

<span data-ttu-id="5a36c-120">El compilador MIDL genera un tipo de datos **EPV** predeterminado denominado \* if-name \***\_ Server \_ EPV**, donde *-Name* especifica el identificador de interfaz en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5a36c-120">The MIDL compiler generates a default **EPV** data type named \*if-name\***\_SERVER\_EPV**, where *if-name* specifies the interface identifier in the IDL file.</span></span> <span data-ttu-id="5a36c-121">El compilador MIDL inicializa este **EPV** predeterminado para contener punteros de función para cada uno de los procedimientos especificados en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5a36c-121">The MIDL compiler initializes this default **EPV** to contain function pointers for each of the procedures specified in the IDL file.</span></span>

<span data-ttu-id="5a36c-122">Cuando el servidor ofrece varias implementaciones de la misma interfaz, la aplicación de servidor debe declarar e inicializar una variable de tipo *If-name \* \* \* \_ Server \_ EPV*\* para cada implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5a36c-122">When the server offers multiple implementations of the same interface, the server application must declare and initialize one variable of type *if-name\*\*\*\_SERVER\_EPV*\* for each implementation of the interface.</span></span> <span data-ttu-id="5a36c-123">Cada **EPV** debe contener un punto de entrada (puntero de función) para cada procedimiento definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5a36c-123">Each **EPV** must contain one entry point (function pointer) for each procedure defined in the IDL file.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a36c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a36c-124">Requirements</span></span>



| <span data-ttu-id="5a36c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a36c-125">Requirement</span></span> | <span data-ttu-id="5a36c-126">Value</span><span class="sxs-lookup"><span data-stu-id="5a36c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a36c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a36c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5a36c-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5a36c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5a36c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a36c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5a36c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a36c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5a36c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a36c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a36c-132"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a36c-132"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a36c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a36c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a36c-134">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="5a36c-134">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[<span data-ttu-id="5a36c-135">**RpcServerRegisterIf2**</span><span class="sxs-lookup"><span data-stu-id="5a36c-135">**RpcServerRegisterIf2**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[<span data-ttu-id="5a36c-136">**RpcServerRegisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="5a36c-136">**RpcServerRegisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[<span data-ttu-id="5a36c-137">**RpcServerUnregisterIf**</span><span class="sxs-lookup"><span data-stu-id="5a36c-137">**RpcServerUnregisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[<span data-ttu-id="5a36c-138">**RpcServerUnregisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="5a36c-138">**RpcServerUnregisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





