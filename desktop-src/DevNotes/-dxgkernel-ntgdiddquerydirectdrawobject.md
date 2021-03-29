---
description: Consulta una representación de modo kernel creada anteriormente de un objeto DirectDraw de Microsoft para sus capacidades.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Función NtGdiDdQueryDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907403"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a><span data-ttu-id="657a3-103">NtGdiDdQueryDirectDrawObject función)</span><span class="sxs-lookup"><span data-stu-id="657a3-103">NtGdiDdQueryDirectDrawObject function</span></span>

<span data-ttu-id="657a3-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="657a3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="657a3-105">En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="657a3-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="657a3-106">Consulta una representación de modo kernel creada anteriormente de un objeto DirectDraw de Microsoft para sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="657a3-106">Queries a previously created kernel-mode representation of a Microsoft DirectDraw object for its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="657a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="657a3-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a><span data-ttu-id="657a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="657a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="657a3-109">*hDirectDrawLocal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="657a3-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-110">Identificador del dispositivo DirectDraw en modo kernel creado previamente.</span><span class="sxs-lookup"><span data-stu-id="657a3-110">Handle to the previously-created kernel-mode DirectDraw device.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-111">*pHalInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-111">*pHalInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-112">Puntero a una estructura [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) que se rellenará con las funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="657a3-112">Pointer to a [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) structure that will be filled with the device's capabilities.</span></span> <span data-ttu-id="657a3-113">Consulte la documentación de DDK para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="657a3-113">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-114">*pCallBackFlags*</span><span class="sxs-lookup"><span data-stu-id="657a3-114">*pCallBackFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="657a3-115">Puntero a un búfer proporcionado por el autor de la llamada que almacena marcas de devolución de llamada detectadas por el controlador.</span><span class="sxs-lookup"><span data-stu-id="657a3-115">Pointer to a caller-provided buffer that stores driver-reported callback flags.</span></span> <span data-ttu-id="657a3-116">El búfer debe tener el tamaño 3 \* (DWORD) y almacena las marcas de devolución de llamada en el orden siguiente: pCallBackFlags \[ 0 \] para las marcas en las [**\_ devoluciones de llamada de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), PCallBackFlags \[ 1 para las \] marcas en [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)y pCallBackFlags \[ 2 para las \] marcas en [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span><span class="sxs-lookup"><span data-stu-id="657a3-116">The buffer should be of size 3\*sizeof(DWORD) and stores callback flags in the following order: pCallBackFlags\[0\] for flags in [**DD\_CALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags\[1\] for flags in [**DD\_SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks), and pCallBackFlags\[2\] for flags in [**DD\_PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span></span> <span data-ttu-id="657a3-117">Consulte la documentación de DDK para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="657a3-117">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-118">*puD3dCallbacks* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-118">*puD3dCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-119">Puntero a una tabla de punteros de devolución de llamada de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="657a3-119">Pointer to a table of Direct3D callback pointers.</span></span> <span data-ttu-id="657a3-120">La tabla se rellena con punteros a funciones dentro de Gdi32.dll que imitan un controlador de pantalla de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="657a3-120">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="657a3-121">Esta tabla de devolución de llamada es idéntica a la estructura D3DHAL D3DCALLBACKS que se \_ describe en la documentación de DDK.</span><span class="sxs-lookup"><span data-stu-id="657a3-121">This callback table is identical to the D3DHAL\_D3DCALLBACKS structure discussed in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-122">*puD3dDriverData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-122">*puD3dDriverData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-123">Puntero a los datos de [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) , tal como se describe en la documentación de DDK.</span><span class="sxs-lookup"><span data-stu-id="657a3-123">Pointer to [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) data, as described in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-124">*puD3dBufferCallbacks* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-124">*puD3dBufferCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-125">Puntero a una tabla de punteros de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="657a3-125">Pointer to a table of callback pointers.</span></span> <span data-ttu-id="657a3-126">La tabla se rellena con punteros a funciones dentro de Gdi32.dll que imitan un controlador de pantalla de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="657a3-126">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="657a3-127">Esta tabla de devolución de llamada es idéntica a la \_ estructura DDHAL DDEXEBUFCALLBACKS, que se asigna a la estructura [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) descrita en la documentación de DDK, salvo que los miembros XxxD3DBuffer en **DD \_ D3DBUFCALLBACKS** se reemplazan por XxxExecuteBuffer en DDHAL \_ DDEXEBUFCALLBACKS.</span><span class="sxs-lookup"><span data-stu-id="657a3-127">This callback table is identical to the DDHAL\_DDEXEBUFCALLBACKS structure, which maps to the [**DD\_D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) structure discussed in the DDK documentation, except that members XxxD3DBuffer in **DD\_D3DBUFCALLBACKS** are replaced with XxxExecuteBuffer in DDHAL\_DDEXEBUFCALLBACKS.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-128">*puD3dTextureFormats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-128">*puD3dTextureFormats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-129">Puntero a una matriz de estructuras [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que definen el conjunto de formatos de textura permitidos.</span><span class="sxs-lookup"><span data-stu-id="657a3-129">Pointer to an array of [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structures that define the set of permissible texture formats.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-130">*puNumHeaps* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-130">*puNumHeaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-131">Puntero al miembro **dwNumHeaps** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span><span class="sxs-lookup"><span data-stu-id="657a3-131">Pointer to the **dwNumHeaps** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span></span> <span data-ttu-id="657a3-132">El miembro **dwNumHeaps** especifica el número de montones de memoria en *puvmList*.</span><span class="sxs-lookup"><span data-stu-id="657a3-132">The **dwNumHeaps** member specifies the number of memory heaps in *puvmList*.</span></span> <span data-ttu-id="657a3-133">Consulte la documentación de DDK para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="657a3-133">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-134">*puvmList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-134">*puvmList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-135">Puntero a una lista de descriptores del montón de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="657a3-135">Pointer to a list of video memory heap descriptors.</span></span> <span data-ttu-id="657a3-136">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="657a3-136">Can be **NULL**.</span></span> <span data-ttu-id="657a3-137">Este parámetro no se usa porque la administración de la memoria de vídeo se controla completamente dentro del modo kernel.</span><span class="sxs-lookup"><span data-stu-id="657a3-137">This parameter is not used because video memory management is handled entirely within kernel mode.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-138">*puNumFourCC* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-138">*puNumFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-139">Puntero al miembro **puNumFourCCCodes** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span><span class="sxs-lookup"><span data-stu-id="657a3-139">Pointer to the **puNumFourCCCodes** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span></span> <span data-ttu-id="657a3-140">El miembro **puNumFourCCCodes** especifica el número de códigos de [cuatro caracteres (FourCC)](../directshow/fourcc-codes.md) que admite el controlador.</span><span class="sxs-lookup"><span data-stu-id="657a3-140">The **puNumFourCCCodes** member specifies the number of [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) codes that the driver supports.</span></span> <span data-ttu-id="657a3-141">Consulte la documentación de DDK para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="657a3-141">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="657a3-142">*puFourCC* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="657a3-142">*puFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="657a3-143">Puntero a una lista de formatos de superficie admitidos de [códigos de cuatro caracteres (FourCC)](../directshow/fourcc-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="657a3-143">Pointer to a list of supported [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) surface formats.</span></span> <span data-ttu-id="657a3-144">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="657a3-144">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="657a3-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="657a3-145">Return value</span></span>

<span data-ttu-id="657a3-146">Si se realiza correctamente, esta función devuelve **true**; en caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="657a3-146">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="657a3-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="657a3-147">Remarks</span></span>

<span data-ttu-id="657a3-148">Una llamada a esta función está diseñada para realizarse en un proceso de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="657a3-148">A call to this function is designed to be made in a two-step process.</span></span> <span data-ttu-id="657a3-149">En el primer paso, *puFourCC*, *puvmList* y *PuD3dTextureFormats* deben ser **null** y [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) se rellenará como [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. **dwNumFourCCCodes**, **DD \_ HALINFO**.**vmiData**. **dwNumHeaps** y [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** con el número de entradas que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="657a3-149">In the first step, *puFourCC*, *puvmList* and *puD3dTextureFormats* should be **NULL**, and [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) will fill in [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.**dwNumFourCCCodes**, **DD\_HALINFO**.**vmiData**.**dwNumHeaps**, and [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** with the number of entries that are to be returned.</span></span> <span data-ttu-id="657a3-150">En la segunda llamada, el llamador debe asignar matrices del tamaño indicado y pasar esos punteros en lugar de valores **null** en los parámetros *puFourCC*, *puvmList* y *puD3dTextureFormats* .</span><span class="sxs-lookup"><span data-stu-id="657a3-150">In the second call, the caller should allocate arrays of the indicated size and pass those pointers instead of **NULL** values in the *puFourCC*, *puvmList* and *puD3dTextureFormats* parameters.</span></span> <span data-ttu-id="657a3-151">A continuación, las matrices se rellenarán con los datos adecuados.</span><span class="sxs-lookup"><span data-stu-id="657a3-151">The arrays will then be populated with appropriate data.</span></span>

<span data-ttu-id="657a3-152">Se recomienda que las aplicaciones usen las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="657a3-152">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="657a3-153">Estas construcciones abstraen el proceso de creación de dispositivos de una manera simplificada y independiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="657a3-153">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="657a3-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="657a3-154">Requirements</span></span>



| <span data-ttu-id="657a3-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="657a3-155">Requirement</span></span> | <span data-ttu-id="657a3-156">Value</span><span class="sxs-lookup"><span data-stu-id="657a3-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="657a3-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="657a3-157">Minimum supported client</span></span><br/> | <span data-ttu-id="657a3-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="657a3-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="657a3-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="657a3-159">Minimum supported server</span></span><br/> | <span data-ttu-id="657a3-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="657a3-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="657a3-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="657a3-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="657a3-162"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="657a3-162"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="657a3-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="657a3-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657a3-164">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="657a3-164">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="657a3-165">**DdQueryDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="657a3-165">**DdQueryDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[<span data-ttu-id="657a3-166">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="657a3-166">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
