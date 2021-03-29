---
description: Cambia un bloqueo compartido a un bloqueo parcial.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'CShareLockNH:: SharedToPartial (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660484"
---
# <a name="csharelocknhsharedtopartial-method"></a><span data-ttu-id="b0a29-103">CShareLockNH:: SharedToPartial (método)</span><span class="sxs-lookup"><span data-stu-id="b0a29-103">CShareLockNH::SharedToPartial method</span></span>

<span data-ttu-id="b0a29-104">Cambia un bloqueo compartido a un bloqueo parcial.</span><span class="sxs-lookup"><span data-stu-id="b0a29-104">Changes a shared lock to a partial lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a29-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0a29-105">Syntax</span></span>


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a><span data-ttu-id="b0a29-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0a29-106">Parameters</span></span>

<span data-ttu-id="b0a29-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b0a29-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0a29-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0a29-108">Return value</span></span>

<span data-ttu-id="b0a29-109">Devuelve **true** si se obtiene el bloqueo parcial; de lo contrario, devuelve **false** y el bloqueo permanece en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="b0a29-109">Returns **TRUE** if the partial lock is obtained; otherwise, it returns **FALSE** and the lock remains in shared mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a29-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0a29-110">Remarks</span></span>

<span data-ttu-id="b0a29-111">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b0a29-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a29-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0a29-112">Requirements</span></span>



| <span data-ttu-id="b0a29-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0a29-113">Requirement</span></span> | <span data-ttu-id="b0a29-114">Value</span><span class="sxs-lookup"><span data-stu-id="b0a29-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a29-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0a29-115">DLL</span></span><br/> | <dl> <span data-ttu-id="b0a29-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0a29-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
