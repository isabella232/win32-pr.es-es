---
description: La función BERGetString descodifica una cadena codificada en BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Función BERGetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909422"
---
# <a name="bergetstring-function"></a><span data-ttu-id="deb5d-103">BERGetString función)</span><span class="sxs-lookup"><span data-stu-id="deb5d-103">BERGetString function</span></span>

<span data-ttu-id="deb5d-104">La función **BERGetString** descodifica una cadena codificada en BER.</span><span class="sxs-lookup"><span data-stu-id="deb5d-104">The **BERGetString** function decodes a BER-encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb5d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="deb5d-105">Syntax</span></span>


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="deb5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="deb5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb5d-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="deb5d-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="deb5d-108">Puntero a la cadena descodificada.</span><span class="sxs-lookup"><span data-stu-id="deb5d-108">Pointer to the string that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="deb5d-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="deb5d-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="deb5d-110">Puntero al puntero de la cadena descodificada.</span><span class="sxs-lookup"><span data-stu-id="deb5d-110">Pointer to the pointer of the decoded string.</span></span>

</dd> <dt>

<span data-ttu-id="deb5d-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="deb5d-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="deb5d-112">Puntero a la longitud de encabezado devuelta.</span><span class="sxs-lookup"><span data-stu-id="deb5d-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="deb5d-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="deb5d-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="deb5d-114">Puntero a la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="deb5d-114">Pointer to the string length.</span></span>

</dd> <dt>

<span data-ttu-id="deb5d-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="deb5d-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="deb5d-116">Puntero al puntero de la siguiente entrada de BER.</span><span class="sxs-lookup"><span data-stu-id="deb5d-116">Pointer to the pointer of the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb5d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="deb5d-117">Return value</span></span>

<span data-ttu-id="deb5d-118">Si la función es correcta (es decir, si se descodifica una cadena con codificación BER válida), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="deb5d-118">If the function is successful (that is, if a valid BER-encoded string is decoded), the return value is **TRUE**.</span></span>

<span data-ttu-id="deb5d-119">Si la función no es correcta, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="deb5d-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb5d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deb5d-120">Requirements</span></span>



| <span data-ttu-id="deb5d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="deb5d-121">Requirement</span></span> | <span data-ttu-id="deb5d-122">Value</span><span class="sxs-lookup"><span data-stu-id="deb5d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="deb5d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deb5d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="deb5d-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="deb5d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="deb5d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deb5d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="deb5d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="deb5d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="deb5d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="deb5d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="deb5d-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="deb5d-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="deb5d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="deb5d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="deb5d-130"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deb5d-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="deb5d-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="deb5d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deb5d-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deb5d-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




