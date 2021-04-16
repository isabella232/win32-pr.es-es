---
description: La función ThunkConnect32 se usa en los controladores de dispositivo de 16 bits (para MS-DOS) que llaman al kernel de 32 bits.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649531"
---
# <a name="thunkconnect32-function"></a><span data-ttu-id="c1bc1-103">ThunkConnect32 función)</span><span class="sxs-lookup"><span data-stu-id="c1bc1-103">ThunkConnect32 function</span></span>

<span data-ttu-id="c1bc1-104">\[Esta función se admitía por compatibilidad con versiones anteriores, pero no está presente en las versiones actuales de Windows.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-104">\[This function was supported for backward compatibility, but is not present in current versions of Windows.</span></span> <span data-ttu-id="c1bc1-105">Los controladores de dispositivos nuevos deben ser de 32 a 64 bits y no necesitan esta función.\]</span><span class="sxs-lookup"><span data-stu-id="c1bc1-105">New device drivers should be 32- or 64-bit and do not need this function.\]</span></span>

<span data-ttu-id="c1bc1-106">La función **ThunkConnect32** se usa en los controladores de dispositivo de 16 bits (para MS-dos) que llaman al kernel de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-106">The **ThunkConnect32** function is used by 16-bit device drivers (for MS-DOS) that call into the 32-bit kernel.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1bc1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1bc1-107">Syntax</span></span>


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a><span data-ttu-id="c1bc1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1bc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1bc1-109">*lpThunkData32*</span><span class="sxs-lookup"><span data-stu-id="c1bc1-109">*lpThunkData32*</span></span> 
</dt> <dd>

<span data-ttu-id="c1bc1-110">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c1bc1-111">*pszThunkData16Name*</span><span class="sxs-lookup"><span data-stu-id="c1bc1-111">*pszThunkData16Name*</span></span> 
</dt> <dd>

<span data-ttu-id="c1bc1-112">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c1bc1-113">*pszDll16*</span><span class="sxs-lookup"><span data-stu-id="c1bc1-113">*pszDll16*</span></span> 
</dt> <dd>

<span data-ttu-id="c1bc1-114">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-114">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c1bc1-115">*pszDll32*</span><span class="sxs-lookup"><span data-stu-id="c1bc1-115">*pszDll32*</span></span> 
</dt> <dd>

<span data-ttu-id="c1bc1-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c1bc1-117">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="c1bc1-117">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="c1bc1-118">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-118">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c1bc1-119">*dwReason*</span><span class="sxs-lookup"><span data-stu-id="c1bc1-119">*dwReason*</span></span> 
</dt> <dd>

<span data-ttu-id="c1bc1-120">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-120">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1bc1-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1bc1-121">Return value</span></span>

<span data-ttu-id="c1bc1-122">Siempre devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="c1bc1-122">Always returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1bc1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1bc1-123">Requirements</span></span>



| <span data-ttu-id="c1bc1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1bc1-124">Requirement</span></span> | <span data-ttu-id="c1bc1-125">Value</span><span class="sxs-lookup"><span data-stu-id="c1bc1-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1bc1-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1bc1-126">DLL</span></span><br/> | <dl> <span data-ttu-id="c1bc1-127"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1bc1-127"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




