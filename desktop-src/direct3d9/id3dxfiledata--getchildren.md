---
description: Recupera el número de elementos secundarios de este objeto de datos de archivo.
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: 'ID3DXFileData:: GetChildren (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dd6932801f3d4b079efa6f1ed2688505dbd7828b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670241"
---
# <a name="id3dxfiledatagetchildren-method"></a><span data-ttu-id="e3b8a-103">ID3DXFileData:: GetChildren (método)</span><span class="sxs-lookup"><span data-stu-id="e3b8a-103">ID3DXFileData::GetChildren method</span></span>

<span data-ttu-id="e3b8a-104">Recupera el número de elementos secundarios de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-104">Retrieves the number of children in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3b8a-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="e3b8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3b8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b8a-107">*puiChildren* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3b8a-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b8a-108">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3b8a-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e3b8a-109">Dirección de un puntero para recibir el número de elementos secundarios de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-109">Address of a pointer to receive the number of children in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b8a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3b8a-110">Return value</span></span>

<span data-ttu-id="e3b8a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3b8a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3b8a-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e3b8a-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e3b8a-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b8a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3b8a-114">Requirements</span></span>



| <span data-ttu-id="e3b8a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b8a-115">Requirement</span></span> | <span data-ttu-id="e3b8a-116">Value</span><span class="sxs-lookup"><span data-stu-id="e3b8a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b8a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b8a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b8a-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b8a-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e3b8a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3b8a-119">Library</span></span><br/> | <dl> <span data-ttu-id="e3b8a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3b8a-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e3b8a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3b8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b8a-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="e3b8a-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
