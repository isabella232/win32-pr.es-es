---
description: Devuelve el valor actual de un contador de rendimiento y, opcionalmente, la frecuencia del contador de rendimiento.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670625"
---
# <a name="ntqueryperformancecounter-function"></a><span data-ttu-id="55fe9-103">NtQueryPerformanceCounter función)</span><span class="sxs-lookup"><span data-stu-id="55fe9-103">NtQueryPerformanceCounter function</span></span>

<span data-ttu-id="55fe9-104">\[Esta función no se admite y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="55fe9-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="55fe9-105">En su lugar, use las funciones **QueryPerformanceCounter** y **QueryPerformanceFrequency** .\]</span><span class="sxs-lookup"><span data-stu-id="55fe9-105">Use the **QueryPerformanceCounter** and **QueryPerformanceFrequency** functions instead.\]</span></span>

<span data-ttu-id="55fe9-106">Devuelve el valor actual de un contador de rendimiento y, opcionalmente, la frecuencia del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="55fe9-106">Returns the current value of a performance counter and, optionally, the frequency of the performance counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="55fe9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55fe9-107">Syntax</span></span>


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a><span data-ttu-id="55fe9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55fe9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55fe9-109">*PerformanceCounter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="55fe9-109">*PerformanceCounter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55fe9-110">Dirección de una variable para recibir el valor del contador de rendimiento actual.</span><span class="sxs-lookup"><span data-stu-id="55fe9-110">The address of a variable to receive the current performance counter value.</span></span>

</dd> <dt>

<span data-ttu-id="55fe9-111">*PerformanceFrequency* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="55fe9-111">*PerformanceFrequency* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55fe9-112">Dirección de una variable que va a recibir la frecuencia del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="55fe9-112">The address of a variable to receive the performance counter frequency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55fe9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55fe9-113">Return value</span></span>

<span data-ttu-id="55fe9-114">Si la función se ejecuta correctamente, devuelve el estado del código de **NTSTATUS** **\_ Success**; de lo contrario, devuelve un código de error como **\_ \_ infracción de acceso de estado**.</span><span class="sxs-lookup"><span data-stu-id="55fe9-114">If the function succeeds, it returns the **NTSTATUS** code **STATUS\_SUCCESS**; otherwise, it returns an error code such as **STATUS\_ACCESS\_VIOLATION**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55fe9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55fe9-115">Remarks</span></span>

<span data-ttu-id="55fe9-116">No hay ningún archivo de encabezado disponible para **NtQueryPerformanceCounter**.</span><span class="sxs-lookup"><span data-stu-id="55fe9-116">No header file is available for **NtQueryPerformanceCounter**.</span></span> <span data-ttu-id="55fe9-117">Debe utilizar las funciones alternativas mencionadas anteriormente, aunque también puede usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="55fe9-117">You should use the alternative functions named above, although you can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

<span data-ttu-id="55fe9-118">La frecuencia de rendimiento es la frecuencia del contador de rendimiento en hercios, en concreto en recuentos por segundo.</span><span class="sxs-lookup"><span data-stu-id="55fe9-118">Performance frequency is the frequency of the performance counter in hertz, specifically in counts per second.</span></span> <span data-ttu-id="55fe9-119">Este valor depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="55fe9-119">This value is implementation dependent.</span></span> <span data-ttu-id="55fe9-120">Si la implementación no tiene hardware para admitir el tiempo de rendimiento, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="55fe9-120">If the implementation does not have hardware to support performance timing, the value returned is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="55fe9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55fe9-121">Requirements</span></span>



| <span data-ttu-id="55fe9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="55fe9-122">Requirement</span></span> | <span data-ttu-id="55fe9-123">Value</span><span class="sxs-lookup"><span data-stu-id="55fe9-123">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55fe9-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55fe9-124">DLL</span></span><br/> | <dl> <span data-ttu-id="55fe9-125"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55fe9-125"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55fe9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="55fe9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55fe9-127">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="55fe9-127">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[<span data-ttu-id="55fe9-128">**QueryPerformanceFrequency**</span><span class="sxs-lookup"><span data-stu-id="55fe9-128">**QueryPerformanceFrequency**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
