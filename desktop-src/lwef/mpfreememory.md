---
title: Función MpFreeMemory (MpClient. h)
description: Libera memoria para el administrador de protección contra malware de.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Función MpFreeMemory características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801909"
---
# <a name="mpfreememory-function"></a><span data-ttu-id="efe62-104">MpFreeMemory función)</span><span class="sxs-lookup"><span data-stu-id="efe62-104">MpFreeMemory function</span></span>

<span data-ttu-id="efe62-105">Libera memoria para el administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="efe62-105">Frees memory for the malware protection manager.</span></span> <span data-ttu-id="efe62-106">El autor de la llamada debe liberar todos los búferes asignados y devueltos por las funciones de protección contra malware mediante esta función.</span><span class="sxs-lookup"><span data-stu-id="efe62-106">All buffers allocated and returned by malware protection functions must be freed by the caller using this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe62-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efe62-107">Syntax</span></span>


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="efe62-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efe62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe62-109">*pMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efe62-109">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe62-110">Tipo: **PVOID**</span><span class="sxs-lookup"><span data-stu-id="efe62-110">Type: **PVOID**</span></span>

<span data-ttu-id="efe62-111">Puntero a la memoria asignada por una función de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="efe62-111">A pointer to memory allocated by a malware protection function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe62-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efe62-112">Return value</span></span>

<span data-ttu-id="efe62-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="efe62-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="efe62-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efe62-114">Remarks</span></span>

<span data-ttu-id="efe62-115">Para facilitar la administración de la memoria para los clientes, el administrador de protección contra malware también define las macros para liberar memoria asociada a las distintas estructuras devueltas por las funciones de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="efe62-115">To facilitate memory management for clients, the malware protection manager also defines macros to free memory associated with various structures returned by malware protection functions.</span></span> <span data-ttu-id="efe62-116">Las siguientes macros se definen en el archivo de encabezado mpmemfree. h:</span><span class="sxs-lookup"><span data-stu-id="efe62-116">The following macros are defined in the header file mpmemfree.h:</span></span>



| <span data-ttu-id="efe62-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="efe62-117">Name</span></span>                            | <span data-ttu-id="efe62-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="efe62-118">Description</span></span>                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="efe62-119">MPRESOURCE \_ info \_ Free</span><span class="sxs-lookup"><span data-stu-id="efe62-119">MPRESOURCE\_INFO\_FREE</span></span>          | <span data-ttu-id="efe62-120">Libera una información de [**MPRESOURCE \_**](mpresource-info.md)asignada.</span><span class="sxs-lookup"><span data-stu-id="efe62-120">Frees an allocated [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>                  |
| <span data-ttu-id="efe62-121">MPTHREAT \_ info \_ Free</span><span class="sxs-lookup"><span data-stu-id="efe62-121">MPTHREAT\_INFO\_FREE</span></span>            | <span data-ttu-id="efe62-122">Libera una información de [**MPTHREAT \_**](mpthreat-info.md)asignada.</span><span class="sxs-lookup"><span data-stu-id="efe62-122">Frees an allocated [**MPTHREAT\_INFO**](mpthreat-info.md).</span></span>                      |
| <span data-ttu-id="efe62-123">MPTHREAT \_ \_ información localizada \_ gratis</span><span class="sxs-lookup"><span data-stu-id="efe62-123">MPTHREAT\_LOCALIZED\_INFO\_FREE</span></span> | <span data-ttu-id="efe62-124">Libera [**\_ \_ información localizada MPTHREAT**](mpthreat-localized-info.md)asignada.</span><span class="sxs-lookup"><span data-stu-id="efe62-124">Frees an allocated [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="efe62-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efe62-125">Requirements</span></span>



| <span data-ttu-id="efe62-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="efe62-126">Requirement</span></span> | <span data-ttu-id="efe62-127">Value</span><span class="sxs-lookup"><span data-stu-id="efe62-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efe62-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efe62-128">Minimum supported client</span></span><br/> | <span data-ttu-id="efe62-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="efe62-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="efe62-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efe62-130">Minimum supported server</span></span><br/> | <span data-ttu-id="efe62-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="efe62-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="efe62-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efe62-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="efe62-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="efe62-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="efe62-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efe62-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efe62-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efe62-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe62-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="efe62-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe62-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="efe62-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="efe62-138">**información de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="efe62-138">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="efe62-139">**información de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="efe62-139">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="efe62-140">**\_información localizada de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="efe62-140">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





