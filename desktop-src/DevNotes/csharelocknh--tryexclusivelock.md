---
description: Obtiene un bloqueo de forma exclusiva si ningún otro lo mantiene actualmente.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: 'CShareLockNH:: TryExclusiveLock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8465e247807c4229821acef552e0786a5604a3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649745"
---
# <a name="csharelocknhtryexclusivelock-method"></a><span data-ttu-id="e38a6-103">CShareLockNH:: TryExclusiveLock (método)</span><span class="sxs-lookup"><span data-stu-id="e38a6-103">CShareLockNH::TryExclusiveLock method</span></span>

<span data-ttu-id="e38a6-104">Obtiene un bloqueo de forma exclusiva si ningún otro lo mantiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="e38a6-104">Obtains a lock exclusively if no others are currently hold it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e38a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e38a6-105">Syntax</span></span>


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="e38a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e38a6-106">Parameters</span></span>

<span data-ttu-id="e38a6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e38a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e38a6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e38a6-108">Return value</span></span>

<span data-ttu-id="e38a6-109">Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="e38a6-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e38a6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e38a6-110">Remarks</span></span>

<span data-ttu-id="e38a6-111">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e38a6-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e38a6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e38a6-112">Requirements</span></span>



| <span data-ttu-id="e38a6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e38a6-113">Requirement</span></span> | <span data-ttu-id="e38a6-114">Value</span><span class="sxs-lookup"><span data-stu-id="e38a6-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e38a6-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e38a6-115">DLL</span></span><br/> | <dl> <span data-ttu-id="e38a6-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e38a6-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
