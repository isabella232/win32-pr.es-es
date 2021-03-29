---
description: Libera el contexto de dispositivo (DC) creado previamente para el objeto Surface de Microsoft DirectDraw de modo kernel indicado.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Función NtGdiDdReleaseDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906974"
---
# <a name="ntgdiddreleasedc-function"></a><span data-ttu-id="baaf9-103">NtGdiDdReleaseDC función)</span><span class="sxs-lookup"><span data-stu-id="baaf9-103">NtGdiDdReleaseDC function</span></span>

<span data-ttu-id="baaf9-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="baaf9-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="baaf9-105">En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="baaf9-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="baaf9-106">Libera el contexto de dispositivo (DC) creado previamente para el objeto Surface de Microsoft DirectDraw de modo kernel indicado.</span><span class="sxs-lookup"><span data-stu-id="baaf9-106">Releases the previously created device context (DC) for the indicated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="baaf9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baaf9-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="baaf9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baaf9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baaf9-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="baaf9-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baaf9-110">Identificador del objeto de la superficie de DirectDraw del modo kernel creado previamente.</span><span class="sxs-lookup"><span data-stu-id="baaf9-110">Handle to the previously created kernel-mode DirectDraw surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baaf9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="baaf9-111">Return value</span></span>

<span data-ttu-id="baaf9-112">Si se realiza correctamente, esta función devuelve **true**; en caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="baaf9-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="baaf9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="baaf9-113">Remarks</span></span>

<span data-ttu-id="baaf9-114">Las aplicaciones que necesitan obtener un controlador de dominio para una superficie de DirectDraw pueden usar [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), que expone esta funcionalidad de forma independiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="baaf9-114">Applications that need to obtain a DC for a DirectDraw surface may use [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), which exposes this functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="baaf9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baaf9-115">Requirements</span></span>



| <span data-ttu-id="baaf9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="baaf9-116">Requirement</span></span> | <span data-ttu-id="baaf9-117">Value</span><span class="sxs-lookup"><span data-stu-id="baaf9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="baaf9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baaf9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="baaf9-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="baaf9-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="baaf9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baaf9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="baaf9-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="baaf9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="baaf9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="baaf9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="baaf9-123"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="baaf9-123"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baaf9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="baaf9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baaf9-125">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="baaf9-125">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="baaf9-126">**DdReleaseDC**</span><span class="sxs-lookup"><span data-stu-id="baaf9-126">**DdReleaseDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
