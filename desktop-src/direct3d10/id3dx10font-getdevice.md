---
description: Recupere el dispositivo Direct3D asociado al objeto Font.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: 'ID3DX10Font:: GetDevice (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707897"
---
# <a name="id3dx10fontgetdevice-method"></a><span data-ttu-id="bf869-103">ID3DX10Font:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="bf869-103">ID3DX10Font::GetDevice method</span></span>

<span data-ttu-id="bf869-104">Recupere el dispositivo Direct3D asociado al objeto Font.</span><span class="sxs-lookup"><span data-stu-id="bf869-104">Retrieve the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf869-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf869-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="bf869-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf869-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf869-107">*ppDevice* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bf869-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf869-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="bf869-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="bf869-109">Dirección de un puntero a una interfaz ID3D10Device que representa el objeto de dispositivo de Direct3D asociado al objeto de fuente.</span><span class="sxs-lookup"><span data-stu-id="bf869-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf869-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf869-110">Return value</span></span>

<span data-ttu-id="bf869-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf869-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf869-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bf869-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bf869-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="bf869-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf869-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf869-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf869-115">Al llamar a este método, se aumentará el recuento de referencias interno en la interfaz ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="bf869-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span> <span data-ttu-id="bf869-116">Asegúrese de llamar a IUnknown cuando haya terminado de usar esta interfaz ID3D10Device o se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="bf869-116">Be sure to call IUnknown when you are done using this ID3D10Device interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf869-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf869-117">Requirements</span></span>



| <span data-ttu-id="bf869-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf869-118">Requirement</span></span> | <span data-ttu-id="bf869-119">Value</span><span class="sxs-lookup"><span data-stu-id="bf869-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf869-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf869-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bf869-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf869-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf869-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf869-122">Library</span></span><br/> | <dl> <span data-ttu-id="bf869-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf869-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf869-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf869-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf869-125">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="bf869-125">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="bf869-126">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="bf869-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




