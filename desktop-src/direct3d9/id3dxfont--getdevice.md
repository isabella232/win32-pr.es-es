---
description: Recupera el dispositivo Direct3D asociado al objeto Font.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: 'ID3DXFont:: GetDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2de1b6e2c3b2c2b61576c739d96abc8b8fc8851a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362770"
---
# <a name="id3dxfontgetdevice-method"></a><span data-ttu-id="8c90b-103">ID3DXFont:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="8c90b-103">ID3DXFont::GetDevice method</span></span>

<span data-ttu-id="8c90b-104">Recupera el dispositivo Direct3D asociado al objeto Font.</span><span class="sxs-lookup"><span data-stu-id="8c90b-104">Retrieves the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c90b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c90b-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="8c90b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c90b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c90b-107">*ppDevice* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c90b-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c90b-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="8c90b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="8c90b-109">Dirección de un puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo de Direct3D asociado al objeto de fuente.</span><span class="sxs-lookup"><span data-stu-id="8c90b-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c90b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c90b-110">Return value</span></span>

<span data-ttu-id="8c90b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c90b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c90b-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c90b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8c90b-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8c90b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c90b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c90b-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c90b-115">Al llamar a este método, se aumentará el recuento de referencias interno en la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="8c90b-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="8c90b-116">Asegúrese de llamar a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) cuando haya terminado de usar esta interfaz **IDirect3DDevice9** o se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="8c90b-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c90b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c90b-117">Requirements</span></span>



| <span data-ttu-id="8c90b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c90b-118">Requirement</span></span> | <span data-ttu-id="8c90b-119">Value</span><span class="sxs-lookup"><span data-stu-id="8c90b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c90b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c90b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8c90b-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c90b-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8c90b-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c90b-122">Library</span></span><br/> | <dl> <span data-ttu-id="8c90b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c90b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c90b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c90b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c90b-125">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="8c90b-125">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
