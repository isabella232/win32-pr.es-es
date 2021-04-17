---
description: Recupera el objeto de datos que tiene el GUID especificado. En desuso.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'IDirectXFileEnumObject:: GetDataObjectById (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717537"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="1f704-104">IDirectXFileEnumObject:: GetDataObjectById (método)</span><span class="sxs-lookup"><span data-stu-id="1f704-104">IDirectXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="1f704-105">Recupera el objeto de datos que tiene el GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="1f704-105">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="1f704-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="1f704-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f704-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f704-107">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="1f704-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f704-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f704-109">*rguid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f704-109">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f704-110">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="1f704-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="1f704-111">Referencia al GUID solicitado.</span><span class="sxs-lookup"><span data-stu-id="1f704-111">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="1f704-112">*ppDataObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1f704-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f704-113">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f704-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="1f704-114">Dirección de un puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo devuelto.</span><span class="sxs-lookup"><span data-stu-id="1f704-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f704-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f704-115">Return value</span></span>

<span data-ttu-id="1f704-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f704-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f704-117">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f704-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="1f704-118">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="1f704-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f704-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f704-119">Requirements</span></span>



| <span data-ttu-id="1f704-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f704-120">Requirement</span></span> | <span data-ttu-id="1f704-121">Value</span><span class="sxs-lookup"><span data-stu-id="1f704-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f704-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f704-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1f704-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f704-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f704-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f704-124">Library</span></span><br/> | <dl> <span data-ttu-id="1f704-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f704-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f704-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f704-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f704-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="1f704-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
