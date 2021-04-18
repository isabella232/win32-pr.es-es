---
description: Recupera el objeto de datos que tiene el nombre especificado. En desuso.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'IDirectXFileEnumObject:: GetDataObjectByName (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718451"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="d0b3a-104">IDirectXFileEnumObject:: GetDataObjectByName (método)</span><span class="sxs-lookup"><span data-stu-id="d0b3a-104">IDirectXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="d0b3a-105">Recupera el objeto de datos que tiene el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="d0b3a-105">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="d0b3a-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="d0b3a-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b3a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0b3a-107">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="d0b3a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0b3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b3a-109">*szName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0b3a-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0b3a-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0b3a-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0b3a-111">Puntero al nombre solicitado.</span><span class="sxs-lookup"><span data-stu-id="d0b3a-111">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="d0b3a-112">*ppDataObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d0b3a-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0b3a-113">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0b3a-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="d0b3a-114">Dirección de un puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo devuelto.</span><span class="sxs-lookup"><span data-stu-id="d0b3a-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b3a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0b3a-115">Return value</span></span>

<span data-ttu-id="d0b3a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0b3a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0b3a-117">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0b3a-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d0b3a-118">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="d0b3a-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b3a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0b3a-119">Requirements</span></span>



| <span data-ttu-id="d0b3a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b3a-120">Requirement</span></span> | <span data-ttu-id="d0b3a-121">Value</span><span class="sxs-lookup"><span data-stu-id="d0b3a-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b3a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0b3a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d0b3a-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0b3a-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0b3a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0b3a-124">Library</span></span><br/> | <dl> <span data-ttu-id="d0b3a-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0b3a-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0b3a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0b3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b3a-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="d0b3a-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
