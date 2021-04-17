---
description: Quita todos los recursos del dispositivo estableciendo sus punteros en NULL. Se debe llamar a este método durante el cierre de la aplicación. Ayuda a garantizar que cuando se liberan todos los recursos que no están enlazados al dispositivo.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Función D3DX10UnsetAllDeviceObjects (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698268"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a><span data-ttu-id="0100e-105">D3DX10UnsetAllDeviceObjects función)</span><span class="sxs-lookup"><span data-stu-id="0100e-105">D3DX10UnsetAllDeviceObjects function</span></span>

<span data-ttu-id="0100e-106">Quita todos los recursos del dispositivo estableciendo sus punteros en **null**.</span><span class="sxs-lookup"><span data-stu-id="0100e-106">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="0100e-107">Se debe llamar a este método durante el cierre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0100e-107">This should be called during shutdown of your application.</span></span> <span data-ttu-id="0100e-108">Ayuda a garantizar que cuando se liberan todos los recursos que no están enlazados al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0100e-108">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0100e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0100e-109">Syntax</span></span>


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="0100e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0100e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0100e-111">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0100e-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0100e-112">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="0100e-112">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="0100e-113">Puntero al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0100e-113">Pointer to the device.</span></span> <span data-ttu-id="0100e-114">Consulte la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span><span class="sxs-lookup"><span data-stu-id="0100e-114">See [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0100e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0100e-115">Return value</span></span>

<span data-ttu-id="0100e-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0100e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0100e-117">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0100e-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0100e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0100e-118">Requirements</span></span>



| <span data-ttu-id="0100e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0100e-119">Requirement</span></span> | <span data-ttu-id="0100e-120">Value</span><span class="sxs-lookup"><span data-stu-id="0100e-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0100e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0100e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0100e-122"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0100e-122"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="0100e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0100e-123">Library</span></span><br/> | <dl> <span data-ttu-id="0100e-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0100e-124"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0100e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0100e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0100e-126">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="0100e-126">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




