---
description: Obtiene acceso a los datos del archivo. x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'ID3DXFileData:: Lock (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718321"
---
# <a name="id3dxfiledatalock-method"></a><span data-ttu-id="029c6-103">ID3DXFileData:: Lock (método)</span><span class="sxs-lookup"><span data-stu-id="029c6-103">ID3DXFileData::Lock method</span></span>

<span data-ttu-id="029c6-104">Obtiene acceso a los datos del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="029c6-104">Accesses the .x file data.</span></span>

## <a name="syntax"></a><span data-ttu-id="029c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="029c6-105">Syntax</span></span>


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="029c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="029c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029c6-107">*pSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="029c6-107">*pSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="029c6-108">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="029c6-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="029c6-109">Puntero al tamaño de los datos del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="029c6-109">Pointer to the size of the .x file data.</span></span>

</dd> <dt>

<span data-ttu-id="029c6-110">*ppData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="029c6-110">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="029c6-111">Tipo: **const void \* \***</span><span class="sxs-lookup"><span data-stu-id="029c6-111">Type: **const VOID\*\***</span></span>

<span data-ttu-id="029c6-112">Dirección de un puntero para recibir el puntero de interfaz del objeto de datos del archivo [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="029c6-112">Address of a pointer to receive the [**ID3DXFileData**](id3dxfiledata.md) file data object's interface pointer.</span></span> <span data-ttu-id="029c6-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="029c6-113">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="029c6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="029c6-114">Return value</span></span>

<span data-ttu-id="029c6-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="029c6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="029c6-116">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="029c6-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="029c6-117">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="029c6-117">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="029c6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="029c6-118">Remarks</span></span>

<span data-ttu-id="029c6-119">El puntero *ppData* solo es válido durante un **ID3DXFileData:: Lock** ... [**ID3DXFileData:: Unlock**](id3dxfiledata--unlock.md) (secuencia).</span><span class="sxs-lookup"><span data-stu-id="029c6-119">The *ppData* pointer is only valid during a **ID3DXFileData::Lock** ... [**ID3DXFileData::Unlock**](id3dxfiledata--unlock.md) sequence.</span></span> <span data-ttu-id="029c6-120">Puede realizar varias llamadas de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="029c6-120">You can make multiple lock calls.</span></span> <span data-ttu-id="029c6-121">Sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="029c6-121">However, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="029c6-122">Dado que no se garantiza que los datos de archivo se alineen correctamente con límites de bytes, debe acceder a *ppData* con punteros no alineados.</span><span class="sxs-lookup"><span data-stu-id="029c6-122">Because file data is not guaranteed to be aligned properly with byte boundaries, you should access *ppData* with UNALIGNED pointers.</span></span>

<span data-ttu-id="029c6-123">No se garantiza que los valores de parámetro devueltos sean válidos debido a posibles daños en los archivos. por lo tanto, el código debe comprobar los valores de parámetro devueltos.</span><span class="sxs-lookup"><span data-stu-id="029c6-123">Returned parameter values are not guaranteed to be valid due to possible file corruption; therefore, your code should verify the returned parameter values.</span></span>

## <a name="requirements"></a><span data-ttu-id="029c6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="029c6-124">Requirements</span></span>



| <span data-ttu-id="029c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="029c6-125">Requirement</span></span> | <span data-ttu-id="029c6-126">Value</span><span class="sxs-lookup"><span data-stu-id="029c6-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="029c6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="029c6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="029c6-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="029c6-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="029c6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="029c6-129">Library</span></span><br/> | <dl> <span data-ttu-id="029c6-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="029c6-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="029c6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="029c6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029c6-132">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="029c6-132">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
