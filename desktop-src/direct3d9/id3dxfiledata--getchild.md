---
description: 'Método ID3DXFileData::GetChild: recupera un objeto secundario en este objeto de datos de archivo.'
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: Método ID3DXFileData::GetChild (D3DX9Xof.h)
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
ms.openlocfilehash: 7fe6c0393e5cfb9ed8aeaf5808d33175e7f9bfe5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090383"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="09fb1-103">Método ID3DXFileData::GetChild</span><span class="sxs-lookup"><span data-stu-id="09fb1-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="09fb1-104">Recupera un objeto secundario en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="09fb1-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fb1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09fb1-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="09fb1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09fb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fb1-107">*uiChild* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="09fb1-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb1-108">Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09fb1-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09fb1-109">Identificador del objeto secundario que se recuperará.</span><span class="sxs-lookup"><span data-stu-id="09fb1-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="09fb1-110">*ppChild* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="09fb1-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb1-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="09fb1-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="09fb1-112">Dirección de un puntero para recibir el puntero de interfaz del objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="09fb1-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fb1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09fb1-113">Return value</span></span>

<span data-ttu-id="09fb1-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09fb1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09fb1-115">Si el método se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09fb1-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="09fb1-116">Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes valores: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="09fb1-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fb1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09fb1-117">Requirements</span></span>



| <span data-ttu-id="09fb1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fb1-118">Requirement</span></span> | <span data-ttu-id="09fb1-119">Value</span><span class="sxs-lookup"><span data-stu-id="09fb1-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09fb1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09fb1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="09fb1-121"><dt>D3DX9Xof.h</dt></span><span class="sxs-lookup"><span data-stu-id="09fb1-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="09fb1-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09fb1-122">Library</span></span><br/> | <dl> <span data-ttu-id="09fb1-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="09fb1-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="09fb1-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="09fb1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fb1-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="09fb1-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
