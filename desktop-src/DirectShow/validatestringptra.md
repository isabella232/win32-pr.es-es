---
description: Comprueba que el proceso de llamada tiene acceso de lectura a una cadena ANSI. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Macro ValidateStringPtrA (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681166"
---
# <a name="validatestringptra-macro"></a><span data-ttu-id="1d873-104">ValidateStringPtrA (macro)</span><span class="sxs-lookup"><span data-stu-id="1d873-104">ValidateStringPtrA macro</span></span>

<span data-ttu-id="1d873-105">Comprueba que el proceso de llamada tiene acceso de lectura a una cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="1d873-105">Verifies that the calling process has read access to an ANSI string.</span></span> <span data-ttu-id="1d873-106">Si no es así, la macro llama a la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="1d873-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="1d873-107">Esta macro está en desuso.</span><span class="sxs-lookup"><span data-stu-id="1d873-107">This macro is deprecated.</span></span> <span data-ttu-id="1d873-108">En el Windows SDK para Windows Vista (y versiones posteriores), esta macro no hace nada.</span><span class="sxs-lookup"><span data-stu-id="1d873-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1d873-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d873-109">Syntax</span></span>


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="1d873-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d873-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d873-111">*m*</span><span class="sxs-lookup"><span data-stu-id="1d873-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="1d873-112">Puntero a una cadena ANSI terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="1d873-112">Pointer to a NULL-terminated ANSI string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d873-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d873-113">Return value</span></span>

<span data-ttu-id="1d873-114">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1d873-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d873-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d873-115">Remarks</span></span>

<span data-ttu-id="1d873-116">Esta macro se omite a menos que se defina DEBUG, \_ Debug o VFWROBUST cuando se incluye el archivo de encabezado de clase base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1d873-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d873-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d873-117">Requirements</span></span>



| <span data-ttu-id="1d873-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d873-118">Requirement</span></span> | <span data-ttu-id="1d873-119">Value</span><span class="sxs-lookup"><span data-stu-id="1d873-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d873-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d873-120">Header</span></span><br/> | <dl> <span data-ttu-id="1d873-121"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d873-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d873-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d873-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d873-123">Macros de validación de puntero</span><span class="sxs-lookup"><span data-stu-id="1d873-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




