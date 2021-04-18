---
description: Comprueba que el proceso de llamada tiene acceso de lectura a un bloque de memoria. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: Macro ValidateReadPtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691036"
---
# <a name="validatereadptr-macro"></a><span data-ttu-id="d71c1-104">ValidateReadPtr (macro)</span><span class="sxs-lookup"><span data-stu-id="d71c1-104">ValidateReadPtr macro</span></span>

<span data-ttu-id="d71c1-105">Comprueba que el proceso de llamada tiene acceso de lectura a un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="d71c1-105">Verifies that the calling process has read access to a memory block.</span></span> <span data-ttu-id="d71c1-106">Si no es así, la macro llama a la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="d71c1-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="d71c1-107">Esta macro está en desuso.</span><span class="sxs-lookup"><span data-stu-id="d71c1-107">This macro is deprecated.</span></span> <span data-ttu-id="d71c1-108">En el Windows SDK para Windows Vista (y versiones posteriores), esta macro no hace nada.</span><span class="sxs-lookup"><span data-stu-id="d71c1-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d71c1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d71c1-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="d71c1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d71c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d71c1-111">*m*</span><span class="sxs-lookup"><span data-stu-id="d71c1-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="d71c1-112">Puntero a un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="d71c1-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="d71c1-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="d71c1-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="d71c1-114">Tamaño del bloque de memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d71c1-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d71c1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d71c1-115">Return value</span></span>

<span data-ttu-id="d71c1-116">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d71c1-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d71c1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d71c1-117">Remarks</span></span>

<span data-ttu-id="d71c1-118">Esta macro se omite a menos que se defina DEBUG, \_ Debug o VFWROBUST cuando se incluye el archivo de encabezado de clase base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d71c1-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="d71c1-119">Esta macro puede tener un costo de rendimiento considerable.</span><span class="sxs-lookup"><span data-stu-id="d71c1-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="d71c1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d71c1-120">Requirements</span></span>



| <span data-ttu-id="d71c1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d71c1-121">Requirement</span></span> | <span data-ttu-id="d71c1-122">Value</span><span class="sxs-lookup"><span data-stu-id="d71c1-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d71c1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d71c1-123">Header</span></span><br/> | <dl> <span data-ttu-id="d71c1-124"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d71c1-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d71c1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d71c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d71c1-126">Macros de validación de puntero</span><span class="sxs-lookup"><span data-stu-id="d71c1-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




