---
description: Recupera los datos para uno de los miembros del objeto o los datos de todos los miembros. En desuso.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'IDirectXFileData:: GetData (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718388"
---
# <a name="idirectxfiledatagetdata-method"></a><span data-ttu-id="3f71d-104">IDirectXFileData:: GetData (método)</span><span class="sxs-lookup"><span data-stu-id="3f71d-104">IDirectXFileData::GetData method</span></span>

<span data-ttu-id="3f71d-105">Recupera los datos para uno de los miembros del objeto o los datos de todos los miembros.</span><span class="sxs-lookup"><span data-stu-id="3f71d-105">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="3f71d-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="3f71d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f71d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f71d-107">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a><span data-ttu-id="3f71d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f71d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f71d-109">*szMember* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f71d-109">*szMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f71d-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f71d-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f71d-111">Puntero al nombre del miembro para el que se van a recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="3f71d-111">Pointer to the name of the member for which to retrieve data.</span></span> <span data-ttu-id="3f71d-112">Especifique **null** para recuperar los datos de todos los miembros necesarios.</span><span class="sxs-lookup"><span data-stu-id="3f71d-112">Specify **NULL** to retrieve all required members' data.</span></span>

</dd> <dt>

<span data-ttu-id="3f71d-113">*PCB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f71d-113">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f71d-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f71d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3f71d-115">Puntero para recibir el tamaño de búfer de ppvData, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3f71d-115">Pointer to receive the ppvData buffer size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3f71d-116">*ppvData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f71d-116">*ppvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f71d-117">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="3f71d-117">Type: **void\*\***</span></span>

<span data-ttu-id="3f71d-118">Dirección de un puntero al búfer para recibir los datos asociados a szMember.</span><span class="sxs-lookup"><span data-stu-id="3f71d-118">Address of a pointer to the buffer to receive the data associated with szMember.</span></span> <span data-ttu-id="3f71d-119">Si szMember es **null**, ppvData se establece para que apunte a un búfer que contiene todos los datos de los miembros necesarios en un bloque de memoria contiguo.</span><span class="sxs-lookup"><span data-stu-id="3f71d-119">If szMember is **NULL**, ppvData is set to point to a buffer containing all required members' data in a contiguous block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f71d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f71d-120">Return value</span></span>

<span data-ttu-id="3f71d-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f71d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f71d-122">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3f71d-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3f71d-123">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDATAREFERENCE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="3f71d-123">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADDataReference, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f71d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f71d-124">Remarks</span></span>

<span data-ttu-id="3f71d-125">Este método recupera los datos para los miembros necesarios de un objeto de datos, pero no los datos de los miembros (secundarios) opcionales.</span><span class="sxs-lookup"><span data-stu-id="3f71d-125">This method retrieves the data for required members of a data object but no data for optional (child) members.</span></span> <span data-ttu-id="3f71d-126">Use [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) para recuperar objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="3f71d-126">Use [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) to retrieve child objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f71d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f71d-127">Requirements</span></span>



| <span data-ttu-id="3f71d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f71d-128">Requirement</span></span> | <span data-ttu-id="3f71d-129">Value</span><span class="sxs-lookup"><span data-stu-id="3f71d-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f71d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f71d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3f71d-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f71d-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f71d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f71d-132">Library</span></span><br/> | <dl> <span data-ttu-id="3f71d-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f71d-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f71d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f71d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f71d-135">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="3f71d-135">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="3f71d-136">**IDirectXFileData::GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="3f71d-136">**IDirectXFileData::GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
