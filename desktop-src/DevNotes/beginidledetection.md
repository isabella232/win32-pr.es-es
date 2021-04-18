---
description: Comienza la supervisión de inactividad.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671177"
---
# <a name="beginidledetection-function"></a><span data-ttu-id="c2305-103">BeginIdleDetection función)</span><span class="sxs-lookup"><span data-stu-id="c2305-103">BeginIdleDetection function</span></span>

<span data-ttu-id="c2305-104">\[Esta función no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="c2305-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="c2305-105">En su lugar, use la función **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="c2305-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="c2305-106">Comienza la supervisión de inactividad.</span><span class="sxs-lookup"><span data-stu-id="c2305-106">Begins monitoring inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2305-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2305-107">Syntax</span></span>


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="c2305-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2305-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2305-109">*pfnCallback*</span><span class="sxs-lookup"><span data-stu-id="c2305-109">*pfnCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="c2305-110">Función a la que se llama cuando cambia el estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="c2305-110">The function that is called when the idle state changes.</span></span> <span data-ttu-id="c2305-111">Esta devolución de llamada se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c2305-111">This callback is defined as follows:</span></span>

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

<span data-ttu-id="c2305-112">*dwIdleMin*</span><span class="sxs-lookup"><span data-stu-id="c2305-112">*dwIdleMin*</span></span> 
</dt> <dd>

<span data-ttu-id="c2305-113">El número de minutos de inactividad antes de que se realice la llamada a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c2305-113">The number of minutes of inactivity before the call is made to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c2305-114">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="c2305-114">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="c2305-115">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="c2305-115">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2305-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2305-116">Return value</span></span>

<span data-ttu-id="c2305-117">Devuelve 0 si la función se ejecuta correctamente; de lo contrario, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="c2305-117">Returns 0 if the function succeeds; otherwise, it returns an error code.</span></span> <span data-ttu-id="c2305-118">Por ejemplo, si *dwReserved* es distinto de 0, se devuelven los **\_ \_ datos no válidos** .</span><span class="sxs-lookup"><span data-stu-id="c2305-118">For example, if *dwReserved* is anything other than 0, **ERROR\_INVALID\_DATA** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2305-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2305-119">Remarks</span></span>

<span data-ttu-id="c2305-120">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c2305-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="c2305-121">Esta función no se exporta por nombre; Especifique el ordinal 3 al llamar a **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="c2305-121">This function is not exported by name; specify ordinal 3 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2305-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2305-122">Requirements</span></span>



| <span data-ttu-id="c2305-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2305-123">Requirement</span></span> | <span data-ttu-id="c2305-124">Value</span><span class="sxs-lookup"><span data-stu-id="c2305-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2305-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2305-125">DLL</span></span><br/> | <dl> <span data-ttu-id="c2305-126"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2305-126"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2305-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2305-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2305-128">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="c2305-128">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
