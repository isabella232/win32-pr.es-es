---
description: Libera un bloqueo adquirido mediante ExclusiveLock en modo compartido.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'CShareLockNH:: ExclusiveUnlock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661110"
---
# <a name="csharelocknhexclusiveunlock-method"></a><span data-ttu-id="edb77-103">CShareLockNH:: ExclusiveUnlock (método)</span><span class="sxs-lookup"><span data-stu-id="edb77-103">CShareLockNH::ExclusiveUnlock method</span></span>

<span data-ttu-id="edb77-104">Libera un bloqueo adquirido mediante [**ExclusiveLock**](csharelocknh--exclusivelock.md) en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="edb77-104">Releases a lock acquired by using [**ExclusiveLock**](csharelocknh--exclusivelock.md) to shared mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb77-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edb77-105">Syntax</span></span>


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a><span data-ttu-id="edb77-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edb77-106">Parameters</span></span>

<span data-ttu-id="edb77-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="edb77-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="edb77-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edb77-108">Return value</span></span>

<span data-ttu-id="edb77-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="edb77-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edb77-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edb77-110">Remarks</span></span>

<span data-ttu-id="edb77-111">Cada llamada a [**ExclusiveLock**](csharelocknh--exclusivelock.md) se debe emparejar con exactamente una llamada a **ExclusiveUnlock** para evitar el riesgo de un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="edb77-111">Each call to [**ExclusiveLock**](csharelocknh--exclusivelock.md) must be paired with exactly one call to **ExclusiveUnlock** to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="edb77-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="edb77-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb77-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edb77-113">Requirements</span></span>



| <span data-ttu-id="edb77-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="edb77-114">Requirement</span></span> | <span data-ttu-id="edb77-115">Value</span><span class="sxs-lookup"><span data-stu-id="edb77-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="edb77-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edb77-116">DLL</span></span><br/> | <dl> <span data-ttu-id="edb77-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edb77-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb77-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="edb77-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb77-119">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="edb77-119">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
