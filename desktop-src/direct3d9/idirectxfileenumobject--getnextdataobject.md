---
description: Recupera el siguiente objeto de nivel superior en el archivo de DirectX. En desuso.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'IDirectXFileEnumObject:: GetNextDataObject (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362445"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a><span data-ttu-id="bea97-104">IDirectXFileEnumObject:: GetNextDataObject (método)</span><span class="sxs-lookup"><span data-stu-id="bea97-104">IDirectXFileEnumObject::GetNextDataObject method</span></span>

<span data-ttu-id="bea97-105">Recupera el siguiente objeto de nivel superior en el archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="bea97-105">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="bea97-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="bea97-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea97-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bea97-107">Syntax</span></span>


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="bea97-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bea97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea97-109">*ppDataObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bea97-109">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bea97-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="bea97-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="bea97-111">Dirección de un puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo devuelto.</span><span class="sxs-lookup"><span data-stu-id="bea97-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bea97-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bea97-112">Return value</span></span>

<span data-ttu-id="bea97-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bea97-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bea97-114">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bea97-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="bea97-115">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bea97-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS</span></span>

## <a name="remarks"></a><span data-ttu-id="bea97-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bea97-116">Remarks</span></span>

<span data-ttu-id="bea97-117">Los objetos de nivel superior son siempre objetos de datos.</span><span class="sxs-lookup"><span data-stu-id="bea97-117">Top-level objects are always data objects.</span></span> <span data-ttu-id="bea97-118">Los objetos de referencia de datos y los objetos binarios solo pueden ser elementos secundarios de objetos de datos.</span><span class="sxs-lookup"><span data-stu-id="bea97-118">Data reference objects and binary objects can only be children of data objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="bea97-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea97-119">Requirements</span></span>



| <span data-ttu-id="bea97-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea97-120">Requirement</span></span> | <span data-ttu-id="bea97-121">Value</span><span class="sxs-lookup"><span data-stu-id="bea97-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bea97-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bea97-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bea97-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="bea97-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="bea97-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bea97-124">Library</span></span><br/> | <dl> <span data-ttu-id="bea97-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bea97-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bea97-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bea97-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea97-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="bea97-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 




