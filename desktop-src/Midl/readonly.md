---
title: atributo de solo lectura
description: El atributo \ ReadOnly \ prohíbe la asignación a una variable.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- atributo de solo lectura MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995206"
---
# <a name="readonly-attribute"></a><span data-ttu-id="0ff36-104">atributo de solo lectura</span><span class="sxs-lookup"><span data-stu-id="0ff36-104">readonly attribute</span></span>

<span data-ttu-id="0ff36-105">El atributo **\[ ReadOnly \]** prohíbe la asignación a una variable.</span><span class="sxs-lookup"><span data-stu-id="0ff36-105">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span>

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a><span data-ttu-id="0ff36-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ff36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff36-107">*opcional: atributos*</span><span class="sxs-lookup"><span data-stu-id="0ff36-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="0ff36-108">Cero o más atributos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="0ff36-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="0ff36-109">*tipo de datos*</span><span class="sxs-lookup"><span data-stu-id="0ff36-109">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0ff36-110">Tipo de los datos contenidos en el *identificador*.</span><span class="sxs-lookup"><span data-stu-id="0ff36-110">The type of the data contained by *identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="0ff36-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="0ff36-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0ff36-112">Un nombre por el que el software puede hacer referencia a la ubicación de almacenamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="0ff36-112">A name by which the software can refer to the data storage location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ff36-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ff36-113">Remarks</span></span>

<span data-ttu-id="0ff36-114">El atributo **\[ ReadOnly \]** prohíbe la asignación a una variable.</span><span class="sxs-lookup"><span data-stu-id="0ff36-114">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span> <span data-ttu-id="0ff36-115">solo se admite **\[ ReadOnly \]** en el nivel de parámetro, no en el nivel de método.</span><span class="sxs-lookup"><span data-stu-id="0ff36-115">**\[readonly\]** is only supported at the parameter level, not at the method level.</span></span>

### <a name="flags"></a><span data-ttu-id="0ff36-116">Marcas</span><span class="sxs-lookup"><span data-stu-id="0ff36-116">Flags</span></span>

<span data-ttu-id="0ff36-117">VARFLAG \_ FREADONLY</span><span class="sxs-lookup"><span data-stu-id="0ff36-117">VARFLAG\_FREADONLY</span></span>

## <a name="examples"></a><span data-ttu-id="0ff36-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0ff36-118">Examples</span></span>

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a><span data-ttu-id="0ff36-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ff36-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff36-120">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="0ff36-120">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="0ff36-121">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="0ff36-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="0ff36-122">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="0ff36-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="0ff36-123">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="0ff36-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 