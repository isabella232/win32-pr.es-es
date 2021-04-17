---
description: Comprueba que el proceso de llamada tiene acceso de lectura a una cadena. Si no es así, la macro llama a la macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: Macro ValidateStringPtr (Wxdebug. h)
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
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691035"
---
# <a name="validatestringptr-macro"></a><span data-ttu-id="180ff-104">ValidateStringPtr (macro)</span><span class="sxs-lookup"><span data-stu-id="180ff-104">ValidateStringPtr macro</span></span>

<span data-ttu-id="180ff-105">Comprueba que el proceso de llamada tiene acceso de lectura a una cadena.</span><span class="sxs-lookup"><span data-stu-id="180ff-105">Verifies that the calling process has read access to a string.</span></span> <span data-ttu-id="180ff-106">Si no es así, la macro llama a la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="180ff-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="180ff-107">Esta macro está en desuso.</span><span class="sxs-lookup"><span data-stu-id="180ff-107">This macro is deprecated.</span></span> <span data-ttu-id="180ff-108">En el Windows SDK para Windows Vista (y versiones posteriores), esta macro no hace nada.</span><span class="sxs-lookup"><span data-stu-id="180ff-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="180ff-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="180ff-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="180ff-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="180ff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180ff-111">*m*</span><span class="sxs-lookup"><span data-stu-id="180ff-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="180ff-112">Puntero a una cadena de **TCHAR** terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="180ff-112">Pointer to a NULL-terminated **TCHAR** string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="180ff-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="180ff-113">Return value</span></span>

<span data-ttu-id="180ff-114">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="180ff-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="180ff-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="180ff-115">Remarks</span></span>

<span data-ttu-id="180ff-116">Esta macro se omite a menos que se defina DEBUG, \_ Debug o VFWROBUST cuando se incluye el archivo de encabezado de clase base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="180ff-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="180ff-117">Esta macro puede tener un costo de rendimiento considerable.</span><span class="sxs-lookup"><span data-stu-id="180ff-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="180ff-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="180ff-118">Requirements</span></span>



| <span data-ttu-id="180ff-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="180ff-119">Requirement</span></span> | <span data-ttu-id="180ff-120">Value</span><span class="sxs-lookup"><span data-stu-id="180ff-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="180ff-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="180ff-121">Header</span></span><br/> | <dl> <span data-ttu-id="180ff-122"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="180ff-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="180ff-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="180ff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180ff-124">Macros de validación de puntero</span><span class="sxs-lookup"><span data-stu-id="180ff-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




