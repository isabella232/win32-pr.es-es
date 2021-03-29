---
title: Tipos de puntero predeterminados
description: No es necesario que los punteros tengan una descripción de atributo explícita. Cuando no se proporciona un atributo explícito, el compilador MIDL usa un atributo de puntero predeterminado.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c565fe8019567fd1fe319d7b34287d9729bbe1d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078067"
---
# <a name="default-pointer-types"></a><span data-ttu-id="9b8ae-104">Tipos de puntero predeterminados</span><span class="sxs-lookup"><span data-stu-id="9b8ae-104">Default Pointer Types</span></span>

<span data-ttu-id="9b8ae-105">No es necesario que los punteros tengan una descripción de atributo explícita.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-105">Pointers are not required to have an explicit attribute description.</span></span> <span data-ttu-id="9b8ae-106">Cuando no se proporciona un atributo explícito, el compilador MIDL usa un atributo de puntero predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-106">When an explicit attribute is not provided, the MIDL Compiler uses a default pointer attribute.</span></span>

<span data-ttu-id="9b8ae-107">Los casos predeterminados para los punteros sin atributos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9b8ae-107">The default cases for unattributed pointers are the following:</span></span>

-   <span data-ttu-id="9b8ae-108">Los punteros de nivel superior que aparecen en las listas de parámetros tienen como valor predeterminado \[ [](/windows/desktop/Midl/ref) \] punteros Ref.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-108">Top-level pointers that appear in parameter lists default to \[[**ref**](/windows/desktop/Midl/ref)\] pointers.</span></span>
-   <span data-ttu-id="9b8ae-109">El resto de punteros tiene como valor predeterminado el tipo especificado por el \[ atributo [**\_ default del puntero**](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="9b8ae-109">All other pointers default to the type specified by the \[[**pointer\_default**](/windows/desktop/Midl/pointer-default)\] attribute.</span></span> <span data-ttu-id="9b8ae-110">Cuando no \[ se proporciona ningún atributo **\_ predeterminado de puntero** \] , estos punteros tienen como valor predeterminado el \[ [](/windows/desktop/Midl/unique) \] atributo único cuando el compilador MIDL está en modo de [extensiones de Microsoft](microsoft-rpc-binding-handle-extensions.md) o en el \[ atributo [**ptr**](/windows/desktop/Midl/ptr) \] cuando el compilador MIDL está en modo compatible con DCE.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-110">When no \[**pointer\_default**\] attribute is supplied, these pointers default to the \[ [**unique**](/windows/desktop/Midl/unique) \] attribute when the MIDL compiler is in [Microsoft Extensions](microsoft-rpc-binding-handle-extensions.md) mode or the \[[**ptr**](/windows/desktop/Midl/ptr)\] attribute when the MIDL compiler is in DCE-compatible mode.</span></span>

<span data-ttu-id="9b8ae-111">Cuando un procedimiento remoto devuelve un puntero, el valor devuelto debe ser un \[ puntero [**único**](/windows/desktop/Midl/unique) \] o completo ( \[ [**ptr**](/windows/desktop/Midl/ptr) \] ).</span><span class="sxs-lookup"><span data-stu-id="9b8ae-111">When a remote procedure returns a pointer, the return value must be a \[ [**unique**](/windows/desktop/Midl/unique) \] or full (\[ [**ptr**](/windows/desktop/Midl/ptr) \]) pointer.</span></span>

``` syntax
/* IDL file compiled without /osf */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0),
  pointer_default(ptr)
]
interface MyInterface
{
    typedef long *PLONG;
  
    struct MyCircularList {
        struct MyCircularList *pRight;
        struct MyCircularList *pLeft;
        long Data;
    };

    void Foo1( [in] PLONG p );                   // p is ref
 
    void Foo2( [in] struct MyCircularList *p );  // p is ref, p->pRight and p->pLeft is ptr

    struct MyCircularList *Foo3( void );         // returned pointer is ptr.    
}

[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea46),
  version(1.0)
]
interface MyInterface2
{
    struct MySingleList
       {
       struct MySingleList *pNext;
       long Data;
       };
    void Foo4( [in] struct MySingleList *p );  // p is ref, p->pNext is unique

    struct MySingleList *Foo5( void );         // returned pointer is unique.    
}
```

### <a name="remarks"></a><span data-ttu-id="9b8ae-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b8ae-112">Remarks</span></span>

<span data-ttu-id="9b8ae-113">Para garantizar un comportamiento de atributo de puntero inequívoco, use siempre atributos de puntero explícitos al definir un puntero.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-113">To ensure unambiguous pointer-attribute behavior, always use explicit pointer attributes when defining a pointer.</span></span>

<span data-ttu-id="9b8ae-114">Se recomienda **\[** **\]** usar PTR solo cuando se requiere el alias de puntero.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-114">It is recommended that **\[** ptr **\]** is used only when pointer aliasing is required.</span></span>

 

 