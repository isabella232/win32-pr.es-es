---
title: usesgetlasterror (atributo)
description: El atributo \ usesgetlasterror \ indica al llamador que puede llamar a GetLastError para recuperar el código de error.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- usesgetlasterror (atributo) MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790005"
---
# <a name="usesgetlasterror-attribute"></a><span data-ttu-id="784ad-104">usesgetlasterror (atributo)</span><span class="sxs-lookup"><span data-stu-id="784ad-104">usesgetlasterror attribute</span></span>

<span data-ttu-id="784ad-105">El atributo **\[ \] usesgetlasterror** señala al llamador que puede llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el código de error.</span><span class="sxs-lookup"><span data-stu-id="784ad-105">The **\[usesgetlasterror\]** attribute signals the caller that it can call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a><span data-ttu-id="784ad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="784ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="784ad-107">*module: atributos*</span><span class="sxs-lookup"><span data-stu-id="784ad-107">*module-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="784ad-108">Cero o más atributos de MIDL que se aplicarán al [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="784ad-108">Zero or more MIDL attributes that will be applied to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="784ad-109">*nombre del módulo*</span><span class="sxs-lookup"><span data-stu-id="784ad-109">*module-name*</span></span> 
</dt> <dd>

<span data-ttu-id="784ad-110">Nombre del identificador del [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="784ad-110">The identifier name of the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="784ad-111">*identificador de entrada*</span><span class="sxs-lookup"><span data-stu-id="784ad-111">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="784ad-112">Especifica el punto de entrada del módulo, el nombre de la función o el número de identificación de entero.</span><span class="sxs-lookup"><span data-stu-id="784ad-112">Specifies the module entry point–function name or integer-identification number.</span></span>

</dd> <dt>

<span data-ttu-id="784ad-113">*otros: atributos*</span><span class="sxs-lookup"><span data-stu-id="784ad-113">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="784ad-114">Cero o más atributos de MIDL que se aplicarán al procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="784ad-114">Zero or more MIDL attributes that will be applied to the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="784ad-115">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="784ad-115">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="784ad-116">El tipo de datos que el procedimiento remoto devolverá tras su finalización.</span><span class="sxs-lookup"><span data-stu-id="784ad-116">The type of the data that the remote procedure will return upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="784ad-117">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="784ad-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="784ad-118">Nombre del procedimiento remoto tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="784ad-118">The name of the remote procedure as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="784ad-119">*lista de parámetros*</span><span class="sxs-lookup"><span data-stu-id="784ad-119">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="784ad-120">Cero o más parámetros para el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="784ad-120">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="784ad-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="784ad-121">Remarks</span></span>

<span data-ttu-id="784ad-122">El atributo **\[ \] usesgetlasterror** se puede establecer en un punto de entrada del módulo, si ese punto de entrada utiliza la función de Windows [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver los códigos de error.</span><span class="sxs-lookup"><span data-stu-id="784ad-122">The **\[usesgetlasterror\]** attribute can be set on a module entry point, if that entry point uses the Windows function [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return error codes.</span></span> <span data-ttu-id="784ad-123">El atributo indica al llamador que, si se produce un error al llamar a esa función, el autor de la llamada puede llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el código de error.</span><span class="sxs-lookup"><span data-stu-id="784ad-123">The attribute tells the caller that, if there is an error when calling that function, the caller can then call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

## <a name="examples"></a><span data-ttu-id="784ad-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="784ad-124">Examples</span></span>

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="784ad-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="784ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="784ad-126">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="784ad-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="784ad-127">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="784ad-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="784ad-128">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="784ad-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 