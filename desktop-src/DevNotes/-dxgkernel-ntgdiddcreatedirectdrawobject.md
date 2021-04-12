---
description: Crea una representación del kernel del objeto Microsoft DirectDraw.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Función NtGdiDdCreateDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152810"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a><span data-ttu-id="cfb6c-103">NtGdiDdCreateDirectDrawObject función)</span><span class="sxs-lookup"><span data-stu-id="cfb6c-103">NtGdiDdCreateDirectDrawObject function</span></span>

<span data-ttu-id="cfb6c-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cfb6c-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="cfb6c-105">En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="cfb6c-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="cfb6c-106">Crea una representación del kernel del objeto Microsoft DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="cfb6c-106">Creates a kernel-side representation of the Microsoft DirectDraw object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb6c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfb6c-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a><span data-ttu-id="cfb6c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfb6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb6c-109">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfb6c-109">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb6c-110">Cualquier dispositivo de pantalla DC para el que se debe crear el objeto DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="cfb6c-110">Any DC display device for which the DirectDraw object should be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb6c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfb6c-111">Return value</span></span>

<span data-ttu-id="cfb6c-112">Si se realiza correctamente, esta función devuelve un identificador a la representación del objeto en modo kernel; en caso contrario, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="cfb6c-112">If successful, this function returns a handle to the kernel-mode object representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb6c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfb6c-113">Remarks</span></span>

<span data-ttu-id="cfb6c-114">Se recomienda que las aplicaciones usen las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="cfb6c-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="cfb6c-115">Estas construcciones abstraen el proceso de creación de dispositivos de una manera simplificada y independiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cfb6c-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb6c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfb6c-116">Requirements</span></span>



| <span data-ttu-id="cfb6c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfb6c-117">Requirement</span></span> | <span data-ttu-id="cfb6c-118">Value</span><span class="sxs-lookup"><span data-stu-id="cfb6c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb6c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfb6c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb6c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cfb6c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cfb6c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfb6c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb6c-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cfb6c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cfb6c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfb6c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb6c-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb6c-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb6c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfb6c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb6c-126">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="cfb6c-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="cfb6c-127">**DdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="cfb6c-127">**DdCreateDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
