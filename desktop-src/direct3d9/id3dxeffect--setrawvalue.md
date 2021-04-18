---
description: Establezca un intervalo contiguo de constantes de sombreador con una copia de memoria.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'ID3DXEffect:: SetRawValue (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707793"
---
# <a name="id3dxeffectsetrawvalue-method"></a><span data-ttu-id="f6b61-103">ID3DXEffect:: SetRawValue (método)</span><span class="sxs-lookup"><span data-stu-id="f6b61-103">ID3DXEffect::SetRawValue method</span></span>

<span data-ttu-id="f6b61-104">Establezca un intervalo contiguo de constantes de sombreador con una copia de memoria.</span><span class="sxs-lookup"><span data-stu-id="f6b61-104">Set a contiguous range of shader constants with a memory copy.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6b61-105">Syntax</span></span>


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="f6b61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6b61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6b61-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f6b61-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b61-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f6b61-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f6b61-109">Identificador del valor que se va a establecer o nombre del valor que se pasa como una cadena.</span><span class="sxs-lookup"><span data-stu-id="f6b61-109">Handle to the value to set, or the name of the value passed in as a string.</span></span> <span data-ttu-id="f6b61-110">Pasar un identificador es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="f6b61-110">Passing in a handle is more efficient.</span></span> <span data-ttu-id="f6b61-111">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f6b61-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b61-112">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6b61-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b61-113">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="f6b61-113">Type: **void\***</span></span>

<span data-ttu-id="f6b61-114">Puntero a un búfer que contiene los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="f6b61-114">Pointer to a buffer containing the data to be set.</span></span> <span data-ttu-id="f6b61-115">SetRawValue comprueba la memoria válida, pero no realiza ninguna comprobación de datos válidos.</span><span class="sxs-lookup"><span data-stu-id="f6b61-115">SetRawValue checks for valid memory, but does not do any checking for valid data.</span></span>

</dd> <dt>

<span data-ttu-id="f6b61-116">*OffsetInBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6b61-116">*OffsetInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b61-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6b61-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6b61-118">Número de bytes entre el principio de los datos del efecto y el comienzo de las constantes del efecto que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="f6b61-118">Number of bytes between the beginning of the effect data and the beginning of the effect constants you are going to set.</span></span>

</dd> <dt>

<span data-ttu-id="f6b61-119">*Bytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6b61-119">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b61-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6b61-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6b61-121">Tamaño del búfer que se va a establecer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f6b61-121">The size of the buffer to be set, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6b61-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6b61-122">Return value</span></span>

<span data-ttu-id="f6b61-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6b61-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6b61-124">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f6b61-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f6b61-125">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: E \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f6b61-125">If the method fails, the return value can be one of the following:E\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6b61-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6b61-126">Remarks</span></span>

<span data-ttu-id="f6b61-127">SetRawValue es una manera muy rápida de establecer constantes de efecto, ya que realiza una copia de memoria sin realizar la validación ni ninguna conversión de datos (como la conversión de una matriz de filas principales en una matriz de columnas principal).</span><span class="sxs-lookup"><span data-stu-id="f6b61-127">SetRawValue is a very fast way to set effect constants since it performs a memory copy without performing validation or any data conversion (like converting a row-major matrix to a column-major matrix).</span></span> <span data-ttu-id="f6b61-128">Use SetRawValue para establecer una serie de constantes de efectos contiguos.</span><span class="sxs-lookup"><span data-stu-id="f6b61-128">Use SetRawValue to set a series of contiguous effect constants.</span></span> <span data-ttu-id="f6b61-129">Por ejemplo, puede establecer una matriz de veinte matrices con 20 llamadas a [**ID3DXBaseEffect:: SetMatrix**](id3dxbaseeffect--setmatrix.md) o mediante un solo SetRawValue.</span><span class="sxs-lookup"><span data-stu-id="f6b61-129">For instance, you could set an array of twenty matrices with 20 calls to [**ID3DXBaseEffect::SetMatrix**](id3dxbaseeffect--setmatrix.md) or by using a single SetRawValue.</span></span>

<span data-ttu-id="f6b61-130">Se espera que todos los valores sean matrix4x4s o float4s y se espera que todas las matrices estén en orden de columna principal.</span><span class="sxs-lookup"><span data-stu-id="f6b61-130">All values are expected to be either matrix4x4s or float4s and all matrices are expected to be in column-major order.</span></span> <span data-ttu-id="f6b61-131">Los valores int o float se convierten en una FLOAT4; por lo tanto, se recomienda encarecidamente que use SetRawValue solo con datos FLOAT4 o matrix4x4.</span><span class="sxs-lookup"><span data-stu-id="f6b61-131">Int or float values are cast into a float4; therefore, it is highly recommended that you use SetRawValue with only float4 or matrix4x4 data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b61-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6b61-132">Requirements</span></span>



| <span data-ttu-id="f6b61-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b61-133">Requirement</span></span> | <span data-ttu-id="f6b61-134">Value</span><span class="sxs-lookup"><span data-stu-id="f6b61-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b61-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6b61-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f6b61-136"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6b61-136"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f6b61-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6b61-137">Library</span></span><br/> | <dl> <span data-ttu-id="f6b61-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6b61-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f6b61-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6b61-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b61-140">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f6b61-140">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
