---
description: Recupera el dispositivo Direct3D asociado a la asignación de entorno.
ms.assetid: 15f342c5-7665-443a-b7b8-32cc67034c41
title: 'ID3DXRenderToEnvMap:: GetDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b5adc045beeefa220a849a6da752a8d3efc82ff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707811"
---
# <a name="id3dxrendertoenvmapgetdevice-method"></a><span data-ttu-id="eadd5-103">ID3DXRenderToEnvMap:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="eadd5-103">ID3DXRenderToEnvMap::GetDevice method</span></span>

<span data-ttu-id="eadd5-104">Recupera el dispositivo Direct3D asociado a la asignación de entorno.</span><span class="sxs-lookup"><span data-stu-id="eadd5-104">Retrieves the Direct3D device associated with the environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="eadd5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eadd5-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="eadd5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eadd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eadd5-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="eadd5-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="eadd5-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="eadd5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="eadd5-109">Dirección de un puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo Direct3D asociado a la asignación de entorno.</span><span class="sxs-lookup"><span data-stu-id="eadd5-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface that represents the Direct3D device object associated with the environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eadd5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eadd5-110">Return value</span></span>

<span data-ttu-id="eadd5-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eadd5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eadd5-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eadd5-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eadd5-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="eadd5-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="eadd5-114">La llamada a este método aumenta el recuento de referencias internas en la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="eadd5-114">Calling this method increases the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="eadd5-115">Asegúrese de llamar a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) cuando haya terminado de usar esta interfaz **IDirect3DDevice9** o se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="eadd5-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="eadd5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eadd5-116">Requirements</span></span>



| <span data-ttu-id="eadd5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eadd5-117">Requirement</span></span> | <span data-ttu-id="eadd5-118">Value</span><span class="sxs-lookup"><span data-stu-id="eadd5-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eadd5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eadd5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="eadd5-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="eadd5-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="eadd5-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eadd5-121">Library</span></span><br/> | <dl> <span data-ttu-id="eadd5-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eadd5-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eadd5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="eadd5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadd5-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="eadd5-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
