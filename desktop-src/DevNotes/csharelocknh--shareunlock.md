---
description: Libera un bloqueo compartido.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'CShareLockNH:: ShareUnlock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660483"
---
# <a name="csharelocknhshareunlock-method"></a><span data-ttu-id="49e57-103">CShareLockNH:: ShareUnlock (método)</span><span class="sxs-lookup"><span data-stu-id="49e57-103">CShareLockNH::ShareUnlock method</span></span>

<span data-ttu-id="49e57-104">Libera un bloqueo compartido.</span><span class="sxs-lookup"><span data-stu-id="49e57-104">Releases a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e57-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49e57-105">Syntax</span></span>


```C++
void ShareUnlock();
```



## <a name="parameters"></a><span data-ttu-id="49e57-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49e57-106">Parameters</span></span>

<span data-ttu-id="49e57-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="49e57-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49e57-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49e57-108">Return value</span></span>

<span data-ttu-id="49e57-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="49e57-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e57-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49e57-110">Remarks</span></span>

<span data-ttu-id="49e57-111">Cada llamada a [**ShareLock**](csharelocknh--sharelock.md) se debe emparejar con exactamente una llamada a **ShareUnlock**.</span><span class="sxs-lookup"><span data-stu-id="49e57-111">Each call to [**ShareLock**](csharelocknh--sharelock.md) must be paired with exactly one call to **ShareUnlock**.</span></span> <span data-ttu-id="49e57-112">Solo un subproceso que llame correctamente a **ShareLock** puede llamar a **ShareUnlock**; de lo contrario, se puede producir un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="49e57-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="49e57-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="49e57-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="49e57-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49e57-114">Requirements</span></span>



| <span data-ttu-id="49e57-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="49e57-115">Requirement</span></span> | <span data-ttu-id="49e57-116">Value</span><span class="sxs-lookup"><span data-stu-id="49e57-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49e57-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49e57-117">DLL</span></span><br/> | <dl> <span data-ttu-id="49e57-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49e57-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e57-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="49e57-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e57-120">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="49e57-120">**ShareLock**</span></span>](csharelocknh--sharelock.md)
</dt> </dl>

 

 
