---
description: Objeto de procesamiento de datos utilizado por la interfaz ID3DX10ThreadPump para procesar datos cargados de forma asincrónica.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interfaz ID3DX10DataProcessor (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914830"
---
# <a name="id3dx10dataprocessor-interface"></a><span data-ttu-id="a6a94-103">Interfaz ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="a6a94-103">ID3DX10DataProcessor interface</span></span>

<span data-ttu-id="a6a94-104">Objeto de procesamiento de datos utilizado por la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para procesar datos cargados de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a6a94-104">Data processing object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for processing loaded data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="a6a94-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6a94-105">Members</span></span>

<span data-ttu-id="a6a94-106">La interfaz **ID3DX10DataProcessor** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a6a94-106">The **ID3DX10DataProcessor** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a6a94-107">**ID3DX10DataProcessor** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a6a94-107">**ID3DX10DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="a6a94-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6a94-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a6a94-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6a94-109">Methods</span></span>

<span data-ttu-id="a6a94-110">La interfaz **ID3DX10DataProcessor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a6a94-110">The **ID3DX10DataProcessor** interface has these methods.</span></span>



| <span data-ttu-id="a6a94-111">Método</span><span class="sxs-lookup"><span data-stu-id="a6a94-111">Method</span></span>                                                                | <span data-ttu-id="a6a94-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6a94-112">Description</span></span>                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6a94-113">**CreateDeviceObject**</span><span class="sxs-lookup"><span data-stu-id="a6a94-113">**CreateDeviceObject**</span></span>](id3dx10dataprocessor-createdeviceobject.md) | <span data-ttu-id="a6a94-114">Cree un objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6a94-114">Create a device object.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="a6a94-115">**Borrar**</span><span class="sxs-lookup"><span data-stu-id="a6a94-115">**Destroy**</span></span>](id3dx10dataprocessor-destroy.md)                       | <span data-ttu-id="a6a94-116">Lo usa una [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir el procesador después de que se complete un elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a6a94-116">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the processor after a work item completes.</span></span><br/> |
| [<span data-ttu-id="a6a94-117">**Proceso**</span><span class="sxs-lookup"><span data-stu-id="a6a94-117">**Process**</span></span>](id3dx10dataprocessor-process.md)                       | <span data-ttu-id="a6a94-118">Procesa algunos datos.</span><span class="sxs-lookup"><span data-stu-id="a6a94-118">Process some data.</span></span><br/>                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="a6a94-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6a94-119">Remarks</span></span>

<span data-ttu-id="a6a94-120">Este objeto se puede heredar y sus miembros se pueden redefinir.</span><span class="sxs-lookup"><span data-stu-id="a6a94-120">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="a6a94-121">Esto le permitirá personalizar la API para procesar sus propios formatos de archivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="a6a94-121">Doing so would enable you to customize the API for processing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a94-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6a94-122">Requirements</span></span>



| <span data-ttu-id="a6a94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a94-123">Requirement</span></span> | <span data-ttu-id="a6a94-124">Value</span><span class="sxs-lookup"><span data-stu-id="a6a94-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a94-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6a94-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a6a94-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a94-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6a94-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6a94-127">Library</span></span><br/> | <dl> <span data-ttu-id="a6a94-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6a94-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a94-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6a94-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a94-130">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="a6a94-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
