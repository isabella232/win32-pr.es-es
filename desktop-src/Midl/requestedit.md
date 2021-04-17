---
title: requestedit (atributo)
description: El atributo \ requestedit \ indica que la propiedad admite la notificación OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit (atributo) MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651350"
---
# <a name="requestedit-attribute"></a><span data-ttu-id="7e090-104">requestedit (atributo)</span><span class="sxs-lookup"><span data-stu-id="7e090-104">requestedit attribute</span></span>

<span data-ttu-id="7e090-105">El atributo **\[ \] requestedit** indica que la propiedad admite la notificación **OnRequestEdit** .</span><span class="sxs-lookup"><span data-stu-id="7e090-105">The **\[requestedit\]** attribute indicates that the property supports the **OnRequestEdit** notification.</span></span>

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a><span data-ttu-id="7e090-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e090-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e090-107">*opcional: atributos*</span><span class="sxs-lookup"><span data-stu-id="7e090-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7e090-108">Cero o más atributos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7e090-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7e090-109">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="7e090-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7e090-110">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="7e090-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7e090-111">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="7e090-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7e090-112">Especifica el nombre de la función en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7e090-112">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="7e090-113">*params*</span><span class="sxs-lookup"><span data-stu-id="7e090-113">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="7e090-114">Cero o más parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="7e090-114">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e090-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e090-115">Remarks</span></span>

<span data-ttu-id="7e090-116">La compatibilidad con la notificación de **OnRequestEdit** significa que, antes de que se realice un cambio, el objeto enviará al cliente una solicitud de permiso para cambiar una propiedad.</span><span class="sxs-lookup"><span data-stu-id="7e090-116">Supporting **OnRequestEdit** notification means that, before a change is made, the object will send the client a request for permission to change a property.</span></span> <span data-ttu-id="7e090-117">Un objeto puede admitir el enlace de datos pero no tiene este atributo.</span><span class="sxs-lookup"><span data-stu-id="7e090-117">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="7e090-118">Marcas</span><span class="sxs-lookup"><span data-stu-id="7e090-118">Flags</span></span>

<span data-ttu-id="7e090-119">FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT</span><span class="sxs-lookup"><span data-stu-id="7e090-119">FUNCFLAG\_FREQUESTEDIT, VARFLAG\_FREQUESTEDIT</span></span>

## <a name="examples"></a><span data-ttu-id="7e090-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7e090-120">Examples</span></span>

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a><span data-ttu-id="7e090-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e090-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e090-122">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="7e090-122">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="7e090-123">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="7e090-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7e090-124">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="7e090-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7e090-125">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="7e090-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 