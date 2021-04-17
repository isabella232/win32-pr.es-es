---
description: Multiplica los enteros extendidos.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670699"
---
# <a name="rtlextendedintegermultiply-function"></a><span data-ttu-id="27576-103">RtlExtendedIntegerMultiply función)</span><span class="sxs-lookup"><span data-stu-id="27576-103">RtlExtendedIntegerMultiply function</span></span>

<span data-ttu-id="27576-104">\[La función **RtlExtendedIntegerMultiply** se exporta para admitir los archivos binarios del controlador existentes y está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="27576-104">\[The **RtlExtendedIntegerMultiply** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="27576-105">Para mejorar el rendimiento, use la compatibilidad del compilador con las operaciones de enteros de 64 bits.\]</span><span class="sxs-lookup"><span data-stu-id="27576-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="27576-106">Multiplica los enteros extendidos.</span><span class="sxs-lookup"><span data-stu-id="27576-106">Multiplies extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="27576-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27576-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a><span data-ttu-id="27576-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27576-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27576-109">*Multiplicando* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27576-109">*Multiplicand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27576-110">Multiplicando.</span><span class="sxs-lookup"><span data-stu-id="27576-110">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="27576-111">*Multiplicador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27576-111">*Multiplier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27576-112">Multiplicador.</span><span class="sxs-lookup"><span data-stu-id="27576-112">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27576-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27576-113">Return value</span></span>

<span data-ttu-id="27576-114">Devuelve el resultado de multiplicación.</span><span class="sxs-lookup"><span data-stu-id="27576-114">Returns multiplication result.</span></span>

## <a name="remarks"></a><span data-ttu-id="27576-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27576-115">Remarks</span></span>

<span data-ttu-id="27576-116">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="27576-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="27576-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27576-117">Requirements</span></span>



| <span data-ttu-id="27576-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="27576-118">Requirement</span></span> | <span data-ttu-id="27576-119">Value</span><span class="sxs-lookup"><span data-stu-id="27576-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27576-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27576-120">DLL</span></span><br/> | <dl> <span data-ttu-id="27576-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27576-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
