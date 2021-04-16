---
description: Obtiene un bloqueo compartido.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'CShareLockNH:: ShareLock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649746"
---
# <a name="csharelocknhsharelock-method"></a><span data-ttu-id="ebb82-103">CShareLockNH:: ShareLock (método)</span><span class="sxs-lookup"><span data-stu-id="ebb82-103">CShareLockNH::ShareLock method</span></span>

<span data-ttu-id="ebb82-104">Obtiene un bloqueo compartido.</span><span class="sxs-lookup"><span data-stu-id="ebb82-104">Obtains a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb82-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebb82-105">Syntax</span></span>


```C++
void ShareLock();
```



## <a name="parameters"></a><span data-ttu-id="ebb82-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebb82-106">Parameters</span></span>

<span data-ttu-id="ebb82-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ebb82-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebb82-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebb82-108">Return value</span></span>

<span data-ttu-id="ebb82-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ebb82-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebb82-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebb82-110">Remarks</span></span>

<span data-ttu-id="ebb82-111">Cada llamada a **ShareLock** se debe emparejar con exactamente una llamada a [**ShareUnlock**](csharelocknh--shareunlock.md).</span><span class="sxs-lookup"><span data-stu-id="ebb82-111">Each call to **ShareLock** must be paired with exactly one call to [**ShareUnlock**](csharelocknh--shareunlock.md).</span></span> <span data-ttu-id="ebb82-112">Solo un subproceso que llame correctamente a **ShareLock** puede llamar a **ShareUnlock**; de lo contrario, se puede producir un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="ebb82-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="ebb82-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ebb82-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb82-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb82-114">Requirements</span></span>



| <span data-ttu-id="ebb82-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb82-115">Requirement</span></span> | <span data-ttu-id="ebb82-116">Value</span><span class="sxs-lookup"><span data-stu-id="ebb82-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb82-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ebb82-117">DLL</span></span><br/> | <dl> <span data-ttu-id="ebb82-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebb82-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebb82-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebb82-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb82-120">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="ebb82-120">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
