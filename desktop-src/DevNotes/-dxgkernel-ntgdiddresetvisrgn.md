---
description: Se utiliza para habilitar el modo de usuario con el fin de obtener una descripción válida de la región de recorte para Windows en el escritorio. Este recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos del modo de usuario.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Función NtGdiDdResetVisrgn (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906972"
---
# <a name="ntgdiddresetvisrgn-function"></a><span data-ttu-id="43474-104">NtGdiDdResetVisrgn función)</span><span class="sxs-lookup"><span data-stu-id="43474-104">NtGdiDdResetVisrgn function</span></span>

<span data-ttu-id="43474-105">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="43474-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="43474-106">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="43474-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="43474-107">Se utiliza para habilitar el modo de usuario con el fin de obtener una descripción válida de la región de recorte para Windows en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="43474-107">Used to enable the user mode to gain a valid understanding of the clipping region for windows on the desktop.</span></span> <span data-ttu-id="43474-108">Este recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos del modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="43474-108">This clipping can change asynchronously from the point of view of user-mode threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="43474-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43474-109">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="43474-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43474-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43474-111">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43474-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43474-112">Puntero al objeto de modo de usuario de cualquier superficie que pertenezca al dispositivo DirectDraw para el que se va a restablecer el recorte.</span><span class="sxs-lookup"><span data-stu-id="43474-112">Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset.</span></span> <span data-ttu-id="43474-113">Para obtener más información, consulte la documentación de DDK.</span><span class="sxs-lookup"><span data-stu-id="43474-113">For details, see the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="43474-114">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43474-114">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43474-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="43474-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43474-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43474-116">Return value</span></span>

<span data-ttu-id="43474-117">Si se realiza correctamente, esta función devuelve **true**; en caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="43474-117">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="43474-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43474-118">Remarks</span></span>

<span data-ttu-id="43474-119">El recorte puede cambiar de forma asincrónica desde el punto de vista de los subprocesos del modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="43474-119">Clipping can change asynchronously from the point of view of user-mode threads.</span></span> <span data-ttu-id="43474-120">Las partes del modo kernel de DirectDraw y Windows Interfaz de dispositivo gráfico (GDI) mantienen un contador que se incrementa cada vez que cambia la lista de recortes para todo el escritorio.</span><span class="sxs-lookup"><span data-stu-id="43474-120">The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes.</span></span> <span data-ttu-id="43474-121">Una llamada a esta función registra este contador con todas las superficies principales de DirectDraw existentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="43474-121">A call to this function records this counter with every existing DirectDraw primary surface on the system.</span></span>

<span data-ttu-id="43474-122">En cualquier momento posterior, cuando una de estas superficies principales se modifica mediante una operación [IDirectDrawSurface7:: BLT](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) o [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) (consulte la documentación del DDK), el contador registrado con la superficie se compara con el contador global.</span><span class="sxs-lookup"><span data-stu-id="43474-122">At any later time when one of these primary surfaces is modified by a [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) or [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) operation (see DDK documentation), then the counter recorded with the surface is compared with the global counter.</span></span> <span data-ttu-id="43474-123">Si estos valores son diferentes, se devuelve un código de error DDERR \_ VISRGNCHANGED al código del modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="43474-123">If these values are different, an error code DDERR\_VISRGNCHANGED is returned to the user-mode code.</span></span> <span data-ttu-id="43474-124">Después, el código de modo de usuario volverá a consultar el recorte actual del escritorio, llamará a **NtGdiDdResetVisrgn** y volverá a intentar el IDirectDrawSurface7:: BLT aplicado a la superficie primaria, respetando el nuevo recorte.</span><span class="sxs-lookup"><span data-stu-id="43474-124">The user-mode code will then re-query the current clipping for the desktop, call **NtGdiDdResetVisrgn**, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping.</span></span> <span data-ttu-id="43474-125">Finalmente, el recorte que ha muestreado el código en modo de usuario será el mismo que el recorte actual propiedad del modo kernel y se permitirá que IDirectDrawSurface7:: BLT continúe.</span><span class="sxs-lookup"><span data-stu-id="43474-125">Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.</span></span>

<span data-ttu-id="43474-126">Se recomienda a las aplicaciones que usen la interfaz [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) o [IDirect3DDevice8::P método reenviado](/previous-versions/ms889707(v=msdn.10)) para controlar los cambios de recorte asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="43474-126">Applications are advised to use the [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) interface or [IDirect3DDevice8::Present](/previous-versions/ms889707(v=msdn.10)) method to handle asynchronous clipping changes.</span></span> <span data-ttu-id="43474-127">Estas construcciones implementan el recorte asincrónico de una forma independiente del sistema operativo y automatizada.</span><span class="sxs-lookup"><span data-stu-id="43474-127">These constructs implement asynchronous clipping in an automated and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="43474-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43474-128">Requirements</span></span>



| <span data-ttu-id="43474-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="43474-129">Requirement</span></span> | <span data-ttu-id="43474-130">Value</span><span class="sxs-lookup"><span data-stu-id="43474-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43474-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43474-131">Minimum supported client</span></span><br/> | <span data-ttu-id="43474-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="43474-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="43474-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43474-133">Minimum supported server</span></span><br/> | <span data-ttu-id="43474-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="43474-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43474-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43474-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="43474-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="43474-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43474-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="43474-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43474-138">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="43474-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="43474-139">**DdResetVisrgn**</span><span class="sxs-lookup"><span data-stu-id="43474-139">**DdResetVisrgn**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
