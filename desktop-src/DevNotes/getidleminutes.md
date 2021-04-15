---
description: Obtiene el período de tiempo, en minutos, transcurrido desde la última actividad del usuario.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: GetIdleMinutes función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649679"
---
# <a name="getidleminutes-function"></a><span data-ttu-id="9baa7-103">GetIdleMinutes función)</span><span class="sxs-lookup"><span data-stu-id="9baa7-103">GetIdleMinutes function</span></span>

<span data-ttu-id="9baa7-104">\[Esta función no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="9baa7-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="9baa7-105">En su lugar, use la función **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="9baa7-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="9baa7-106">Obtiene el período de tiempo, en minutos, transcurrido desde la última actividad del usuario.</span><span class="sxs-lookup"><span data-stu-id="9baa7-106">Gets the length of time, in minutes, since the user's last activity.</span></span>

## <a name="syntax"></a><span data-ttu-id="9baa7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9baa7-107">Syntax</span></span>


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="9baa7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9baa7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9baa7-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="9baa7-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="9baa7-110">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="9baa7-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9baa7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9baa7-111">Return value</span></span>

<span data-ttu-id="9baa7-112">Devuelve el número de minutos transcurridos desde la última actividad del usuario.</span><span class="sxs-lookup"><span data-stu-id="9baa7-112">Returns the number of minutes since the user's last activity.</span></span>

## <a name="remarks"></a><span data-ttu-id="9baa7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9baa7-113">Remarks</span></span>

<span data-ttu-id="9baa7-114">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9baa7-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="9baa7-115">Esta función no se exporta por nombre; Especifique el ordinal 8 al llamar a **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="9baa7-115">This function is not exported by name; specify ordinal 8 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9baa7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9baa7-116">Requirements</span></span>



| <span data-ttu-id="9baa7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9baa7-117">Requirement</span></span> | <span data-ttu-id="9baa7-118">Value</span><span class="sxs-lookup"><span data-stu-id="9baa7-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9baa7-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9baa7-119">DLL</span></span><br/> | <dl> <span data-ttu-id="9baa7-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9baa7-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9baa7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9baa7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9baa7-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="9baa7-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
