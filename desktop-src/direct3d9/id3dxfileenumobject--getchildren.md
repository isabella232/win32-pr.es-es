---
description: Recupera el número de objetos secundarios de este objeto de datos de archivo.
ms.assetid: 4409819f-a346-40b1-8e12-86e8128ece47
title: 'ID3DXFileEnumObject:: GetChildren (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cafa79844e89602d3b88756e04ca460f611516dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821207"
---
# <a name="id3dxfileenumobjectgetchildren-method"></a><span data-ttu-id="d555b-103">ID3DXFileEnumObject:: GetChildren (método)</span><span class="sxs-lookup"><span data-stu-id="d555b-103">ID3DXFileEnumObject::GetChildren method</span></span>

<span data-ttu-id="d555b-104">Recupera el número de objetos secundarios de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="d555b-104">Retrieves the number of child objects in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d555b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d555b-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="d555b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d555b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d555b-107">*puiChildren* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d555b-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d555b-108">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d555b-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d555b-109">Dirección de un puntero para recibir el número de objetos secundarios en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="d555b-109">Address of a pointer to receive the number of child objects in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d555b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d555b-110">Return value</span></span>

<span data-ttu-id="d555b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d555b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d555b-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d555b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d555b-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d555b-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d555b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d555b-114">Requirements</span></span>



| <span data-ttu-id="d555b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d555b-115">Requirement</span></span> | <span data-ttu-id="d555b-116">Value</span><span class="sxs-lookup"><span data-stu-id="d555b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d555b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d555b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d555b-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d555b-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d555b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d555b-119">Library</span></span><br/> | <dl> <span data-ttu-id="d555b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d555b-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d555b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d555b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d555b-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="d555b-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
