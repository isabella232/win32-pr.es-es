---
description: Libera un bloqueo parcial para que otros compradores de bloqueos exclusivos o parciales puedan escribir ahora.
ms.assetid: 95a3e0d1-4e8b-4e30-b4fd-709b9db465de
title: CShareLockNH::P método artialUnlock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 930c0f51e199c1668a70f2dd017b0280939b0710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649748"
---
# <a name="csharelocknhpartialunlock-method"></a><span data-ttu-id="25710-103">CShareLockNH::P método artialUnlock</span><span class="sxs-lookup"><span data-stu-id="25710-103">CShareLockNH::PartialUnlock method</span></span>

<span data-ttu-id="25710-104">Libera un bloqueo parcial para que otros compradores de bloqueos exclusivos o parciales puedan escribir ahora.</span><span class="sxs-lookup"><span data-stu-id="25710-104">Releases a partial lock so that other exclusive or partial lock acquirers can now enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="25710-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25710-105">Syntax</span></span>


```C++
void PartialUnlock();
```



## <a name="parameters"></a><span data-ttu-id="25710-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25710-106">Parameters</span></span>

<span data-ttu-id="25710-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="25710-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25710-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25710-108">Return value</span></span>

<span data-ttu-id="25710-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="25710-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25710-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25710-110">Remarks</span></span>

<span data-ttu-id="25710-111">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="25710-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="25710-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25710-112">Requirements</span></span>



| <span data-ttu-id="25710-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="25710-113">Requirement</span></span> | <span data-ttu-id="25710-114">Value</span><span class="sxs-lookup"><span data-stu-id="25710-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25710-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25710-115">DLL</span></span><br/> | <dl> <span data-ttu-id="25710-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25710-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
