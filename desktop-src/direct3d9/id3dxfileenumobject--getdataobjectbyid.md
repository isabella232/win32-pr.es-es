---
description: Recupera el objeto de datos que tiene el GUID especificado.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'ID3DXFileEnumObject:: GetDataObjectById (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718319"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="4d180-103">ID3DXFileEnumObject:: GetDataObjectById (método)</span><span class="sxs-lookup"><span data-stu-id="4d180-103">ID3DXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="4d180-104">Recupera el objeto de datos que tiene el GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="4d180-104">Retrieves the data object that has the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d180-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d180-105">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="4d180-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d180-107">*rguid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d180-107">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d180-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="4d180-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="4d180-109">Referencia al GUID solicitado.</span><span class="sxs-lookup"><span data-stu-id="4d180-109">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="4d180-110">*ppDataObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4d180-110">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d180-111">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d180-111">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)\***</span></span>

<span data-ttu-id="4d180-112">Dirección de un puntero a una interfaz [**ID3DXFileData**](id3dxfiledata.md) que representa el objeto de datos de archivo devuelto.</span><span class="sxs-lookup"><span data-stu-id="4d180-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d180-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d180-113">Return value</span></span>

<span data-ttu-id="4d180-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4d180-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4d180-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4d180-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4d180-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="4d180-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d180-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d180-117">Remarks</span></span>

<span data-ttu-id="4d180-118">Obtiene el rguid GUID del objeto de datos de archivo actual con el método [**ID3DXFileData:: getId**](id3dxfiledata--getid.md) .</span><span class="sxs-lookup"><span data-stu-id="4d180-118">Obtain the GUID rguid of the current file data object with the [**ID3DXFileData::GetId**](id3dxfiledata--getid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d180-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d180-119">Requirements</span></span>



| <span data-ttu-id="4d180-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d180-120">Requirement</span></span> | <span data-ttu-id="4d180-121">Value</span><span class="sxs-lookup"><span data-stu-id="4d180-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d180-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d180-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4d180-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d180-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="4d180-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d180-124">Library</span></span><br/> | <dl> <span data-ttu-id="4d180-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d180-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4d180-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d180-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d180-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="4d180-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
