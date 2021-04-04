---
description: Confirme los cambios realizados en una malla en el dispositivo para que los cambios se puedan representar. Se debe llamar a este método después de que se modifiquen los datos de una malla y antes de que se representen. No se puede representar una malla a menos que se confirme en el dispositivo. Vea Notas.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'ID3DX10Mesh:: CommitToDevice (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083734"
---
# <a name="id3dx10meshcommittodevice-method"></a><span data-ttu-id="fe0d6-106">ID3DX10Mesh:: CommitToDevice (método)</span><span class="sxs-lookup"><span data-stu-id="fe0d6-106">ID3DX10Mesh::CommitToDevice method</span></span>

<span data-ttu-id="fe0d6-107">Confirme los cambios realizados en una malla en el dispositivo para que los cambios se puedan representar.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-107">Commit any changes made to a mesh to the device so that the changes can be rendered.</span></span> <span data-ttu-id="fe0d6-108">Se debe llamar a este método después de que se modifiquen los datos de una malla y antes de que se representen.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-108">This should be called after a mesh's data is altered and before it is rendered.</span></span> <span data-ttu-id="fe0d6-109">No se puede representar una malla a menos que se confirme en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-109">A mesh cannot be rendered unless it is committed to the device.</span></span> <span data-ttu-id="fe0d6-110">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-110">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0d6-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe0d6-111">Syntax</span></span>


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a><span data-ttu-id="fe0d6-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe0d6-112">Parameters</span></span>

<span data-ttu-id="fe0d6-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe0d6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe0d6-114">Return value</span></span>

<span data-ttu-id="fe0d6-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe0d6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe0d6-116">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fe0d6-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe0d6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe0d6-117">Remarks</span></span>

<span data-ttu-id="fe0d6-118">Cuando se carga una malla, se cargan los datos en los recursos de almacenamiento provisional, lo que significa que los datos se pueden modificar pero no se representan.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-118">When a mesh is loaded, it's data is loaded into staging resources, meaning the data can be altered but not rendered.</span></span> <span data-ttu-id="fe0d6-119">Cuando se llama a CommitToDevice, los datos de los recursos de almacenamiento provisional se copian en recursos de dispositivo para que se puedan representar.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-119">When CommitToDevice is called, the data from the staging resources are copied into device resources so that they can be rendered.</span></span> <span data-ttu-id="fe0d6-120">Aunque los datos se confirman en el dispositivo, los recursos de almacenamiento provisional permanecen y se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-120">Although the data is committed to the device, the staging resources remain and can be modified.</span></span> <span data-ttu-id="fe0d6-121">Si se realizan modificaciones en los recursos de almacenamiento provisional, los recursos de almacenamiento provisional deben volver a confirmarse en el dispositivo para que esos cambios se representen en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fe0d6-121">If any modifications are made to the staging resources, the staging resources must be committed to the device again in order for those changes to be rendered on screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0d6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe0d6-122">Requirements</span></span>



| <span data-ttu-id="fe0d6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe0d6-123">Requirement</span></span> | <span data-ttu-id="fe0d6-124">Value</span><span class="sxs-lookup"><span data-stu-id="fe0d6-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0d6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe0d6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fe0d6-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe0d6-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe0d6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe0d6-127">Library</span></span><br/> | <dl> <span data-ttu-id="fe0d6-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe0d6-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0d6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe0d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0d6-130">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="fe0d6-130">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="fe0d6-131">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="fe0d6-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




