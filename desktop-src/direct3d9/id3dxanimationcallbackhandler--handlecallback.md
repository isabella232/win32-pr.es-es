---
description: 'La aplicación implementa este método. Se llama a este método cuando se produce una devolución de llamada para un conjunto de animaciones en una de las pistas durante una llamada a ID3DXAnimationController:: AdvanceTime.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'ID3DXAnimationCallbackHandler:: HandleCallback (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698390"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a><span data-ttu-id="148e1-104">ID3DXAnimationCallbackHandler:: HandleCallback (método)</span><span class="sxs-lookup"><span data-stu-id="148e1-104">ID3DXAnimationCallbackHandler::HandleCallback method</span></span>

<span data-ttu-id="148e1-105">La aplicación implementa este método.</span><span class="sxs-lookup"><span data-stu-id="148e1-105">The application implements this method.</span></span> <span data-ttu-id="148e1-106">Se llama a este método cuando se produce una devolución de llamada para un conjunto de animaciones en una de las pistas durante una llamada a [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="148e1-106">This method is called when a callback occurs for an animation set in one of the tracks during a call to [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="148e1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="148e1-107">Syntax</span></span>


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="148e1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="148e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="148e1-109">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="148e1-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="148e1-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="148e1-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="148e1-111">Identificador de la pista en la que se produce la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="148e1-111">Identifier of the track on which the callback occurs.</span></span>

</dd> <dt>

<span data-ttu-id="148e1-112">*pCallbackData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="148e1-112">*pCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="148e1-113">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="148e1-113">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="148e1-114">Puntero a los datos de devolución de llamada propiedad del usuario.</span><span class="sxs-lookup"><span data-stu-id="148e1-114">Pointer to user-owned callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="148e1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="148e1-115">Return value</span></span>

<span data-ttu-id="148e1-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="148e1-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="148e1-117">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="148e1-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="148e1-118">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="148e1-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="148e1-119">En caso contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="148e1-119">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="148e1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="148e1-120">Requirements</span></span>



| <span data-ttu-id="148e1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="148e1-121">Requirement</span></span> | <span data-ttu-id="148e1-122">Value</span><span class="sxs-lookup"><span data-stu-id="148e1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="148e1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="148e1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="148e1-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="148e1-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="148e1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="148e1-125">Library</span></span><br/> | <dl> <span data-ttu-id="148e1-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="148e1-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="148e1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="148e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="148e1-128">ID3DXAnimationCallbackHandler</span><span class="sxs-lookup"><span data-stu-id="148e1-128">ID3DXAnimationCallbackHandler</span></span>](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
