---
description: Destruye un objeto de dispositivo de Microsoft DirectDraw de modo kernel creado previamente.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Función NtGdiDdDeleteDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152808"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a><span data-ttu-id="98889-103">NtGdiDdDeleteDirectDrawObject función)</span><span class="sxs-lookup"><span data-stu-id="98889-103">NtGdiDdDeleteDirectDrawObject function</span></span>

<span data-ttu-id="98889-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="98889-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="98889-105">En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="98889-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="98889-106">Destruye un objeto de dispositivo de Microsoft DirectDraw de modo kernel creado previamente.</span><span class="sxs-lookup"><span data-stu-id="98889-106">Destroys a previously created kernel-mode Microsoft DirectDraw device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="98889-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98889-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a><span data-ttu-id="98889-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98889-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98889-109">*hDirectDrawLocal*</span><span class="sxs-lookup"><span data-stu-id="98889-109">*hDirectDrawLocal*</span></span> 
</dt> <dd>

<span data-ttu-id="98889-110">Identificador del objeto de dispositivo DirectDraw en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="98889-110">Handle to the kernel-mode DirectDraw device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98889-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98889-111">Return value</span></span>

<span data-ttu-id="98889-112">Si se realiza correctamente, esta función devuelve **true**; en caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="98889-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="98889-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98889-113">Remarks</span></span>

<span data-ttu-id="98889-114">Se recomienda que las aplicaciones usen las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="98889-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="98889-115">Estas construcciones abstraen el proceso de creación de dispositivos de una manera simplificada y independiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="98889-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="98889-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98889-116">Requirements</span></span>



| <span data-ttu-id="98889-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="98889-117">Requirement</span></span> | <span data-ttu-id="98889-118">Value</span><span class="sxs-lookup"><span data-stu-id="98889-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98889-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98889-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98889-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98889-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="98889-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98889-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98889-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98889-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="98889-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98889-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98889-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="98889-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98889-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="98889-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98889-126">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="98889-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="98889-127">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="98889-127">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[<span data-ttu-id="98889-128">**DdDeleteDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="98889-128">**DdDeleteDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
