---
description: La función DllGetVersion recupera el número de versión de Cabinet.dll mediante la estructura CABINETDLLVERSIONINFO.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: DllGetVersion función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649670"
---
# <a name="dllgetversion-function"></a><span data-ttu-id="4bf89-103">DllGetVersion función)</span><span class="sxs-lookup"><span data-stu-id="4bf89-103">DllGetVersion function</span></span>

<span data-ttu-id="4bf89-104">\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.\]</span><span class="sxs-lookup"><span data-stu-id="4bf89-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="4bf89-105">La función **DllGetVersion** recupera el número de versión de Cabinet.dll mediante la estructura [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="4bf89-105">The **DllGetVersion** function retrieves the version number of Cabinet.dll using the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf89-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bf89-106">Syntax</span></span>


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a><span data-ttu-id="4bf89-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bf89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf89-108">*pcdvi*</span><span class="sxs-lookup"><span data-stu-id="4bf89-108">*pcdvi*</span></span> 
</dt> <dd>

<span data-ttu-id="4bf89-109">Puntero a la estructura [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) que contiene la información de versión.</span><span class="sxs-lookup"><span data-stu-id="4bf89-109">Pointer to the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure that contains the version information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf89-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bf89-110">Return value</span></span>

<span data-ttu-id="4bf89-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4bf89-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bf89-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bf89-112">Remarks</span></span>

<span data-ttu-id="4bf89-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4bf89-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf89-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bf89-114">Requirements</span></span>



| <span data-ttu-id="4bf89-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bf89-115">Requirement</span></span> | <span data-ttu-id="4bf89-116">Value</span><span class="sxs-lookup"><span data-stu-id="4bf89-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf89-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bf89-117">DLL</span></span><br/> | <dl> <span data-ttu-id="4bf89-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bf89-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bf89-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bf89-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf89-120">**CABINETDLLVERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="4bf89-120">**CABINETDLLVERSIONINFO**</span></span>](cabinetdllversioninfo.md)
</dt> <dt>

[<span data-ttu-id="4bf89-121">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="4bf89-121">**GetDllVersion**</span></span>](getdllversion.md)
</dt> </dl>

 

 
