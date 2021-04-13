---
description: Describe los parámetros de creación de un dispositivo.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: D3DDEVICE_CREATION_PARAMETERS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362494"
---
# <a name="d3ddevice_creation_parameters-structure"></a><span data-ttu-id="d7ed6-103">\_Estructura de \_ los parámetros de creación de D3DDEVICE</span><span class="sxs-lookup"><span data-stu-id="d7ed6-103">D3DDEVICE\_CREATION\_PARAMETERS structure</span></span>

<span data-ttu-id="d7ed6-104">Describe los parámetros de creación de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-104">Describes the creation parameters for a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ed6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7ed6-105">Syntax</span></span>


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="d7ed6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7ed6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7ed6-107">**AdapterOrdinal**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-107">**AdapterOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="d7ed6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7ed6-109">Número ordinal que denota el adaptador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-109">Ordinal number that denotes the display adapter.</span></span> <span data-ttu-id="d7ed6-110">D3DADAPTER \_ default siempre es el adaptador de pantalla principal.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-110">D3DADAPTER\_DEFAULT is always the primary display adapter.</span></span> <span data-ttu-id="d7ed6-111">Use este ordinal como parámetro del adaptador para cualquiera de los métodos [**IDirect3D9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="d7ed6-111">Use this ordinal as the Adapter parameter for any of the [**IDirect3D9**](/windows/desktop/api) methods.</span></span> <span data-ttu-id="d7ed6-112">Tenga en cuenta que las diferentes instancias de objetos de Direct3D 9,0 pueden utilizar distintos ordinales.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-112">Note that different instances of Direct3D 9.0 objects can use different ordinals.</span></span> <span data-ttu-id="d7ed6-113">Los adaptadores pueden escribir o dejar un sistema cuando los usuarios, por ejemplo, agregan o quitan monitores de un sistema de varios monitores o cuando intercambian a un portátil.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-113">Adapters can enter or leave a system when users, for example, add or remove monitors from a multiple-monitor system or when they hot-swap a laptop.</span></span> <span data-ttu-id="d7ed6-114">Por lo tanto, use este ordinal solo en una instancia de Direct3D 9,0 conocida como válida, es decir, el Direct3D 9,0 que creó esta interfaz [**IDirect3DDevice9**](/windows/desktop/api) o el Direct3D 9,0 devuelto desde [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), como se llama a través de esta interfaz **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="d7ed6-114">Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this [**IDirect3DDevice9**](/windows/desktop/api) interface or the Direct3D 9.0 returned from [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), as called through this **IDirect3DDevice9** interface.</span></span>

</dd> <dt>

<span data-ttu-id="d7ed6-115">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-115">**DeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="d7ed6-116">Tipo: **[ **D3DDEVTYPE**](./d3ddevtype.md)**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-116">Type: **[**D3DDEVTYPE**](./d3ddevtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7ed6-117">Miembro del tipo enumerado [**D3DDEVTYPE**](./d3ddevtype.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ed6-117">Member of the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type.</span></span> <span data-ttu-id="d7ed6-118">Denota la cantidad de funcionalidad emulada para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-118">Denotes the amount of emulated functionality for this device.</span></span> <span data-ttu-id="d7ed6-119">El valor de este parámetro refleja el valor pasado a la llamada a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) que creó este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-119">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="d7ed6-120">**hFocusWindow**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-120">**hFocusWindow**</span></span>
</dt> <dd>

<span data-ttu-id="d7ed6-121">Tipo: **[ **hWnd**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-121">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7ed6-122">Identificador de ventana al que pertenece el foco para este dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-122">Window handle to which focus belongs for this Direct3D device.</span></span> <span data-ttu-id="d7ed6-123">El valor de este parámetro refleja el valor pasado a la llamada a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) que creó este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-123">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="d7ed6-124">**BehaviorFlags**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-124">**BehaviorFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d7ed6-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7ed6-126">Combinación de una o varias constantes de [D3DCREATE](d3dcreate.md) que controlan el comportamiento global del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-126">A combination of one or more [D3DCREATE](d3dcreate.md) constants that control global behavior of the device.</span></span> <span data-ttu-id="d7ed6-127">Estas constantes reflejan las constantes pasadas a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) cuando se creó el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ed6-127">These constants mirror the constants passed to [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) when the device was created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7ed6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7ed6-128">Requirements</span></span>



| <span data-ttu-id="d7ed6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7ed6-129">Requirement</span></span> | <span data-ttu-id="d7ed6-130">Value</span><span class="sxs-lookup"><span data-stu-id="d7ed6-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ed6-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7ed6-131">Header</span></span><br/> | <dl> <span data-ttu-id="d7ed6-132"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ed6-132"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ed6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7ed6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ed6-134">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d7ed6-134">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d7ed6-135">**GetCreationParameters**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-135">**GetCreationParameters**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[<span data-ttu-id="d7ed6-136">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="d7ed6-136">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
