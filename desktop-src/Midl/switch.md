---
title: atributo switch
description: La palabra clave switch selecciona el discriminante de una Unión encapsulada \_ .
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- atributo de modificador MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994733"
---
# <a name="switch-attribute"></a><span data-ttu-id="4b217-104">atributo switch</span><span class="sxs-lookup"><span data-stu-id="4b217-104">switch attribute</span></span>

<span data-ttu-id="4b217-105">La palabra clave **Switch** selecciona el discriminante de una [**\_ Unión encapsulada**](encapsulated-unions.md).</span><span class="sxs-lookup"><span data-stu-id="4b217-105">The **switch** keyword selects the discriminant for an [**encapsulated\_union**](encapsulated-unions.md).</span></span>

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a><span data-ttu-id="4b217-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b217-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b217-107">*tipo de conmutador*</span><span class="sxs-lookup"><span data-stu-id="4b217-107">*switch-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4b217-108">Especifica un tipo [**int**](int.md), [**Char**](-char.md), [**enum**](enum.md) o un identificador que se resuelve en uno de estos tipos.</span><span class="sxs-lookup"><span data-stu-id="4b217-108">Specifies an [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) type, or an identifier that resolves to one of these types.</span></span>

</dd> <dt>

<span data-ttu-id="4b217-109">*cambiar nombre*</span><span class="sxs-lookup"><span data-stu-id="4b217-109">*switch-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4b217-110">Especifica el nombre de la variable de tipo *Switch-Type* que actúa como discriminante de Unión.</span><span class="sxs-lookup"><span data-stu-id="4b217-110">Specifies the name of the variable of type *switch-type* that acts as the union discriminant.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4b217-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4b217-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="4b217-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b217-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b217-113">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="4b217-113">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4b217-114">Uniones no encapsuladas</span><span class="sxs-lookup"><span data-stu-id="4b217-114">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="4b217-115">**el modificador \_ es**</span><span class="sxs-lookup"><span data-stu-id="4b217-115">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="4b217-116">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="4b217-116">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="4b217-117">**Unión**</span><span class="sxs-lookup"><span data-stu-id="4b217-117">**union**</span></span>](union.md)
</dt> </dl>

 

 




