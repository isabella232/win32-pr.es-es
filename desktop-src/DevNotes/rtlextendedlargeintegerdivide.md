---
description: Divide los enteros extendidos.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: RtlExtendedLargeIntegerDivide función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671272"
---
# <a name="rtlextendedlargeintegerdivide-function"></a><span data-ttu-id="66433-103">RtlExtendedLargeIntegerDivide función)</span><span class="sxs-lookup"><span data-stu-id="66433-103">RtlExtendedLargeIntegerDivide function</span></span>

<span data-ttu-id="66433-104">\[La función **RtlExtendedLargeIntegerDivide** se exporta para admitir los archivos binarios del controlador existentes y está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="66433-104">\[The **RtlExtendedLargeIntegerDivide** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="66433-105">Para mejorar el rendimiento, use la compatibilidad del compilador con las operaciones de enteros de 64 bits.\]</span><span class="sxs-lookup"><span data-stu-id="66433-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="66433-106">Divide los enteros extendidos.</span><span class="sxs-lookup"><span data-stu-id="66433-106">Divides extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="66433-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66433-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a><span data-ttu-id="66433-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66433-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66433-109">*Dividendo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66433-109">*Dividend* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66433-110">Divi.</span><span class="sxs-lookup"><span data-stu-id="66433-110">Dividend.</span></span>

</dd> <dt>

<span data-ttu-id="66433-111">*Divisor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66433-111">*Divisor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66433-112">Divisor.</span><span class="sxs-lookup"><span data-stu-id="66433-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="66433-113">*Resto* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="66433-113">*Remainder* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="66433-114">Puntero al resto de la división.</span><span class="sxs-lookup"><span data-stu-id="66433-114">Pointer to division remainder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66433-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66433-115">Return value</span></span>

<span data-ttu-id="66433-116">Devuelve el resultado de la operación de división.</span><span class="sxs-lookup"><span data-stu-id="66433-116">Returns the result of the division operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="66433-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66433-117">Remarks</span></span>

<span data-ttu-id="66433-118">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="66433-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="66433-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66433-119">Requirements</span></span>



| <span data-ttu-id="66433-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="66433-120">Requirement</span></span> | <span data-ttu-id="66433-121">Value</span><span class="sxs-lookup"><span data-stu-id="66433-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66433-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66433-122">DLL</span></span><br/> | <dl> <span data-ttu-id="66433-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66433-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
