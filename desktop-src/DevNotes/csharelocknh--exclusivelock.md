---
description: Adquiere un bloqueo de lector/escritor.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'CShareLockNH:: ExclusiveLock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661111"
---
# <a name="csharelocknhexclusivelock-method"></a><span data-ttu-id="05f63-103">CShareLockNH:: ExclusiveLock (método)</span><span class="sxs-lookup"><span data-stu-id="05f63-103">CShareLockNH::ExclusiveLock method</span></span>

<span data-ttu-id="05f63-104">Adquiere un bloqueo de lector/escritor.</span><span class="sxs-lookup"><span data-stu-id="05f63-104">Acquires a reader/writer lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f63-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05f63-105">Syntax</span></span>


```C++
void ExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="05f63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05f63-106">Parameters</span></span>

<span data-ttu-id="05f63-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="05f63-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05f63-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05f63-108">Return value</span></span>

<span data-ttu-id="05f63-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="05f63-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f63-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05f63-110">Remarks</span></span>

<span data-ttu-id="05f63-111">Cada llamada a **ExclusiveLock** se debe emparejar con exactamente una llamada a [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) para evitar el riesgo de un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="05f63-111">Each call to **ExclusiveLock** must be paired with exactly one call to [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="05f63-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="05f63-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f63-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05f63-113">Requirements</span></span>



| <span data-ttu-id="05f63-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="05f63-114">Requirement</span></span> | <span data-ttu-id="05f63-115">Value</span><span class="sxs-lookup"><span data-stu-id="05f63-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="05f63-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05f63-116">DLL</span></span><br/> | <dl> <span data-ttu-id="05f63-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f63-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f63-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="05f63-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f63-119">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="05f63-119">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
