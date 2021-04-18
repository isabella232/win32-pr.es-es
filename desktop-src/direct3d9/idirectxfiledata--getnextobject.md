---
description: Recupera el siguiente objeto de datos secundario, el objeto de referencia de datos o el objeto binario del archivo de DirectX. En desuso.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'IDirectXFileData:: GetNextObject (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718387"
---
# <a name="idirectxfiledatagetnextobject-method"></a><span data-ttu-id="2b751-104">IDirectXFileData:: GetNextObject (método)</span><span class="sxs-lookup"><span data-stu-id="2b751-104">IDirectXFileData::GetNextObject method</span></span>

<span data-ttu-id="2b751-105">Recupera el siguiente objeto de datos secundario, el objeto de referencia de datos o el objeto binario del archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="2b751-105">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="2b751-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="2b751-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b751-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b751-107">Syntax</span></span>


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a><span data-ttu-id="2b751-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b751-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b751-109">*ppChildObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2b751-109">*ppChildObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2b751-110">Tipo: **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b751-110">Type: **[**LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span></span>

<span data-ttu-id="2b751-111">Dirección de un puntero a una interfaz [**IDirectXFileObject**](idirectxfileobject.md) que representa la interfaz de objeto de archivo del objeto secundario devuelta.</span><span class="sxs-lookup"><span data-stu-id="2b751-111">Address of a pointer to an [**IDirectXFileObject**](idirectxfileobject.md) interface, representing the returned child object's file object interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b751-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b751-112">Return value</span></span>

<span data-ttu-id="2b751-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b751-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b751-114">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b751-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="2b751-115">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="2b751-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b751-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b751-116">Remarks</span></span>

<span data-ttu-id="2b751-117">Para determinar el tipo de objeto recuperado, use QueryInterface para consultar el objeto recuperado para la compatibilidad de las interfaces [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md)o [**IDirectXFileBinary**](idirectxfilebinary.md) .</span><span class="sxs-lookup"><span data-stu-id="2b751-117">To determine the type of object retrieved, use QueryInterface to query the retrieved object for support of [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md), or [**IDirectXFileBinary**](idirectxfilebinary.md) interfaces.</span></span> <span data-ttu-id="2b751-118">La interfaz compatible indica el tipo de objeto (datos, referencia de datos o binario).</span><span class="sxs-lookup"><span data-stu-id="2b751-118">The interface supported indicates the type of object (data, data reference, or binary).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b751-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b751-119">Requirements</span></span>



| <span data-ttu-id="2b751-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b751-120">Requirement</span></span> | <span data-ttu-id="2b751-121">Value</span><span class="sxs-lookup"><span data-stu-id="2b751-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b751-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b751-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2b751-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b751-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b751-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b751-124">Library</span></span><br/> | <dl> <span data-ttu-id="2b751-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b751-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b751-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b751-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b751-127">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="2b751-127">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
</dt> <dt>

[<span data-ttu-id="2b751-128">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="2b751-128">**IDirectXFileData**</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="2b751-129">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="2b751-129">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




