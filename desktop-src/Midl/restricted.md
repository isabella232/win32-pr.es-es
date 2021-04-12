---
title: restricted (atributo)
description: El atributo \ Restricted \ especifica que una biblioteca, o un miembro de un módulo, una interfaz o una dispinterface, no se puede llamar arbitrariamente.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- MIDL de atributo restringido
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420647"
---
# <a name="restricted-attribute"></a><span data-ttu-id="95e6e-104">restricted (atributo)</span><span class="sxs-lookup"><span data-stu-id="95e6e-104">restricted attribute</span></span>

<span data-ttu-id="95e6e-105">El atributo **\[ Restricted \]** especifica que una biblioteca, o miembro de un módulo, una interfaz o una dispinterface, no se puede llamar arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="95e6e-105">The **\[restricted\]** attribute specifies that a library, or member of a module, interface, or dispinterface cannot be called arbitrarily.</span></span>

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a><span data-ttu-id="95e6e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95e6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e6e-107">*otros: atributos*</span><span class="sxs-lookup"><span data-stu-id="95e6e-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="95e6e-108">Cero o más atributos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="95e6e-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="95e6e-109">*tipo de instrucción*</span><span class="sxs-lookup"><span data-stu-id="95e6e-109">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="95e6e-110">Uno de los siguientes: [**Library**](library.md), [**Module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="95e6e-110">One of the following: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="95e6e-111">*nombre de instrucción*</span><span class="sxs-lookup"><span data-stu-id="95e6e-111">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="95e6e-112">Identificador por el que el software hace referencia a esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="95e6e-112">The identifier by which the software refers to this statement.</span></span>

</dd> <dt>

<span data-ttu-id="95e6e-113">*Figura*</span><span class="sxs-lookup"><span data-stu-id="95e6e-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="95e6e-114">Elementos del lenguaje MIDL que definen el contenido de esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="95e6e-114">MIDL language elements that define the contents of this statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95e6e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95e6e-115">Remarks</span></span>

<span data-ttu-id="95e6e-116">Este atributo permite controlar el acceso a los elementos de interfaces, bibliotecas, módulos e interfaces dispinterface.</span><span class="sxs-lookup"><span data-stu-id="95e6e-116">This attribute enables you to control access to elements of interfaces, libraries, modules, and dispinterfaces.</span></span> <span data-ttu-id="95e6e-117">Por ejemplo, puede impedir que un elemento de datos sea utilizado por un programador de macros.</span><span class="sxs-lookup"><span data-stu-id="95e6e-117">For example, it can prevent a data item from being used by a macro programmer.</span></span> <span data-ttu-id="95e6e-118">Puede aplicar este atributo a un miembro de una [**coclase**](coclass.md), independientemente de si el miembro es una interfaz dispinterface o una interfaz, e independientemente de si el miembro es un receptor (entrante) o de origen (saliente).</span><span class="sxs-lookup"><span data-stu-id="95e6e-118">You can apply this attribute to a member of a [**coclass**](coclass.md), independent of whether the member is a dispinterface or interface, and independent of whether the member is a sink (incoming) or source (outgoing).</span></span> <span data-ttu-id="95e6e-119">Un miembro de una **coclase** no puede tener los atributos **\[ restringidos \]** y **\[ predeterminados \]** .</span><span class="sxs-lookup"><span data-stu-id="95e6e-119">A member of a **coclass** cannot have both the **\[restricted\]** and **\[default\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="95e6e-120">Marcas</span><span class="sxs-lookup"><span data-stu-id="95e6e-120">Flags</span></span>

<span data-ttu-id="95e6e-121">IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED</span><span class="sxs-lookup"><span data-stu-id="95e6e-121">IMPLTYPEFLAG\_FRESTRICTED, FUNCFLAG\_FRESTRICTED</span></span>

## <a name="examples"></a><span data-ttu-id="95e6e-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="95e6e-122">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a><span data-ttu-id="95e6e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="95e6e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e6e-124">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="95e6e-124">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="95e6e-125">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="95e6e-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="95e6e-126">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="95e6e-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="95e6e-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="95e6e-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="95e6e-128">**destina**</span><span class="sxs-lookup"><span data-stu-id="95e6e-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="95e6e-129">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="95e6e-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="95e6e-130">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="95e6e-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="95e6e-131">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="95e6e-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 