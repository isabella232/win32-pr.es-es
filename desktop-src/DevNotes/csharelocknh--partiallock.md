---
description: Impide que más de un subproceso complete la adquisición de un bloqueo.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: CShareLockNH::P método artialLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660487"
---
# <a name="csharelocknhpartiallock-method"></a><span data-ttu-id="fff67-103">CShareLockNH::P método artialLock</span><span class="sxs-lookup"><span data-stu-id="fff67-103">CShareLockNH::PartialLock method</span></span>

<span data-ttu-id="fff67-104">Impide que más de un subproceso complete la adquisición de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="fff67-104">Prevents more than one thread from completing acquiring a lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fff67-105">Syntax</span></span>


```C++
void PartialLock();
```



## <a name="parameters"></a><span data-ttu-id="fff67-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fff67-106">Parameters</span></span>

<span data-ttu-id="fff67-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fff67-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fff67-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fff67-108">Return value</span></span>

<span data-ttu-id="fff67-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fff67-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fff67-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fff67-110">Remarks</span></span>

<span data-ttu-id="fff67-111">Mientras **PartialLock** está en vigor, otros subprocesos que llaman a [**ShareLock**](csharelocknh--sharelock.md) pueden entrar en el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="fff67-111">While **PartialLock** is in effect, other threads calling [**ShareLock**](csharelocknh--sharelock.md) can enter the lock.</span></span>

<span data-ttu-id="fff67-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fff67-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff67-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fff67-113">Requirements</span></span>



| <span data-ttu-id="fff67-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fff67-114">Requirement</span></span> | <span data-ttu-id="fff67-115">Value</span><span class="sxs-lookup"><span data-stu-id="fff67-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fff67-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fff67-116">DLL</span></span><br/> | <dl> <span data-ttu-id="fff67-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff67-117"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
