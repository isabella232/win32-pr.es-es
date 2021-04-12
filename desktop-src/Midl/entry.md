---
title: entry (atributo)
description: El atributo \ entry \ especifica una función exportada o una constante en un módulo mediante la identificación del punto de entrada en el archivo DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- atributo de entrada MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358843"
---
# <a name="entry-attribute"></a><span data-ttu-id="46665-104">entry (atributo)</span><span class="sxs-lookup"><span data-stu-id="46665-104">entry attribute</span></span>

<span data-ttu-id="46665-105">El atributo de **\[ entrada \]** especifica una función o constante exportada en un módulo mediante la identificación del punto de entrada en el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="46665-105">The **\[entry\]** attribute specifies an exported function or constant in a module by identifying the entry point in the DLL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="46665-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46665-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46665-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="46665-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="46665-108">Especifica un número de identificación único universal para el [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="46665-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="46665-109">*identificador de entrada*</span><span class="sxs-lookup"><span data-stu-id="46665-109">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="46665-110">Especifica el nombre de función del punto de entrada del módulo o el número de identificación de entero.</span><span class="sxs-lookup"><span data-stu-id="46665-110">Specifies the module entry point function name or integer identification number.</span></span>

</dd> <dt>

<span data-ttu-id="46665-111">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="46665-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="46665-112">Especifica cero o más atributos para que el compilador de MIDL los aplique al [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="46665-112">Specifies zero or more attributes for the MIDL compiler to apply to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="46665-113">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="46665-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="46665-114">Especifica el nombre que otros componentes de software usan para denotar el [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="46665-114">Specifies the name other software components use to denote the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="46665-115">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="46665-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="46665-116">Especifica una o más instrucciones de definición de elementos de módulo.</span><span class="sxs-lookup"><span data-stu-id="46665-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46665-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46665-117">Remarks</span></span>

<span data-ttu-id="46665-118">Si la variable *EntryID* del atributo de **\[ entrada \]** es una cadena, se trata de un punto de entrada con nombre.</span><span class="sxs-lookup"><span data-stu-id="46665-118">If the *entryid* variable of the **\[entry\]** attribute is a string, this is a named entry point.</span></span> <span data-ttu-id="46665-119">Si *EntryID* es un número, el punto de entrada se define mediante un ordinal.</span><span class="sxs-lookup"><span data-stu-id="46665-119">If *entryid* is a number, the entry point is defined by an ordinal.</span></span> <span data-ttu-id="46665-120">Este atributo proporciona una manera de obtener la dirección de una función en un módulo.</span><span class="sxs-lookup"><span data-stu-id="46665-120">This attribute provides a way to obtain the address of a function in a module.</span></span>

## <a name="examples"></a><span data-ttu-id="46665-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="46665-121">Examples</span></span>

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a><span data-ttu-id="46665-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="46665-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46665-123">**DllName**</span><span class="sxs-lookup"><span data-stu-id="46665-123">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="46665-124">**destina**</span><span class="sxs-lookup"><span data-stu-id="46665-124">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="46665-125">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="46665-125">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="46665-126">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="46665-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="46665-127">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="46665-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 