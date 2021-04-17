---
description: La función VarLenSmallIntToDword convierte un entero pequeño de longitud variable en un valor DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Función VarLenSmallIntToDword (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677669"
---
# <a name="varlensmallinttodword-function"></a><span data-ttu-id="6e145-103">VarLenSmallIntToDword función)</span><span class="sxs-lookup"><span data-stu-id="6e145-103">VarLenSmallIntToDword function</span></span>

<span data-ttu-id="6e145-104">La función **VarLenSmallIntToDword** convierte un entero pequeño de longitud variable en un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6e145-104">The **VarLenSmallIntToDword** function converts a variable-length, small integer to a **DWORD**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e145-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e145-105">Syntax</span></span>


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a><span data-ttu-id="6e145-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e145-107">*pValue*</span><span class="sxs-lookup"><span data-stu-id="6e145-107">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="6e145-108">Puntero al entero pequeño de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="6e145-108">Pointer to the variable-length, small integer.</span></span>

</dd> <dt>

<span data-ttu-id="6e145-109">*ValueLen*</span><span class="sxs-lookup"><span data-stu-id="6e145-109">*ValueLen*</span></span> 
</dt> <dd>

<span data-ttu-id="6e145-110">Longitud (en bytes) del entero pequeño de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="6e145-110">Length (in bytes) of the variable-length, small integer .</span></span>

</dd> <dt>

<span data-ttu-id="6e145-111">*fIsByteswapped*</span><span class="sxs-lookup"><span data-stu-id="6e145-111">*fIsByteswapped*</span></span> 
</dt> <dd>

<span data-ttu-id="6e145-112">Marca que indica si el entero de longitud variable pequeño es un intercambio de bytes.</span><span class="sxs-lookup"><span data-stu-id="6e145-112">Flag that indicates whether the variable length small integer is byte-swapped.</span></span>

</dd> <dt>

<span data-ttu-id="6e145-113">*lpDword*</span><span class="sxs-lookup"><span data-stu-id="6e145-113">*lpDword*</span></span> 
</dt> <dd>

<span data-ttu-id="6e145-114">**DWORD** en la que se convierte el entero.</span><span class="sxs-lookup"><span data-stu-id="6e145-114">The **DWORD** that the integer is converted to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e145-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e145-115">Return value</span></span>

<span data-ttu-id="6e145-116">El valor devuelto es un puntero a la **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6e145-116">The return value is a pointer to the **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e145-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e145-117">Requirements</span></span>



| <span data-ttu-id="6e145-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e145-118">Requirement</span></span> | <span data-ttu-id="6e145-119">Value</span><span class="sxs-lookup"><span data-stu-id="6e145-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e145-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e145-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e145-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6e145-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6e145-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e145-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e145-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e145-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e145-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e145-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e145-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e145-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e145-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e145-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e145-127"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e145-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e145-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e145-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e145-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e145-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




