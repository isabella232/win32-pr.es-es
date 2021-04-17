---
description: La interfaz ID3DXBuffer se usa como un búfer de datos, que almacena información de vértices, de adyacencias y de material durante las operaciones de carga y optimización de malla.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interfaz ID3DXBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678803"
---
# <a name="id3dxbuffer-interface"></a><span data-ttu-id="1f1dd-103">Interfaz ID3DXBuffer</span><span class="sxs-lookup"><span data-stu-id="1f1dd-103">ID3DXBuffer interface</span></span>

<span data-ttu-id="1f1dd-104">La interfaz ID3DXBuffer se usa como un búfer de datos, que almacena información de vértices, de adyacencias y de material durante las operaciones de carga y optimización de malla.</span><span class="sxs-lookup"><span data-stu-id="1f1dd-104">The ID3DXBuffer interface is used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.</span></span> <span data-ttu-id="1f1dd-105">El objeto de búfer se usa para devolver datos de longitud arbitraria.</span><span class="sxs-lookup"><span data-stu-id="1f1dd-105">The buffer object is used to return arbitrary length data.</span></span> <span data-ttu-id="1f1dd-106">Además, los objetos de búfer se usan para devolver código objeto y mensajes de error en métodos que ensamblan sombreadores de píxeles y vértices.</span><span class="sxs-lookup"><span data-stu-id="1f1dd-106">Also, buffer objects are used to return object code and error messages in methods that assemble vertex and pixel shaders.</span></span>

## <a name="members"></a><span data-ttu-id="1f1dd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1f1dd-107">Members</span></span>

<span data-ttu-id="1f1dd-108">La interfaz **ID3DXBuffer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1f1dd-108">The **ID3DXBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1f1dd-109">**ID3DXBuffer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1f1dd-109">**ID3DXBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="1f1dd-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f1dd-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1f1dd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f1dd-111">Methods</span></span>

<span data-ttu-id="1f1dd-112">La interfaz **ID3DXBuffer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1f1dd-112">The **ID3DXBuffer** interface has these methods.</span></span>



| <span data-ttu-id="1f1dd-113">Método</span><span class="sxs-lookup"><span data-stu-id="1f1dd-113">Method</span></span>                                                    | <span data-ttu-id="1f1dd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f1dd-114">Description</span></span>                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="1f1dd-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="1f1dd-115">**GetBufferPointer**</span></span>](id3dxbuffer--getbufferpointer.md) | <span data-ttu-id="1f1dd-116">Recupera un puntero a los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="1f1dd-116">Retrieves a pointer to the data in the buffer.</span></span><br/>      |
| [<span data-ttu-id="1f1dd-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="1f1dd-117">**GetBufferSize**</span></span>](id3dxbuffer--getbuffersize.md)       | <span data-ttu-id="1f1dd-118">Recupera el tamaño total de los datos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="1f1dd-118">Retrieves the total size of the data in the buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f1dd-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f1dd-119">Remarks</span></span>

<span data-ttu-id="1f1dd-120">La interfaz **ID3DXBuffer** se obtiene mediante una llamada a la función [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1f1dd-120">The **ID3DXBuffer** interface is obtained by calling the [**D3DXCreateBuffer**](d3dxcreatebuffer.md) function.</span></span>

<span data-ttu-id="1f1dd-121">El tipo LPD3DXBUFFER se define como un puntero a la interfaz **ID3DXBuffer** .</span><span class="sxs-lookup"><span data-stu-id="1f1dd-121">The LPD3DXBUFFER type is defined as a pointer to the **ID3DXBuffer** interface.</span></span>


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="1f1dd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f1dd-122">Requirements</span></span>



| <span data-ttu-id="1f1dd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f1dd-123">Requirement</span></span> | <span data-ttu-id="1f1dd-124">Value</span><span class="sxs-lookup"><span data-stu-id="1f1dd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1dd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f1dd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1f1dd-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f1dd-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1f1dd-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f1dd-127">Library</span></span><br/> | <dl> <span data-ttu-id="1f1dd-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f1dd-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1f1dd-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f1dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1dd-130">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="1f1dd-130">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
