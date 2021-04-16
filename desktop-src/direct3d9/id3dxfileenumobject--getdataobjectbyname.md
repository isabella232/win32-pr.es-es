---
description: Recupera el objeto de datos que tiene el nombre especificado.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'ID3DXFileEnumObject:: GetDataObjectByName (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707969"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="6e6ab-103">ID3DXFileEnumObject:: GetDataObjectByName (método)</span><span class="sxs-lookup"><span data-stu-id="6e6ab-103">ID3DXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="6e6ab-104">Recupera el objeto de datos que tiene el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="6e6ab-104">Retrieves the data object that has the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e6ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e6ab-105">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="6e6ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e6ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e6ab-107">*szName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e6ab-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6ab-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e6ab-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e6ab-109">Puntero al nombre solicitado.</span><span class="sxs-lookup"><span data-stu-id="6e6ab-109">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="6e6ab-110">*ppObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e6ab-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6ab-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6e6ab-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="6e6ab-112">Dirección de un puntero a una interfaz [**ID3DXFileData**](id3dxfiledata.md) que representa el objeto de datos de archivo devuelto.</span><span class="sxs-lookup"><span data-stu-id="6e6ab-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e6ab-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e6ab-113">Return value</span></span>

<span data-ttu-id="6e6ab-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e6ab-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e6ab-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6e6ab-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6e6ab-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="6e6ab-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e6ab-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e6ab-117">Remarks</span></span>

<span data-ttu-id="6e6ab-118">Obtiene el nombre szName del objeto de datos de archivo actual con el método [**ID3DXFileData:: GetName**](id3dxfiledata--getname.md) .</span><span class="sxs-lookup"><span data-stu-id="6e6ab-118">Obtain the name szName of the current file data object with the [**ID3DXFileData::GetName**](id3dxfiledata--getname.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e6ab-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e6ab-119">Requirements</span></span>



| <span data-ttu-id="6e6ab-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e6ab-120">Requirement</span></span> | <span data-ttu-id="6e6ab-121">Value</span><span class="sxs-lookup"><span data-stu-id="6e6ab-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6ab-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e6ab-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6e6ab-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e6ab-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="6e6ab-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e6ab-124">Library</span></span><br/> | <dl> <span data-ttu-id="6e6ab-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e6ab-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6e6ab-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e6ab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e6ab-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="6e6ab-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
