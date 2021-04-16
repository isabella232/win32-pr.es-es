---
description: Notifica a DWM una actualización entrante de una superficie compartida de ventana.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface función)
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544198"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a><span data-ttu-id="b9a26-103">DwmDxUpdateWindowSharedSurface función)</span><span class="sxs-lookup"><span data-stu-id="b9a26-103">DwmDxUpdateWindowSharedSurface function</span></span>

<span data-ttu-id="b9a26-104">Notifica a DWM una actualización entrante de una superficie compartida de ventana.</span><span class="sxs-lookup"><span data-stu-id="b9a26-104">Notifies the DWM of an incoming update to a window shared surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a26-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9a26-105">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a><span data-ttu-id="b9a26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9a26-106">Parameters</span></span>

`hwnd`

<span data-ttu-id="b9a26-107">[**HWnd**](/windows/desktop/winprog/windows-data-types) que especifica la ventana que se está actualizando.</span><span class="sxs-lookup"><span data-stu-id="b9a26-107">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window being updated.</span></span>

`uiUpdateId`

<span data-ttu-id="b9a26-108">IDENTIFICADOR de actualización recuperado de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span><span class="sxs-lookup"><span data-stu-id="b9a26-108">The update ID retrieved from [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span></span>

`dwFlags`

<span data-ttu-id="b9a26-109">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b9a26-109">Reserved.</span></span>

`hmonitorAssociation`

<span data-ttu-id="b9a26-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b9a26-110">Reserved.</span></span>

`prc`

<span data-ttu-id="b9a26-111">Rectángulo de la ventana que se está actualizando, en el espacio de coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b9a26-111">The rect of the window being updated, in window coordinate space.</span></span> <span data-ttu-id="b9a26-112">Un rectángulo nulo indica que no se ha actualizado ninguna región.</span><span class="sxs-lookup"><span data-stu-id="b9a26-112">A NULL rectangle indicates that no region was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9a26-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9a26-113">Return value</span></span>

<span data-ttu-id="b9a26-114">**S \_ Correcto si se** realiza correctamente, de lo contrario, un **HRESULT erróneo.**</span><span class="sxs-lookup"><span data-stu-id="b9a26-114">**S\_OK** if successful, otherwise a FAILED **HRESULT.**</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a26-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9a26-115">Remarks</span></span>

<span data-ttu-id="b9a26-116">Esta API está pensada para implementar un controlador de gráficos o un entorno de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b9a26-116">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="b9a26-117">Una aplicación no puede llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="b9a26-117">An application may not call this method.</span></span> <span data-ttu-id="b9a26-118">Esta documentación solo es válida para Windows 7 y no se garantiza que esta API exista ni se comporte de forma similar en otras versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="b9a26-118">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="b9a26-119">Esta función no está presente en ningún encabezado ni en una biblioteca de vínculos estáticos, y se encuentra en el ordinal 101 en dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="b9a26-119">This function is not present in any header or static-link library, and it is located at ordinal 101 in dwmapi.dll.</span></span>

<span data-ttu-id="b9a26-120">Solo se debe llamar a este método después de que [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) devuelva **S \_ OK** y se debe llamar en ese escenario, independientemente de si la superficie está actualizada o no.</span><span class="sxs-lookup"><span data-stu-id="b9a26-120">This method should only ever be called after [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) returns **S\_OK**, and must be called in that scenario, regardless of whether the surface is updated or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9a26-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9a26-121">Requirements</span></span>

| <span data-ttu-id="b9a26-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9a26-122">Requirement</span></span> | <span data-ttu-id="b9a26-123">Value</span><span class="sxs-lookup"><span data-stu-id="b9a26-123">Value</span></span> |
|-|-|
| <span data-ttu-id="b9a26-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9a26-124">Minimum supported client</span></span> | <span data-ttu-id="b9a26-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9a26-125">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="b9a26-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9a26-126">Minimum supported server</span></span> | <span data-ttu-id="b9a26-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b9a26-127">None supported</span></span> |
| <span data-ttu-id="b9a26-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b9a26-128">End of client support</span></span> | <span data-ttu-id="b9a26-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9a26-129">Windows 7</span></span> |
| <span data-ttu-id="b9a26-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9a26-130">Header</span></span> | <span data-ttu-id="b9a26-131">N/D</span><span class="sxs-lookup"><span data-stu-id="b9a26-131">N/A</span></span> |
| <span data-ttu-id="b9a26-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9a26-132">DLL</span></span> | <span data-ttu-id="b9a26-133">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="b9a26-133">Dwmapi.dll</span></span> |
