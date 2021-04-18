---
description: Recupera el dispositivo asociado al efecto.
ms.assetid: acef5d0a-b185-4054-8982-0580440ab76b
title: 'ID3DXEffect:: GetDevice (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fde2d9f3d9db362bf48fda66e9da10b91a864bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718566"
---
# <a name="id3dxeffectgetdevice-method"></a><span data-ttu-id="8464f-103">ID3DXEffect:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="8464f-103">ID3DXEffect::GetDevice method</span></span>

<span data-ttu-id="8464f-104">Recupera el dispositivo asociado al efecto.</span><span class="sxs-lookup"><span data-stu-id="8464f-104">Retrieves the device associated with the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="8464f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8464f-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="8464f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8464f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8464f-107">*ppDevice* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8464f-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8464f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="8464f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="8464f-109">Dirección de un puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado al efecto.</span><span class="sxs-lookup"><span data-stu-id="8464f-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8464f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8464f-110">Return value</span></span>

<span data-ttu-id="8464f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8464f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8464f-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8464f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8464f-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8464f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8464f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8464f-114">Remarks</span></span>

<span data-ttu-id="8464f-115">Al llamar a este método, se aumentará el recuento de referencias interno de la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="8464f-115">Calling this method will increase the internal reference count for the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="8464f-116">Asegúrese de llamar a IUnknown:: Release cuando haya terminado de usar la interfaz **IDirect3DDevice9** o se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="8464f-116">Be sure to call IUnknown::Release when you are done using the **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="8464f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8464f-117">Requirements</span></span>



| <span data-ttu-id="8464f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8464f-118">Requirement</span></span> | <span data-ttu-id="8464f-119">Value</span><span class="sxs-lookup"><span data-stu-id="8464f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8464f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8464f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8464f-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8464f-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8464f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8464f-122">Library</span></span><br/> | <dl> <span data-ttu-id="8464f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8464f-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8464f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8464f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8464f-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8464f-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
