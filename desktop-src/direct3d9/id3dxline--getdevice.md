---
description: Recupera el dispositivo Direct3D asociado al objeto de línea.
ms.assetid: 42459668-aa18-478d-82d9-b8b25dc4a898
title: 'ID3DXLine:: GetDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a97edf37d14edce4982d62d76f9429091ad491ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698445"
---
# <a name="id3dxlinegetdevice-method"></a><span data-ttu-id="d3430-103">ID3DXLine:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="d3430-103">ID3DXLine::GetDevice method</span></span>

<span data-ttu-id="d3430-104">Recupera el dispositivo Direct3D asociado al objeto de línea.</span><span class="sxs-lookup"><span data-stu-id="d3430-104">Retrieves the Direct3D device associated with the line object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3430-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3430-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d3430-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3430-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3430-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d3430-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d3430-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="d3430-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="d3430-109">Dirección de un puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo de Direct3D asociado al objeto de línea.</span><span class="sxs-lookup"><span data-stu-id="d3430-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the line object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3430-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3430-110">Return value</span></span>

<span data-ttu-id="d3430-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3430-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3430-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3430-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d3430-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="d3430-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3430-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3430-114">Requirements</span></span>



| <span data-ttu-id="d3430-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3430-115">Requirement</span></span> | <span data-ttu-id="d3430-116">Value</span><span class="sxs-lookup"><span data-stu-id="d3430-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3430-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3430-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d3430-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3430-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d3430-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3430-119">Library</span></span><br/> | <dl> <span data-ttu-id="d3430-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3430-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3430-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3430-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3430-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="d3430-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
