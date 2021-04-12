---
title: midl_user_allocate atributo)
description: La función de asignación de usuarios de MIDL \_ \_ es una función que proporcionan las aplicaciones cliente y servidor para asignar memoria.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate el atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358949"
---
# <a name="midl_user_allocate-attribute"></a><span data-ttu-id="0e56a-104">atributo de asignación de \_ usuarios de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="0e56a-104">midl\_user\_allocate attribute</span></span>

<span data-ttu-id="0e56a-105">La función de **\_ \_ asignación de usuarios de MIDL** es una función que proporcionan las aplicaciones cliente y servidor para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="0e56a-105">The **midl\_user\_allocate** function is a function that client and server applications provide to allocate memory.</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a><span data-ttu-id="0e56a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e56a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e56a-107">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="0e56a-107">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="0e56a-108">Especifica el recuento de bytes que se van a asignar.</span><span class="sxs-lookup"><span data-stu-id="0e56a-108">Specifies the count of bytes to allocate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e56a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e56a-109">Remarks</span></span>

<span data-ttu-id="0e56a-110">Las aplicaciones cliente y las aplicaciones de servidor deben implementar la función de **\_ \_ asignación de usuarios de MIDL** , a menos que se esté compilando en modo de compatibilidad de OSF ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="0e56a-110">Both client applications and server applications must implement the **midl\_user\_allocate** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="0e56a-111">Las aplicaciones y los códigos auxiliares generados llaman a la **\_ \_ asignación de usuarios de MIDL** al tratar con objetos a los que hacen referencia los punteros:</span><span class="sxs-lookup"><span data-stu-id="0e56a-111">Applications and generated stubs call **midl\_user\_allocate** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="0e56a-112">La aplicación de servidor debe llamar a **MIDL \_ User \_ allocate** para asignar memoria para aplicación € ", por ejemplo, al crear un nuevo nodo.</span><span class="sxs-lookup"><span data-stu-id="0e56a-112">The server application should call **midl\_user\_allocate** to allocate memory for the applicationâ€”for example, when creating a new node.</span></span>
-   <span data-ttu-id="0e56a-113">El código auxiliar del servidor llama a la **\_ \_ asignación de usuarios de MIDL** al desserializar los datos señalados en el espacio de direcciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="0e56a-113">The server stub calls **midl\_user\_allocate** when unmarshaling pointed-at data into the server address space.</span></span>
-   <span data-ttu-id="0e56a-114">El código auxiliar de cliente llama a la **\_ \_ asignación de usuario de MIDL** al quitar las referencias de datos del servidor al que hace referencia un puntero de [**salida**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="0e56a-114">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an [**out**](out-idl.md) pointer.</span></span> <span data-ttu-id="0e56a-115">Tenga en cuenta que para **\[** [](in.md) **\]** los punteros in, **\[ out \]** y **\[** [**Unique**](unique.md) **\]** , el código auxiliar de cliente llama a la **\_ \_ asignación de usuario de MIDL** solo si el valor de puntero **\[ único \]** era **null** en la entrada y cambia a un valor distinto de **null** durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="0e56a-115">Note that for **\[**[**in**](in.md)**\]**, **\[out\]**, and **\[**[**unique**](unique.md)**\]** pointers, the client stub calls **midl\_user\_allocate** only if the **\[unique\]** pointer value was **NULL** on input and changes to a non-**NULL** value during the call.</span></span> <span data-ttu-id="0e56a-116">Si el puntero **\[ \] único** no era **null** en la entrada, el código auxiliar del cliente escribe los datos asociados en la memoria existente.</span><span class="sxs-lookup"><span data-stu-id="0e56a-116">If the **\[unique\]** pointer was non-**NULL** on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="0e56a-117">Si el usuario de la **\_ \_ asignación de MIDL** no puede asignar memoria, debe devolver un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="0e56a-117">If **midl\_user\_allocate** fails to allocate memory, it must return a **NULL** pointer.</span></span>

<span data-ttu-id="0e56a-118">Se recomienda que la **\_ \_ asignación de usuarios de MIDL** devuelva un puntero de 8 bytes alineado.</span><span class="sxs-lookup"><span data-stu-id="0e56a-118">It is recommended that **midl\_user\_allocate** return a pointer that is 8 bytes aligned.</span></span>

## <a name="examples"></a><span data-ttu-id="0e56a-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0e56a-119">Examples</span></span>


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a><span data-ttu-id="0e56a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e56a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e56a-121">**allocate**</span><span class="sxs-lookup"><span data-stu-id="0e56a-121">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="0e56a-122">**matrices**</span><span class="sxs-lookup"><span data-stu-id="0e56a-122">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="0e56a-123">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="0e56a-123">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="0e56a-124">Atributos array y Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="0e56a-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e56a-125">**de**</span><span class="sxs-lookup"><span data-stu-id="0e56a-125">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="0e56a-126">**usuario de MIDL \_ \_ gratis**</span><span class="sxs-lookup"><span data-stu-id="0e56a-126">**midl\_user\_free**</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="0e56a-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="0e56a-127">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="0e56a-128">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="0e56a-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="0e56a-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="0e56a-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="0e56a-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="0e56a-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="0e56a-131">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="0e56a-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 