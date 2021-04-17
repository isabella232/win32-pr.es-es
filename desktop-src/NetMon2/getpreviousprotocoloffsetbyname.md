---
description: La función GetPreviousProtocolOffsetByName devuelve la instancia anterior de un protocolo determinado.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Función GetPreviousProtocolOffsetByName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677277"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a><span data-ttu-id="ac819-103">GetPreviousProtocolOffsetByName función)</span><span class="sxs-lookup"><span data-stu-id="ac819-103">GetPreviousProtocolOffsetByName function</span></span>

<span data-ttu-id="ac819-104">La función **GetPreviousProtocolOffsetByName** devuelve la instancia anterior de un protocolo determinado.</span><span class="sxs-lookup"><span data-stu-id="ac819-104">The **GetPreviousProtocolOffsetByName** function returns the previous instance of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac819-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac819-105">Syntax</span></span>


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a><span data-ttu-id="ac819-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac819-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac819-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac819-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="ac819-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="ac819-109">*dwStartOffset* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac819-109">*dwStartOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac819-110">Desplazamiento en el marco.</span><span class="sxs-lookup"><span data-stu-id="ac819-110">Offset in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="ac819-111">*szProtocolName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac819-111">*szProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac819-112">Nombre del protocolo que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="ac819-112">Name of the protocol you want to search for.</span></span>

</dd> <dt>

<span data-ttu-id="ac819-113">*pdwPreviousOffset* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac819-113">*pdwPreviousOffset* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac819-114">Puntero a un **valor DWORD** que contiene el desplazamiento al protocolo anterior (si la función se ejecuta correctamente).</span><span class="sxs-lookup"><span data-stu-id="ac819-114">Pointer to a **DWORD** that contains the offset to the previous protocol (if the function succeeds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac819-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac819-115">Return value</span></span>

<span data-ttu-id="ac819-116">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ac819-116">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ac819-117">Si la función no se realiza correctamente, el valor devuelto es el \_ Protocolo NMERR \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="ac819-117">If the function is unsuccessful, the return value is NMERR\_PROTOCOL\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac819-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac819-118">Remarks</span></span>

<span data-ttu-id="ac819-119">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a **GetPreviousProtocolOffsetByName**.</span><span class="sxs-lookup"><span data-stu-id="ac819-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPreviousProtocolOffsetByName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac819-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac819-120">Requirements</span></span>



| <span data-ttu-id="ac819-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac819-121">Requirement</span></span> | <span data-ttu-id="ac819-122">Value</span><span class="sxs-lookup"><span data-stu-id="ac819-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac819-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac819-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ac819-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac819-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ac819-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac819-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ac819-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac819-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ac819-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac819-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac819-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac819-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ac819-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac819-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac819-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac819-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac819-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac819-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac819-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac819-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




