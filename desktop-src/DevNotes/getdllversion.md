---
description: La función GetDllVersion recupera el número de versión de Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660408"
---
# <a name="getdllversion-function"></a><span data-ttu-id="173d4-103">GetDllVersion función)</span><span class="sxs-lookup"><span data-stu-id="173d4-103">GetDllVersion function</span></span>

<span data-ttu-id="173d4-104">\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="173d4-104">\[This function is no longer supported, so its behavior cannot be guaranteed.</span></span> <span data-ttu-id="173d4-105">\]</span><span class="sxs-lookup"><span data-stu-id="173d4-105">\]</span></span>

<span data-ttu-id="173d4-106">La función **GetDllVersion** recupera el número de versión de Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="173d4-106">The **GetDllVersion** function retrieves the version number of Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="173d4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="173d4-107">Syntax</span></span>


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a><span data-ttu-id="173d4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="173d4-108">Parameters</span></span>

<span data-ttu-id="173d4-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="173d4-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="173d4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="173d4-110">Return value</span></span>

<span data-ttu-id="173d4-111">El número de versión del archivo (consulte el [recurso versionInfo](../menurc/versioninfo-resource.md)).</span><span class="sxs-lookup"><span data-stu-id="173d4-111">The version number of the file (see [VERSIONINFO Resource](../menurc/versioninfo-resource.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="173d4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="173d4-112">Remarks</span></span>

<span data-ttu-id="173d4-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="173d4-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="173d4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="173d4-114">Requirements</span></span>



| <span data-ttu-id="173d4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="173d4-115">Requirement</span></span> | <span data-ttu-id="173d4-116">Value</span><span class="sxs-lookup"><span data-stu-id="173d4-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="173d4-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="173d4-117">DLL</span></span><br/> | <dl> <span data-ttu-id="173d4-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="173d4-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="173d4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="173d4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="173d4-120">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="173d4-120">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 
