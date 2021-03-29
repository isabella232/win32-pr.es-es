---
description: Dibuja varias instancias del mismo subconjunto de una malla.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh::D método rawSubsetInstanced (D3DX10. h)
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
ms.openlocfilehash: 314f85d896be629254def560e55ce6a05bfe1fbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678834"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="efc89-103">ID3DX10Mesh::D método rawSubsetInstanced</span><span class="sxs-lookup"><span data-stu-id="efc89-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="efc89-104">Dibuja varias instancias del mismo subconjunto de una malla.</span><span class="sxs-lookup"><span data-stu-id="efc89-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efc89-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="efc89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efc89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc89-107">*AttribId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efc89-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc89-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efc89-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efc89-109">Especifica el subconjunto de la malla que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="efc89-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="efc89-110">Este valor se usa para diferenciar caras en una malla como perteneciente a uno o varios grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="efc89-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="efc89-111">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="efc89-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="efc89-112">*InstanceCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efc89-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc89-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efc89-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efc89-114">Número de instancias que se van a representar.</span><span class="sxs-lookup"><span data-stu-id="efc89-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="efc89-115">*StartInstanceLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="efc89-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc89-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efc89-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efc89-117">La instancia de en la que se va a iniciar la captura en cada búfer marcado como datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="efc89-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc89-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efc89-118">Return value</span></span>

<span data-ttu-id="efc89-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efc89-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efc89-120">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="efc89-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="efc89-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efc89-121">Remarks</span></span>

<span data-ttu-id="efc89-122">Una malla contiene una tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="efc89-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="efc89-123">La tabla de atributos puede dividir una malla en subconjuntos, donde cada subconjunto se identifica con un identificador de atributo.</span><span class="sxs-lookup"><span data-stu-id="efc89-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="efc89-124">Por ejemplo, una malla con 200 caras, dividida en tres subconjuntos, podría tener una tabla de atributos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="efc89-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



|            |                 |
|------------|-----------------|
| <span data-ttu-id="efc89-125">AttribID 0</span><span class="sxs-lookup"><span data-stu-id="efc89-125">AttribID 0</span></span> | <span data-ttu-id="efc89-126">Caras 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="efc89-126">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="efc89-127">AttribID 1</span><span class="sxs-lookup"><span data-stu-id="efc89-127">AttribID 1</span></span> | <span data-ttu-id="efc89-128">Caras 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="efc89-128">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="efc89-129">AttribID 2</span><span class="sxs-lookup"><span data-stu-id="efc89-129">AttribID 2</span></span> | <span data-ttu-id="efc89-130">Caras 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="efc89-130">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="efc89-131">La creación de instancias puede ampliar el rendimiento mediante la reutilización de la misma geometría para dibujar varios objetos en una escena.</span><span class="sxs-lookup"><span data-stu-id="efc89-131">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="efc89-132">Un ejemplo de creación de instancias podría ser dibujar el mismo objeto con diferentes posiciones y colores.</span><span class="sxs-lookup"><span data-stu-id="efc89-132">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="efc89-133">La indexación requiere varios búferes de vértices: al menos uno para los datos por vértice y un segundo búfer para los datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="efc89-133">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="efc89-134">Dibujar instancias con DrawSubsetInstanced es muy similar al proceso utilizado con [**ID3D10Device::D rawindexedinstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) que se describe en el ejemplo de [creación de instancias](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="efc89-134">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="efc89-135">La diferencia clave al usar DrawSubsetInstanced es que los búferes de vértices y de índices deben extraerse del objeto de [**interfaz ID3DX10Mesh**](id3dx10mesh.md) antes de que se puedan combinar los datos de la instancia.</span><span class="sxs-lookup"><span data-stu-id="efc89-135">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="efc89-136">En el código siguiente se muestra cómo extraer los búferes de vértices y de índices del objeto de malla.</span><span class="sxs-lookup"><span data-stu-id="efc89-136">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="efc89-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efc89-137">Requirements</span></span>



| <span data-ttu-id="efc89-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc89-138">Requirement</span></span> | <span data-ttu-id="efc89-139">Value</span><span class="sxs-lookup"><span data-stu-id="efc89-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efc89-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efc89-140">Header</span></span><br/>  | <dl> <span data-ttu-id="efc89-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="efc89-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="efc89-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efc89-142">Library</span></span><br/> | <dl> <span data-ttu-id="efc89-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efc89-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc89-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="efc89-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc89-145">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="efc89-145">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="efc89-146">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="efc89-146">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
