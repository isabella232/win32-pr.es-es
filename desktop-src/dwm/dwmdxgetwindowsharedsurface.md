---
description: Recupera la superficie compartida de DirectX que respalda una ventana determinada. Esta superficie se puede escribir en para actualizar el contenido de la ventana.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface función)
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
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715647"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a><span data-ttu-id="a4377-104">DwmDxGetWindowSharedSurface función)</span><span class="sxs-lookup"><span data-stu-id="a4377-104">DwmDxGetWindowSharedSurface function</span></span>

<span data-ttu-id="a4377-105">Recupera la superficie compartida de DirectX que respalda una ventana determinada.</span><span class="sxs-lookup"><span data-stu-id="a4377-105">Retrieves the DirectX shared surface backing a given window.</span></span> <span data-ttu-id="a4377-106">Esta superficie se puede escribir en para actualizar el contenido de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a4377-106">This surface can be written to in order to update the contents of the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4377-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4377-107">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a><span data-ttu-id="a4377-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4377-108">Parameters</span></span>

`hwnd`

<span data-ttu-id="a4377-109">[**HWnd**](/windows/desktop/winprog/windows-data-types) que especifica la ventana que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="a4377-109">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window to be updated.</span></span>

`luidAdapter`

<span data-ttu-id="a4377-110">[**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) del adaptador donde se debe ubicar la superficie.</span><span class="sxs-lookup"><span data-stu-id="a4377-110">The [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) of the adapter where the surface should be located.</span></span>

`hmonitorAssociation`

<span data-ttu-id="a4377-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a4377-111">Reserved.</span></span>

`dwFlags`

<span data-ttu-id="a4377-112">Este parámetro puede ser uno de los valores siguientes, o una combinación OR bit a bit de varios valores cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a4377-112">This parameter can be one of the following values, or a bitwise OR combination of multiple values where appropriate.</span></span>

| <span data-ttu-id="a4377-113">Value</span><span class="sxs-lookup"><span data-stu-id="a4377-113">Value</span></span> | <span data-ttu-id="a4377-114">Significado</span><span class="sxs-lookup"><span data-stu-id="a4377-114">Meaning</span></span> |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <span data-ttu-id="a4377-115"><dt>**DWM \_ \_ \_ Espera de la marca de redireccionamiento**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a4377-115"><dt>**DWM\_REDIRECTION\_FLAG\_WAIT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="a4377-116">Hace que la función se bloquee hasta que haya transcurrido una sincronización vertical (VSync) desde la última vez que se llamó a la función correctamente.</span><span class="sxs-lookup"><span data-stu-id="a4377-116">Causes the function to block until a vertical synchronization (VSync) has passed since the last time the function was called successfully.</span></span> |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <span data-ttu-id="a4377-117"><dt>**DWM \_ \_Compatibilidad con la marca de REdireccionamiento \_ \_ presente \_ en la \_ \_ superficie de GDI**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="a4377-117"><dt>**DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="a4377-118">Indica que la aplicación que realiza la llamada es capaz de presentar en una superficie compartida de GDI.</span><span class="sxs-lookup"><span data-stu-id="a4377-118">Indicates that the calling application is capable of presenting to a GDI shared surface.</span></span> |

`pfmtWindow`

<span data-ttu-id="a4377-119">En la entrada, el formato deseado de la superficie.</span><span class="sxs-lookup"><span data-stu-id="a4377-119">On input, the desired format of the surface.</span></span> <span data-ttu-id="a4377-120">En la salida, el formato real de la superficie devuelta.</span><span class="sxs-lookup"><span data-stu-id="a4377-120">On output, the actual format of the returned surface.</span></span>

`phDxSurface`

<span data-ttu-id="a4377-121">En la salida, el identificador compartido de la superficie.</span><span class="sxs-lookup"><span data-stu-id="a4377-121">On output, the shared handle to the surface.</span></span>

`puiUpdateId`

<span data-ttu-id="a4377-122">En la salida, identificador de la actualización.</span><span class="sxs-lookup"><span data-stu-id="a4377-122">On output, the ID of the update.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4377-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4377-123">Return value</span></span>

<span data-ttu-id="a4377-124">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a4377-124">This function can return one of these values.</span></span>

| <span data-ttu-id="a4377-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a4377-125">Return code</span></span> | <span data-ttu-id="a4377-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4377-126">Description</span></span> |
|-|-|
| <span data-ttu-id="a4377-127">**S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="a4377-127">**S\_OK**</span></span> | <span data-ttu-id="a4377-128">La llamada se realizó correctamente y debe actualizar la superficie, asegurándose de pasar el identificador de la actualización a [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (en el miembro **PresentHistoryToken** de la estructura de **\_ representación D3DKMT** cuando se envía la actualización y, a continuación, se debe llamar a [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) con el mismo identificador de actualización.</span><span class="sxs-lookup"><span data-stu-id="a4377-128">The call succeeded, and you should update the surface, being sure to pass the update ID to [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (in the **PresentHistoryToken** member of the **D3DKMT\_RENDER** structure when the update is submitted, and then [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) should be called with the same update ID.</span></span> <span data-ttu-id="a4377-129">Tenga en cuenta que se debe llamar a **DwmDxUpdateWindowSharedSurface** independientemente de si la superficie se actualizó realmente o no.</span><span class="sxs-lookup"><span data-stu-id="a4377-129">Note that **DwmDxUpdateWindowSharedSurface** should be called regardless of whether the surface was actually updated or not.</span></span> |
| <span data-ttu-id="a4377-130">**\_superficie de \_ \_ redirección GDI \_ de DWM S**</span><span class="sxs-lookup"><span data-stu-id="a4377-130">**DWM\_S\_GDI\_REDIRECTION\_SURFACE**</span></span> | <span data-ttu-id="a4377-131">La llamada se realizó correctamente y debe actualizar la superficie llamando a [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)y estableciendo el **modelo** de miembro de **PresentHistoryToken** en **D3DKMT \_ PM \_ Redirigido \_ BLT** y proporcionando el identificador de actualización en el miembro **BLT** de la Unión.</span><span class="sxs-lookup"><span data-stu-id="a4377-131">The call succeeded, and you should update the surface by calling [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent), and setting **PresentHistoryToken** member's **Model** to **D3DKMT\_PM\_REDIRECTED\_BLT**, and providing the update ID in the **Blt** member of the union.</span></span> <span data-ttu-id="a4377-132">Este valor solo se devuelve si **la \_ \_ compatibilidad con la marca de redirección \_ de DWM presente en la \_ \_ \_ \_ superficie de GDI** se especificó en *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="a4377-132">This value is only returned if **DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE** was specified in *dwFlags*.</span></span> |
| <span data-ttu-id="a4377-133">**\_ \_ \_ no \_ se encontró el adaptador de DWM E**</span><span class="sxs-lookup"><span data-stu-id="a4377-133">**DWM\_E\_ADAPTER\_NOT\_FOUND**</span></span> | <span data-ttu-id="a4377-134">El valor de *luidAdapter* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a4377-134">The value of *luidAdapter* is not valid.</span></span> |
| <span data-ttu-id="a4377-135">**COMPOSITIONDISABLED de DWM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a4377-135">**DWM\_E\_COMPOSITIONDISABLED**</span></span> | <span data-ttu-id="a4377-136">DWM no está habilitado actualmente y la aplicación tendrá que presentar otra manera.</span><span class="sxs-lookup"><span data-stu-id="a4377-136">DWM is not currently enabled, and the application will need to present another way.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a4377-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4377-137">Remarks</span></span>

<span data-ttu-id="a4377-138">Esta API está pensada para implementar un controlador de gráficos o un entorno de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a4377-138">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="a4377-139">Una aplicación no puede llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="a4377-139">An application may not call this method.</span></span> <span data-ttu-id="a4377-140">Esta documentación solo es válida para Windows 7 y no se garantiza que esta API exista ni se comporte de forma similar en otras versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="a4377-140">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="a4377-141">Esta función no está presente en ningún encabezado ni en una biblioteca de vínculos estáticos, y se encuentra en el ordinal 100 en dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="a4377-141">This function is not present in any header or static-link library, and it is located at ordinal 100 in dwmapi.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4377-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4377-142">Requirements</span></span>

| <span data-ttu-id="a4377-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4377-143">Requirement</span></span> | <span data-ttu-id="a4377-144">Value</span><span class="sxs-lookup"><span data-stu-id="a4377-144">Value</span></span> |
|-|-|
| <span data-ttu-id="a4377-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4377-145">Minimum supported client</span></span> | <span data-ttu-id="a4377-146">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4377-146">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="a4377-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4377-147">Minimum supported server</span></span> | <span data-ttu-id="a4377-148">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a4377-148">None supported</span></span> |
| <span data-ttu-id="a4377-149">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a4377-149">End of client support</span></span> | <span data-ttu-id="a4377-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a4377-150">Windows 7</span></span> |
| <span data-ttu-id="a4377-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4377-151">Header</span></span> | <span data-ttu-id="a4377-152">N/D</span><span class="sxs-lookup"><span data-stu-id="a4377-152">N/A</span></span> |
| <span data-ttu-id="a4377-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a4377-153">DLL</span></span> | <span data-ttu-id="a4377-154">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="a4377-154">Dwmapi.dll</span></span> |
