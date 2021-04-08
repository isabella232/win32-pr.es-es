---
title: atributo DllName (STR)
description: El atributo \ DllName \ define el nombre del archivo DLL que contiene los puntos de entrada de un módulo.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- DllName (STR) atributo MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077737"
---
# <a name="dllnamestr-attribute"></a><span data-ttu-id="cf20d-104">atributo DllName (STR)</span><span class="sxs-lookup"><span data-stu-id="cf20d-104">dllname(str) attribute</span></span>

<span data-ttu-id="cf20d-105">El atributo **\[ DllName \]** define el nombre de la dll que contiene los puntos de entrada de un módulo.</span><span class="sxs-lookup"><span data-stu-id="cf20d-105">The **\[dllname\]** attribute defines the name of the DLL that contains the entry points for a module.</span></span>

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="cf20d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf20d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf20d-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="cf20d-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="cf20d-108">Especifica un número de identificación único universal para el [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="cf20d-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf20d-109">*filename*</span><span class="sxs-lookup"><span data-stu-id="cf20d-109">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="cf20d-110">Especifica una cadena terminada en NULL que contiene la ruta de acceso completa al archivo dll.</span><span class="sxs-lookup"><span data-stu-id="cf20d-110">Specifies a NULL-terminated string which contains the full path to the Dll file.</span></span>

</dd> <dt>

<span data-ttu-id="cf20d-111">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="cf20d-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="cf20d-112">Especifica una lista de cero o más atributos de la interfaz de MIDL.</span><span class="sxs-lookup"><span data-stu-id="cf20d-112">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="cf20d-113">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="cf20d-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="cf20d-114">Especifica el nombre que otros componentes de software pueden usar para hacer referencia al módulo.</span><span class="sxs-lookup"><span data-stu-id="cf20d-114">Specifies the name which other software components can use to refer to the module.</span></span>

</dd> <dt>

<span data-ttu-id="cf20d-115">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="cf20d-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="cf20d-116">Especifica una o más instrucciones de definición de elementos de módulo.</span><span class="sxs-lookup"><span data-stu-id="cf20d-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf20d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf20d-117">Remarks</span></span>

<span data-ttu-id="cf20d-118">El atributo **\[ DllName \]** es obligatorio en un módulo.</span><span class="sxs-lookup"><span data-stu-id="cf20d-118">The **\[dllname\]** attribute is required on a module.</span></span>

## <a name="examples"></a><span data-ttu-id="cf20d-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cf20d-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a><span data-ttu-id="cf20d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf20d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf20d-121">**destina**</span><span class="sxs-lookup"><span data-stu-id="cf20d-121">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="cf20d-122">**movimientos**</span><span class="sxs-lookup"><span data-stu-id="cf20d-122">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="cf20d-123">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="cf20d-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="cf20d-124">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="cf20d-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="cf20d-125">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="cf20d-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 