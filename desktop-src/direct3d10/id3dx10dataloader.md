---
description: Objeto de carga de datos utilizado por la interfaz ID3DX10ThreadPump para cargar datos de forma asincrónica.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interfaz ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003830"
---
# <a name="id3dx10dataloader-interface"></a><span data-ttu-id="af154-103">Interfaz ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="af154-103">ID3DX10DataLoader interface</span></span>

<span data-ttu-id="af154-104">Objeto de carga de datos utilizado por la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para cargar datos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="af154-104">Data loading object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="af154-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="af154-105">Members</span></span>

<span data-ttu-id="af154-106">La interfaz **ID3DX10DataLoader** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="af154-106">The **ID3DX10DataLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="af154-107">**ID3DX10DataLoader** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="af154-107">**ID3DX10DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="af154-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="af154-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="af154-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="af154-109">Methods</span></span>

<span data-ttu-id="af154-110">La interfaz **ID3DX10DataLoader** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="af154-110">The **ID3DX10DataLoader** interface has these methods.</span></span>



| <span data-ttu-id="af154-111">Método</span><span class="sxs-lookup"><span data-stu-id="af154-111">Method</span></span>                                             | <span data-ttu-id="af154-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="af154-112">Description</span></span>                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af154-113">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="af154-113">**Decompress**</span></span>](id3dx10dataloader-decompress.md) | <span data-ttu-id="af154-114">Se usa para descomprimir datos codificados.</span><span class="sxs-lookup"><span data-stu-id="af154-114">Used to decompress encoded data.</span></span> <span data-ttu-id="af154-115">Normalmente, esto se utilizaría para cargar recursos desde sistemas de archivos, como archivos ZIP.</span><span class="sxs-lookup"><span data-stu-id="af154-115">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="af154-116">Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="af154-116">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span><br/> |
| [<span data-ttu-id="af154-117">**Borrar**</span><span class="sxs-lookup"><span data-stu-id="af154-117">**Destroy**</span></span>](id3dx10dataloader-destroy.md)       | <span data-ttu-id="af154-118">Lo usa una [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir el cargador una vez completado un elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="af154-118">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the loader after a work item completes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="af154-119">**Cargar**</span><span class="sxs-lookup"><span data-stu-id="af154-119">**Load**</span></span>](id3dx10dataloader-load.md)             | <span data-ttu-id="af154-120">Lo usa una [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para cargar datos de un disco.</span><span class="sxs-lookup"><span data-stu-id="af154-120">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to load data from a disk.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="af154-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af154-121">Remarks</span></span>

<span data-ttu-id="af154-122">Este objeto se puede heredar y sus miembros se pueden redefinir.</span><span class="sxs-lookup"><span data-stu-id="af154-122">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="af154-123">Esto le permitirá personalizar la API para cargar y descomprimir sus propios formatos de archivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="af154-123">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="af154-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af154-124">Requirements</span></span>



| <span data-ttu-id="af154-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="af154-125">Requirement</span></span> | <span data-ttu-id="af154-126">Value</span><span class="sxs-lookup"><span data-stu-id="af154-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af154-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af154-127">Header</span></span><br/>  | <dl> <span data-ttu-id="af154-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="af154-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="af154-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af154-129">Library</span></span><br/> | <dl> <span data-ttu-id="af154-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af154-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af154-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="af154-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af154-132">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="af154-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
