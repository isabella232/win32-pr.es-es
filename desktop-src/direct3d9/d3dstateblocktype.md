---
description: Conjuntos predefinidos de estado de canalización usados por bloques de estado (vea bloques de estado guardar y restaurar estado (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Enumeración D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104552932"
---
# <a name="d3dstateblocktype-enumeration"></a><span data-ttu-id="2f9e0-103">Enumeración D3DSTATEBLOCKTYPE</span><span class="sxs-lookup"><span data-stu-id="2f9e0-103">D3DSTATEBLOCKTYPE enumeration</span></span>

<span data-ttu-id="2f9e0-104">Conjuntos predefinidos de estado de canalización usados por bloques de estado (vea [bloques de estado guardar y restaurar estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="2f9e0-104">Predefined sets of pipeline state used by state blocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f9e0-105">Syntax</span></span>


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a><span data-ttu-id="2f9e0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2f9e0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2f9e0-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ todo**</span><span class="sxs-lookup"><span data-stu-id="2f9e0-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="2f9e0-108">Capture el estado actual del [dispositivo](saving-all-device-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="2f9e0-108">Capture the current [device state](saving-all-device-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f9e0-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**</span><span class="sxs-lookup"><span data-stu-id="2f9e0-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT\_PIXELSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="2f9e0-110">Capturar el estado actual de los [píxeles](saving-pixel-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="2f9e0-110">Capture the current [pixel state](saving-pixel-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f9e0-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**</span><span class="sxs-lookup"><span data-stu-id="2f9e0-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT\_VERTEXSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="2f9e0-112">Capturar el estado actual del [vértice](saving-vertex-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="2f9e0-112">Capture the current [vertex state](saving-vertex-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f9e0-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2f9e0-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2f9e0-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2f9e0-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2f9e0-116">No utilice este valor.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-116">Do not use this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f9e0-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f9e0-117">Remarks</span></span>

<span data-ttu-id="2f9e0-118">Como se muestra en el diagrama siguiente, el estado de los vértices y los píxeles son ambos subconjuntos del estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-118">As the following diagram shows, vertex and pixel state are both subsets of device state.</span></span>

![diagrama del estado del dispositivo, con estado de vértice y estado de píxel como subconjuntos](images/statesets.png)

<span data-ttu-id="2f9e0-120">Solo hay algunos Estados que se consideran el estado de vértices y de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-120">There are only a few states that are considered both vertex and pixel state.</span></span> <span data-ttu-id="2f9e0-121">Estos estados son:</span><span class="sxs-lookup"><span data-stu-id="2f9e0-121">These states are:</span></span>

-   <span data-ttu-id="2f9e0-122">Estado de representación: D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="2f9e0-122">Render state: D3DRS\_FOGDENSITY</span></span>
-   <span data-ttu-id="2f9e0-123">Estado de representación: D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="2f9e0-123">Render state: D3DRS\_FOGSTART</span></span>
-   <span data-ttu-id="2f9e0-124">Estado de representación: D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="2f9e0-124">Render state: D3DRS\_FOGEND</span></span>
-   <span data-ttu-id="2f9e0-125">Estado de textura: D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="2f9e0-125">Texture state: D3DTSS\_TEXCOORDINDEX</span></span>
-   <span data-ttu-id="2f9e0-126">Estado de textura: D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="2f9e0-126">Texture state: D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>

## <a name="requirements"></a><span data-ttu-id="2f9e0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f9e0-127">Requirements</span></span>



| <span data-ttu-id="2f9e0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f9e0-128">Requirement</span></span> | <span data-ttu-id="2f9e0-129">Value</span><span class="sxs-lookup"><span data-stu-id="2f9e0-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9e0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f9e0-130">Header</span></span><br/> | <dl> <span data-ttu-id="2f9e0-131"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e0-131"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f9e0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f9e0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f9e0-133">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2f9e0-133">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="2f9e0-134">**IDirect3DDevice9::CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="2f9e0-134">**IDirect3DDevice9::CreateStateBlock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

<span data-ttu-id="2f9e0-135">**IDirect3DDevice9::CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="2f9e0-135">**IDirect3DDevice9::CreateStateBlock**</span></span>
</dt> </dl>

 

 
