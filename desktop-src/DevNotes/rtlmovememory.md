---
description: Copia el contenido de un bloque de memoria de origen en un bloque de memoria de destino y admite los bloques de memoria de origen y de destino superpuestos.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Función RtlMoveMemory (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666176"
---
# <a name="rtlmovememory-function"></a><span data-ttu-id="6bdef-103">RtlMoveMemory función)</span><span class="sxs-lookup"><span data-stu-id="6bdef-103">RtlMoveMemory function</span></span>

<span data-ttu-id="6bdef-104">Copia el contenido de un bloque de memoria de origen en un bloque de memoria de destino y admite los bloques de memoria de origen y de destino superpuestos.</span><span class="sxs-lookup"><span data-stu-id="6bdef-104">Copies the contents of a source memory block to a destination memory block, and supports overlapping source and destination memory blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bdef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bdef-105">Syntax</span></span>


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a><span data-ttu-id="6bdef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bdef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bdef-107">*Destino* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6bdef-107">*Destination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bdef-108">Puntero al bloque de memoria de destino en el que se van a copiar los bytes.</span><span class="sxs-lookup"><span data-stu-id="6bdef-108">A pointer to the destination memory block to copy the bytes to.</span></span>

</dd> <dt>

<span data-ttu-id="6bdef-109">*Origen* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6bdef-109">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bdef-110">Puntero al bloque de memoria de origen desde el que se van a copiar los bytes.</span><span class="sxs-lookup"><span data-stu-id="6bdef-110">A pointer to the source memory block to copy the bytes from.</span></span>

</dd> <dt>

<span data-ttu-id="6bdef-111">*Longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6bdef-111">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bdef-112">Número de bytes que se van a copiar desde el origen al destino.</span><span class="sxs-lookup"><span data-stu-id="6bdef-112">The number of bytes to copy from the source to the destination.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bdef-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bdef-113">Return value</span></span>

<span data-ttu-id="6bdef-114">None</span><span class="sxs-lookup"><span data-stu-id="6bdef-114">None</span></span>

## <a name="remarks"></a><span data-ttu-id="6bdef-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bdef-115">Remarks</span></span>

<span data-ttu-id="6bdef-116">El bloque de memoria de origen, que se define mediante el *origen* y la *longitud*, puede superponer el bloque de memoria de destino, que se define mediante el *destino* y la *longitud*.</span><span class="sxs-lookup"><span data-stu-id="6bdef-116">The source memory block, which is defined by *Source* and *Length*, can overlap the destination memory block, which is defined by *Destination* and *Length*.</span></span>

<span data-ttu-id="6bdef-117">La rutina [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) se ejecuta más rápido que **RtlMoveMemory**, pero **RtlCopyMemory** requiere que los bloques de memoria de origen y de destino no se superpongan.</span><span class="sxs-lookup"><span data-stu-id="6bdef-117">The [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) routine runs faster than **RtlMoveMemory**, but **RtlCopyMemory** requires that the source and destination memory blocks do not overlap.</span></span>

<span data-ttu-id="6bdef-118">Los autores de llamadas de **RtlMoveMemory** se pueden ejecutar en cualquier IRQL si los bloques de memoria de origen y de destino están en la memoria no paginada del sistema.</span><span class="sxs-lookup"><span data-stu-id="6bdef-118">Callers of **RtlMoveMemory** can be running at any IRQL if the source and destination memory blocks are in nonpaged system memory.</span></span> <span data-ttu-id="6bdef-119">De lo contrario, el llamador debe ejecutarse en IRQL <= \_ nivel APC.</span><span class="sxs-lookup"><span data-stu-id="6bdef-119">Otherwise, the caller must be running at IRQL <= APC\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bdef-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bdef-120">Requirements</span></span>



| <span data-ttu-id="6bdef-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bdef-121">Requirement</span></span> | <span data-ttu-id="6bdef-122">Value</span><span class="sxs-lookup"><span data-stu-id="6bdef-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdef-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bdef-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6bdef-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6bdef-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="6bdef-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bdef-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6bdef-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6bdef-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="6bdef-127">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="6bdef-127">Target platform</span></span><br/>          | <dl> <span data-ttu-id="6bdef-128"><dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="6bdef-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="6bdef-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bdef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bdef-130"><dt>WDM. h (incluir WDM. h, Ntddk. h o Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bdef-130"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="6bdef-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bdef-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bdef-132"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bdef-132"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6bdef-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6bdef-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bdef-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bdef-134"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="6bdef-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bdef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bdef-136">**RtlCopyMemory**</span><span class="sxs-lookup"><span data-stu-id="6bdef-136">**RtlCopyMemory**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
