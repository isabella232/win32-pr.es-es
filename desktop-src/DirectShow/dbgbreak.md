---
description: Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de código fuente y el número de línea. El usuario puede omitir el mensaje, entrar en el depurador o salir de la aplicación. Se omite en las compilaciones comerciales.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Macro DbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661243"
---
# <a name="dbgbreak-macro"></a><span data-ttu-id="4e9b3-105">DbgBreak (macro)</span><span class="sxs-lookup"><span data-stu-id="4e9b3-105">DbgBreak macro</span></span>

<span data-ttu-id="4e9b3-106">Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de código fuente y el número de línea.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-106">Displays a message box with the specified string, the name of the source file, and the line number.</span></span> <span data-ttu-id="4e9b3-107">El usuario puede omitir el mensaje, entrar en el depurador o salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-107">The user can ignore the message, enter the debugger, or quit the application.</span></span> <span data-ttu-id="4e9b3-108">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e9b3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e9b3-109">Syntax</span></span>


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="4e9b3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e9b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e9b3-111">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="4e9b3-111">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="4e9b3-112">Cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-112">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e9b3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e9b3-113">Return value</span></span>

<span data-ttu-id="4e9b3-114">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-114">This macro does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="4e9b3-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4e9b3-115">Examples</span></span>


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a><span data-ttu-id="4e9b3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e9b3-116">Requirements</span></span>



| <span data-ttu-id="4e9b3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e9b3-117">Requirement</span></span> | <span data-ttu-id="4e9b3-118">Value</span><span class="sxs-lookup"><span data-stu-id="4e9b3-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9b3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e9b3-119">Header</span></span><br/> | <dl> <span data-ttu-id="4e9b3-120"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e9b3-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e9b3-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e9b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9b3-122">Macros Assert y Breakpoint</span><span class="sxs-lookup"><span data-stu-id="4e9b3-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




