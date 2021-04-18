---
description: Consulta la cantidad de memoria temporal que la capa de abstracción de hardware (HAL) asignará para su uso privado.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'IDirect3DVideoDevice9:: GetDXVAInternalInfo (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715439"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a><span data-ttu-id="d3a0d-103">IDirect3DVideoDevice9:: GetDXVAInternalInfo (método)</span><span class="sxs-lookup"><span data-stu-id="d3a0d-103">IDirect3DVideoDevice9::GetDXVAInternalInfo method</span></span>

<span data-ttu-id="d3a0d-104">Consulta la cantidad de memoria temporal que la capa de abstracción de hardware (HAL) asignará para su uso privado.</span><span class="sxs-lookup"><span data-stu-id="d3a0d-104">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a0d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3a0d-105">Syntax</span></span>


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a><span data-ttu-id="d3a0d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3a0d-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="d3a0d-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a0d-108">Puntero a un GUID que especifica el perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="d3a0d-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="d3a0d-109">Para obtener una lista de los perfiles compatibles, llame a [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="d3a0d-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3a0d-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="d3a0d-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a0d-111">Puntero a una estructura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica el tamaño y el formato de píxel de los datos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="d3a0d-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="d3a0d-112">*pMemoryUsed*</span><span class="sxs-lookup"><span data-stu-id="d3a0d-112">*pMemoryUsed*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a0d-113">Recibe la cantidad de memoria temporal que asignará la HAL, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d3a0d-113">Receives the amount of scratch memory that the HAL will allocate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3a0d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3a0d-114">Return value</span></span>

<span data-ttu-id="d3a0d-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d3a0d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3a0d-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3a0d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a0d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3a0d-117">Requirements</span></span>



| <span data-ttu-id="d3a0d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3a0d-118">Requirement</span></span> | <span data-ttu-id="d3a0d-119">Value</span><span class="sxs-lookup"><span data-stu-id="d3a0d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d3a0d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3a0d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a0d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d3a0d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d3a0d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3a0d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a0d-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3a0d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d3a0d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3a0d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3a0d-125"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3a0d-125"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3a0d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3a0d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a0d-127">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="d3a0d-127">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




