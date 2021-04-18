---
title: atributo void
description: El tipo de base void indica un procedimiento sin argumentos o un procedimiento que no devuelve un valor de resultado.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- atributo void de MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665761"
---
# <a name="void-attribute"></a><span data-ttu-id="d7900-104">atributo void</span><span class="sxs-lookup"><span data-stu-id="d7900-104">void attribute</span></span>

<span data-ttu-id="d7900-105">El tipo de base **void** indica un procedimiento sin argumentos o un procedimiento que no devuelve un valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="d7900-105">The base type **void** indicates a procedure with no arguments or a procedure that does not return a result value.</span></span>

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="d7900-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7900-107">*nombre de función*</span><span class="sxs-lookup"><span data-stu-id="d7900-107">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d7900-108">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="d7900-108">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="d7900-109">*lista de parámetros*</span><span class="sxs-lookup"><span data-stu-id="d7900-109">*parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d7900-110">Especifica la lista de parámetros que se pasan a la función junto con los tipos de parámetros y atributos de parámetro asociados.</span><span class="sxs-lookup"><span data-stu-id="d7900-110">Specifies the list of parameters passed to the function along with the associated parameter types and parameter attributes.</span></span>

</dd> <dt>

<span data-ttu-id="d7900-111">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="d7900-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d7900-112">Especifica el nombre del tipo devuelto por la función.</span><span class="sxs-lookup"><span data-stu-id="d7900-112">Specifies the name of the type returned by the function.</span></span>

</dd> <dt>

<span data-ttu-id="d7900-113">*context-Handle-type*</span><span class="sxs-lookup"><span data-stu-id="d7900-113">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d7900-114">Especifica el nombre del tipo que toma el atributo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d7900-114">Specifies the name of the type that takes the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7900-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7900-115">Remarks</span></span>

<span data-ttu-id="d7900-116">El tipo de **puntero \* void**, que en C describe un puntero genérico que se puede convertir para representar cualquier tipo de puntero, está limitado en MIDL a su uso con la palabra clave de **\[ \_ identificador \] de contexto** .</span><span class="sxs-lookup"><span data-stu-id="d7900-116">The pointer type **void \***, which in C describes a generic pointer that can be cast to represent any pointer type, is limited in MIDL to its use with the **\[context\_handle\]** keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="d7900-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d7900-117">Examples</span></span>

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a><span data-ttu-id="d7900-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7900-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7900-119">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="d7900-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="d7900-120">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="d7900-120">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="d7900-121">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="d7900-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




