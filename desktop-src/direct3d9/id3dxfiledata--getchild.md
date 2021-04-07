---
description: Recupera un objeto secundario en este objeto de datos de archivo.
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: 'ID3DXFileData:: GetChild (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 37982ca1e4801b7d70bec503ff9510fc66772651
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003876"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="f65d9-103">ID3DXFileData:: GetChild (método)</span><span class="sxs-lookup"><span data-stu-id="f65d9-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="f65d9-104">Recupera un objeto secundario en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f65d9-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f65d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f65d9-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="f65d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f65d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f65d9-107">*uiChild* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f65d9-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65d9-108">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f65d9-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f65d9-109">IDENTIFICADOR del objeto secundario que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f65d9-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f65d9-110">*ppChild* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f65d9-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65d9-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f65d9-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="f65d9-112">Dirección de un puntero para recibir el puntero de interfaz del objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="f65d9-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f65d9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f65d9-113">Return value</span></span>

<span data-ttu-id="f65d9-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f65d9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f65d9-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f65d9-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f65d9-116">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="f65d9-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="f65d9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f65d9-117">Requirements</span></span>



| <span data-ttu-id="f65d9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f65d9-118">Requirement</span></span> | <span data-ttu-id="f65d9-119">Value</span><span class="sxs-lookup"><span data-stu-id="f65d9-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f65d9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f65d9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f65d9-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="f65d9-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="f65d9-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f65d9-122">Library</span></span><br/> | <dl> <span data-ttu-id="f65d9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f65d9-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f65d9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f65d9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f65d9-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="f65d9-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
