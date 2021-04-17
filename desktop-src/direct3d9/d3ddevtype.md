---
description: Define los tipos de dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumeración D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698212"
---
# <a name="d3ddevtype-enumeration"></a><span data-ttu-id="336a0-103">Enumeración D3DDEVTYPE</span><span class="sxs-lookup"><span data-stu-id="336a0-103">D3DDEVTYPE enumeration</span></span>

<span data-ttu-id="336a0-104">Define los tipos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="336a0-104">Defines device types.</span></span>

## <a name="syntax"></a><span data-ttu-id="336a0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="336a0-105">Syntax</span></span>


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a><span data-ttu-id="336a0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="336a0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="336a0-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**\_Hal D3DDEVTYPE**</span><span class="sxs-lookup"><span data-stu-id="336a0-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE\_HAL**</span></span>
</dt> <dd>

<span data-ttu-id="336a0-108">Rasterización de hardware.</span><span class="sxs-lookup"><span data-stu-id="336a0-108">Hardware rasterization.</span></span> <span data-ttu-id="336a0-109">El sombreado se realiza con el software, el hardware o la transformación y la iluminación mixtas.</span><span class="sxs-lookup"><span data-stu-id="336a0-109">Shading is done with software, hardware, or mixed transform and lighting.</span></span>

</dd> <dt>

<span data-ttu-id="336a0-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**</span><span class="sxs-lookup"><span data-stu-id="336a0-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE\_NULLREF**</span></span>
</dt> <dd>

<span data-ttu-id="336a0-111">Inicialice Direct3D en un equipo que no tenga hardware ni rasterización de referencia disponible y habilite los recursos para la creación de contenido 3D.</span><span class="sxs-lookup"><span data-stu-id="336a0-111">Initialize Direct3D on a computer that has neither hardware nor reference rasterization available, and enable resources for 3D content creation.</span></span> <span data-ttu-id="336a0-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="336a0-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="336a0-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**Referencia de D3DDEVTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="336a0-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE\_REF**</span></span>
</dt> <dd>

<span data-ttu-id="336a0-114">Las características de Direct3D se implementan en el software; sin embargo, el rasterizador de referencia hace uso de instrucciones de CPU especiales siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="336a0-114">Direct3D features are implemented in software; however, the reference rasterizer does make use of special CPU instructions whenever it can.</span></span>

<span data-ttu-id="336a0-115">El dispositivo de referencia se instala con el Windows SDK 8,0 o posterior y está pensado como ayuda para la depuración solo para el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="336a0-115">The reference device is installed by the Windows SDK 8.0 or later and is intended as an aid in debugging for development only.</span></span>

</dd> <dt>

<span data-ttu-id="336a0-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**</span><span class="sxs-lookup"><span data-stu-id="336a0-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE\_SW**</span></span>
</dt> <dd>

<span data-ttu-id="336a0-117">Un dispositivo de software acoplable que se ha registrado con [**IDirect3D9:: RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span><span class="sxs-lookup"><span data-stu-id="336a0-117">A pluggable software device that has been registered with [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span></span>

</dd> <dt>

<span data-ttu-id="336a0-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="336a0-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="336a0-119">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="336a0-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="336a0-120">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="336a0-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="336a0-121">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="336a0-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="336a0-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="336a0-122">Remarks</span></span>

<span data-ttu-id="336a0-123">Se producirá un error en todos los métodos de la interfaz [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) que toman un tipo de dispositivo **D3DDEVTYPE** si \_ se especifica D3DDEVTYPE NULLREF.</span><span class="sxs-lookup"><span data-stu-id="336a0-123">All methods of the [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) interface that take a **D3DDEVTYPE** device type will fail if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="336a0-124">Para usar estos métodos, sustituya D3DDEVTYPE \_ ref en la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="336a0-124">To use these methods, substitute D3DDEVTYPE\_REF in the method call.</span></span>

<span data-ttu-id="336a0-125">Se \_ debe crear un dispositivo de referencia D3DDEVTYPE en la \_ memoria temporal de D3DPOOL, a menos que se requieran búferes de vértices y de índices.</span><span class="sxs-lookup"><span data-stu-id="336a0-125">A D3DDEVTYPE\_REF device should be created in D3DPOOL\_SCRATCH memory, unless vertex and index buffers are required.</span></span> <span data-ttu-id="336a0-126">Para admitir los búferes de vértices y de índices, cree el dispositivo en D3DPOOL \_ SYSTEMMEM Memory.</span><span class="sxs-lookup"><span data-stu-id="336a0-126">To support vertex and index buffers, create the device in D3DPOOL\_SYSTEMMEM memory.</span></span>

<span data-ttu-id="336a0-127">Si D3dref9.dll está instalado, Direct3D usará el rasterizador de referencia para crear un \_ tipo de dispositivo D3DDEVTYPE Ref, incluso si \_ se especifica D3DDEVTYPE NULLREF.</span><span class="sxs-lookup"><span data-stu-id="336a0-127">If D3dref9.dll is installed, Direct3D will use the reference rasterizer to create a D3DDEVTYPE\_REF device type, even if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="336a0-128">Si D3dref9.dll no está disponible y \_ se especifica D3DDEVTYPE NULLREF, Direct3D no representará ni presentará la escena.</span><span class="sxs-lookup"><span data-stu-id="336a0-128">If D3dref9.dll is not available and D3DDEVTYPE\_NULLREF is specified, Direct3D will neither render nor present the scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="336a0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="336a0-129">Requirements</span></span>



| <span data-ttu-id="336a0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="336a0-130">Requirement</span></span> | <span data-ttu-id="336a0-131">Value</span><span class="sxs-lookup"><span data-stu-id="336a0-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="336a0-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="336a0-132">Header</span></span><br/> | <dl> <span data-ttu-id="336a0-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="336a0-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="336a0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="336a0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="336a0-135">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="336a0-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="336a0-136">**IDirect3D9::CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="336a0-136">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[<span data-ttu-id="336a0-137">**IDirect3D9::CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="336a0-137">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[<span data-ttu-id="336a0-138">**IDirect3D9::CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="336a0-138">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[<span data-ttu-id="336a0-139">**IDirect3D9::CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="336a0-139">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="336a0-140">**IDirect3D9::GetDeviceCaps**</span><span class="sxs-lookup"><span data-stu-id="336a0-140">**IDirect3D9::GetDeviceCaps**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[<span data-ttu-id="336a0-141">**\_Parámetros de creación de D3DDEVICE \_**</span><span class="sxs-lookup"><span data-stu-id="336a0-141">**D3DDEVICE\_CREATION\_PARAMETERS**</span></span>](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
