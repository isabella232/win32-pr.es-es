---
description: Dibuje varias instancias del mismo subconjunto de una malla.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: Método ID3DX10Mesh::D rawSubsetInstanced (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2e28d7a7d2c1d743090832d68793ec3743662308
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335639"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="56cb7-103">Método ID3DX10Mesh::D rawSubsetInstanced</span><span class="sxs-lookup"><span data-stu-id="56cb7-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="56cb7-104">Dibuje varias instancias del mismo subconjunto de una malla.</span><span class="sxs-lookup"><span data-stu-id="56cb7-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="56cb7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56cb7-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="56cb7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56cb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56cb7-107">*AttribId* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="56cb7-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56cb7-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56cb7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56cb7-109">Especifica qué subconjunto de la malla se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="56cb7-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="56cb7-110">Este valor se usa para diferenciar las caras de una malla como pertenecientes a uno o varios grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="56cb7-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="56cb7-111">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="56cb7-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="56cb7-112">*InstanceCount* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="56cb7-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56cb7-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56cb7-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56cb7-114">Número de instancias que se representará.</span><span class="sxs-lookup"><span data-stu-id="56cb7-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="56cb7-115">*StartInstanceLocation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="56cb7-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56cb7-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56cb7-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56cb7-117">Instancia de la que se va a empezar a capturar en cada búfer marcado como datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="56cb7-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56cb7-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56cb7-118">Return value</span></span>

<span data-ttu-id="56cb7-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56cb7-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56cb7-120">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="56cb7-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56cb7-121">Remarks</span></span>

<span data-ttu-id="56cb7-122">Una malla contiene una tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="56cb7-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="56cb7-123">La tabla de atributos puede dividir una malla en subconjuntos, donde cada subconjunto se identifica con un identificador de atributo.</span><span class="sxs-lookup"><span data-stu-id="56cb7-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="56cb7-124">Por ejemplo, una malla con 200 caras, dividida en tres subconjuntos, podría tener una tabla de atributos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="56cb7-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



| <span data-ttu-id="56cb7-125">Subset</span><span class="sxs-lookup"><span data-stu-id="56cb7-125">Subset</span></span>     | <span data-ttu-id="56cb7-126">Caras</span><span class="sxs-lookup"><span data-stu-id="56cb7-126">Faces</span></span>           |
|------------|-----------------|
| <span data-ttu-id="56cb7-127">AttribID 0</span><span class="sxs-lookup"><span data-stu-id="56cb7-127">AttribID 0</span></span> | <span data-ttu-id="56cb7-128">Caras 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="56cb7-128">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="56cb7-129">AttribID 1</span><span class="sxs-lookup"><span data-stu-id="56cb7-129">AttribID 1</span></span> | <span data-ttu-id="56cb7-130">Caras 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="56cb7-130">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="56cb7-131">AttribID 2</span><span class="sxs-lookup"><span data-stu-id="56cb7-131">AttribID 2</span></span> | <span data-ttu-id="56cb7-132">Caras 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="56cb7-132">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="56cb7-133">La creación de instancias puede ampliar el rendimiento si se vuelve a usar la misma geometría para dibujar varios objetos en una escena.</span><span class="sxs-lookup"><span data-stu-id="56cb7-133">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="56cb7-134">Un ejemplo de creación de instancias podría ser dibujar el mismo objeto con diferentes posiciones y colores.</span><span class="sxs-lookup"><span data-stu-id="56cb7-134">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="56cb7-135">La indexación requiere varios búferes de vértices: al menos uno para los datos por vértice y un segundo búfer para los datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="56cb7-135">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="56cb7-136">El dibujo de instancias con DrawSubsetInstanced es muy similar al proceso usado con [**ID3D10Device::D rawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) que se describe en Ejemplo de creación de instancias [.](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="56cb7-136">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="56cb7-137">La diferencia clave al usar DrawSubsetInstanced es que los búferes de vértice e índice deben extraerse del objeto [**ID3DX10Mesh Interface**](id3dx10mesh.md) para poder combinar los datos de creación de instancias.</span><span class="sxs-lookup"><span data-stu-id="56cb7-137">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="56cb7-138">En el código siguiente se muestra cómo extraer los búferes de vértice e índice del objeto de malla.</span><span class="sxs-lookup"><span data-stu-id="56cb7-138">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="56cb7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56cb7-139">Requirements</span></span>



| <span data-ttu-id="56cb7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="56cb7-140">Requirement</span></span> | <span data-ttu-id="56cb7-141">Value</span><span class="sxs-lookup"><span data-stu-id="56cb7-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56cb7-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56cb7-142">Header</span></span><br/>  | <dl> <span data-ttu-id="56cb7-143"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="56cb7-143"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="56cb7-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56cb7-144">Library</span></span><br/> | <dl> <span data-ttu-id="56cb7-145"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="56cb7-145"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56cb7-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="56cb7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56cb7-147">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="56cb7-147">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="56cb7-148">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="56cb7-148">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
