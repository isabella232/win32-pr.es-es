---
title: public (atributo)
description: El atributo \ Public \ incluye un alias declarado con la palabra clave typedef en la biblioteca de tipos.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- atributo público MIDL
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651351"
---
# <a name="public-attribute"></a><span data-ttu-id="010ad-104">public (atributo)</span><span class="sxs-lookup"><span data-stu-id="010ad-104">public attribute</span></span>

<span data-ttu-id="010ad-105">El atributo **\[ \] Public** incluye un alias declarado con la palabra clave [**typedef**](typedef.md) en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="010ad-105">The **\[public\]** attribute includes an alias declared with the [**typedef**](typedef.md) keyword in the type library.</span></span>

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a><span data-ttu-id="010ad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="010ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010ad-107">*tipo de datos*</span><span class="sxs-lookup"><span data-stu-id="010ad-107">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="010ad-108">El tipo de datos para el que el identificador será un alias.</span><span class="sxs-lookup"><span data-stu-id="010ad-108">The data type that the identifier will be an alias for.</span></span>

</dd> <dt>

<span data-ttu-id="010ad-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="010ad-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="010ad-110">Otro nombre por el que se conocerá el *tipo de datos* en el software.</span><span class="sxs-lookup"><span data-stu-id="010ad-110">Another name by which *data-type* will be known in the software.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="010ad-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="010ad-111">Remarks</span></span>

<span data-ttu-id="010ad-112">De forma predeterminada, un alias declarado con [**typedef**](typedef.md) y que no tiene otros atributos se trata como una **\# definición** y no se incluye en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="010ad-112">By default, an alias that is declared with [**typedef**](typedef.md) and has no other attributes is treated as a **\#define** and is not included in the type library.</span></span> <span data-ttu-id="010ad-113">El uso del atributo **\[ Public \]** garantiza que el alias se convierte en parte de la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="010ad-113">Using the **\[public\]** attribute ensures that the alias becomes part of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="010ad-114">El compilador MIDL requiere que aplique explícitamente el atributo **\[ público \]** a cada TypeDef que desee que sea público.</span><span class="sxs-lookup"><span data-stu-id="010ad-114">The MIDL compiler requires that you explicitly apply the **\[public\]** attribute to each typedef that you want public.</span></span>

 

## <a name="examples"></a><span data-ttu-id="010ad-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="010ad-115">Examples</span></span>

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a><span data-ttu-id="010ad-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="010ad-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010ad-117">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="010ad-117">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="010ad-118">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="010ad-118">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="010ad-119">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="010ad-119">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="010ad-120">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="010ad-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="010ad-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="010ad-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 