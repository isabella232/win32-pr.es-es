---
description: Indica la versión de CTL3D que se está ejecutando actualmente.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Ctl3dGetVer función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650058"
---
# <a name="ctl3dgetver-function"></a><span data-ttu-id="05191-103">Ctl3dGetVer función)</span><span class="sxs-lookup"><span data-stu-id="05191-103">Ctl3dGetVer function</span></span>

<span data-ttu-id="05191-104">Indica la versión de CTL3D que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="05191-104">Indicates the version of CTL3D that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="05191-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05191-105">Syntax</span></span>


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a><span data-ttu-id="05191-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05191-106">Parameters</span></span>

<span data-ttu-id="05191-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="05191-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05191-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05191-108">Return value</span></span>

<span data-ttu-id="05191-109">Devuelve un valor que contiene el número de versión principal en el byte de orden superior y el número de versión secundaria en el byte de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="05191-109">Returns a value that contains the major version number in the high-order byte and the minor version number in the low-order byte.</span></span>

## <a name="remarks"></a><span data-ttu-id="05191-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05191-110">Remarks</span></span>

<span data-ttu-id="05191-111">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="05191-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="05191-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05191-112">Requirements</span></span>



| <span data-ttu-id="05191-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="05191-113">Requirement</span></span> | <span data-ttu-id="05191-114">Value</span><span class="sxs-lookup"><span data-stu-id="05191-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05191-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05191-115">DLL</span></span><br/> | <dl> <span data-ttu-id="05191-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05191-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
